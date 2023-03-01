## Stylig with Material UI
- Material UI is an open-source React component library that implements Google's Material Design. 
- It includes a comprehensive collection of prebuilt components that are ready for use in production right out of the box.

#### Installing Material UI
`$ npm install @material-ui/core @material-ui/icons`

## Button

![Screenshot 2023-03-01 124609](https://user-images.githubusercontent.com/94469107/222069903-d2103370-83ea-47cb-a7a6-8264bdb10b84.png)

## ColorPicker

![Screenshot 2023-03-01 124819](https://user-images.githubusercontent.com/94469107/222070287-61f0fd15-a016-4906-b53b-9753abe9390a.png)

# Form

## useState + Form

![Screenshot 2023-03-01 133901](https://user-images.githubusercontent.com/94469107/222080967-9230c539-953f-47b7-a875-e0e8dafa1ae7.png)

## useEffect + Form

![Screenshot 2023-03-01 134614](https://user-images.githubusercontent.com/94469107/222082455-575324f8-17fd-46cd-bb5c-b3096dae5629.png)

## useContext + Form

```
const MyContext = React.createContext();


const useMyContext = (section, init) => {
  // context and setContext came from MyContext.Provider
 
 const { context, setContext } = React.useContext(MyContext)
  const data = (context[section] === undefined) ? init : context[section]
  const setData = (data) => setContext({...context, [section]: data})
  return [data, setData]
}

// data and actions provider
const useNameForm = () => {
  const init = {
    values: {
      name: '',
      surname: '',
    },
    errors: []
  }
  const [data, setData] = useMyContext('formName', init)
  const changeValue = (input, value) => {
    setData({...data, values: {...data.values, [input]: value}})
  }
  const setErrors = errors => {
    setData({...data, errors})
  }
  return {data, changeValue, setErrors}
}

const Content = (props) => {
  const {data, changeValue, setErrors} = useNameForm()

  const handleChange = (event) => {
    changeValue(event.target.name, event.target.value);
  }
  
  const validate = (values) => {
    const errors = []
    !values.name && errors.push("Name is required")
    !values.surname && errors.push("surname is required")
    setErrors(errors)
    return errors.length === 0
  }
  
  const handleSubmit = (event) => {
    if(validate(data.values)){
      alert('form submited: ' + JSON.stringify(data.values))
    }
    event.preventDefault();
  }
  
  return (
    <form onSubmit={handleSubmit}>
      <label>Name: <input type="text" value={data.values.name}
                     name="name" onChange={handleChange} /></label><br />
      <label>Surname: <input type="text" value={data.values.surname} 
                        name="surname" onChange={handleChange} /></label>
      <input type="submit" value="Submit" />
      {data.errors.length > 0 && data.errors.map((err,i) => (
        <p key={i}>{err}</p>
      ))}
    </form>
  );
}

const DeepComponent = () => {
  const { data } = useNameForm('formName')
  return <div><br />DeepComponent:
              <br />name: {data.values.name}
              <br />surname: {data.values.surname}</div>
}

const App = (props) => {
  const [data, setData] = React.useState({})
  return (
    <MyContext.Provider value={{
        context: data,
        setContext: newData => setData(newData)
      }}>
      <Content />
      <DeepComponent />
    </MyContext.Provider>
  )
}

ReactDOM.render(
  <App />,
  document.getElementById('root')
);
```

## useReducer + Form

```
import { useReducer } from "react"

type FormState = {
    firstName: string
    lastName: string
    age: string
    email: string
    password: string
}
const initialState: FormState = {
    firstName: "",
    lastName: "",
    age: "",
    email: "",
    password: ""
}
type FormValidityState = {
    firstNameError: boolean
    lastNameError: boolean
    ageError: boolean
    emailError: boolean
    passwordError: boolean
    isFormValid: boolean
}
const initialValidityState: FormValidityState = {
    firstNameError: false,
    lastNameError: false,
    ageError: false,
    emailError: false,
    passwordError: false,
    isFormValid: false
}
type FormAction = {
    type: string
    payLoad: string
}
type FormValidityAction = {
    type: string
    payLoad: FormState
}
const formReducer = (state: FormState, action: FormAction): FormState => {
    switch(action.type){
        case "UPDATE_FIRST_NAME": return{
            ...state, firstName: action.payLoad, 
        }
        case "UPDATE_LAST_NAME": return{
            ...state,lastName: action.payLoad, 
        }
        case "UPDATE_AGE": return{
            ...state, age: action.payLoad, 
        }
        case "UPDATE_EMAIL": return{
            ...state, email: action.payLoad, 
        }
        case "UPDATE_PASSWORD": return{
            ...state, password: action.payLoad, 
        }
        default:
            return state
    }
}
const formValidityReducer = (state: FormValidityState, action: FormValidityAction): FormValidityState => {
    let isValid: boolean = false;
    switch(action.type){
        
        case "VALIDATE_FIRST_NAME": 
        isValid = action.payLoad.firstName.length > 0 ? true: false
        return{
            ...state,
            ...({firstNameError: !isValid, isFormValid: isValid && !state.lastNameError && !state.ageError && !state.emailError && !state.passwordError}),
        }
        case "VALIDATE_LAST_NAME": 
        isValid = action.payLoad.lastName.length > 0 ? true: false
        return{
            ...state,
            ...({lastNameError: !isValid, isFormValid: isValid && !state.firstNameError && !state.ageError && !state.emailError && !state.passwordError})
        }
        case "VALIDATE_AGE": 
        isValid = action.payLoad.age.length > 0 ? true: false
        return{
            ...state,
            ...({ageError: !isValid, isFormValid: isValid && !state.firstNameError && !state.lastNameError && !state.emailError && !state.passwordError})
        }
        case "VALIDATE_EMAIL": 
        isValid = (action.payLoad.email.length > 0 && action.payLoad.email.includes("@")) ? true: false
        return{
            ...state,
            ...({emailError: !isValid, isFormValid: isValid && !state.firstNameError && !state.lastNameError && !state.ageError && !state.passwordError})
        }
        case "VALIDATE_PASSWORD": 
        isValid = action.payLoad.password.length > 9 ? true: false
        return{
            ...state,
            ...({passwordError: !isValid, isFormValid: isValid && !state.firstNameError && !state.lastNameError && !state.ageError && !state.emailError})
        }
    default:
        return state
    }
}

export const Form = () => {
    const [formData, setFormData] = useReducer(formReducer, initialState)
    const [formValidityData, setFormValidityData] = useReducer(formValidityReducer, initialValidityState)

    const onButtonPress = (event: React.FormEvent<HTMLFormElement>) => {
        event.preventDefault()
        console.log(formData)
        //Form submission happens here
    }
    return(
        <div style={STYLE.container}>
        <form onSubmit={onButtonPress}>
            <label style={STYLE.formElement} htmlFor="first_name">First Name</label>
            <div style={STYLE.formElement}>
                <input 
                id="first_name" 
                style={{backgroundColor:formValidityData.firstNameError ?"pink" : ""}} 
                onChange={(e) =>setFormData({type:"UPDATE_FIRST_NAME", payLoad:e.target.value})}
                onBlur={(e) => setFormValidityData({type: "VALIDATE_FIRST_NAME", payLoad: formData})}
                type="text"/>
            </div>
           <label style={STYLE.formElement} htmlFor="last_name">Last Name</label>
            <div style={STYLE.formElement}>
                <input 
                id="last_name" 
                style={{backgroundColor:formValidityData.lastNameError ? "pink" : ""}} 
                onChange={(e) =>setFormData({type:"UPDATE_LAST_NAME", payLoad:e.target.value})}
                onBlur={(e) => setFormValidityData({type: "VALIDATE_LAST_NAME", payLoad: formData})}
                type="text"/>
            </div>
            <label style={STYLE.formElement} htmlFor="last_name">Email</label>
            <div style={STYLE.formElement}>
                <input 
                id="email" 
                style={{backgroundColor:formValidityData.emailError ? "pink" : ""}} 
                onChange={(e) =>setFormData({type:"UPDATE_EMAIL", payLoad:e.target.value})}
                onBlur={(e) => setFormValidityData({type: "VALIDATE_EMAIL", payLoad: formData})}
                type="text"/>
            </div>
            <label style={STYLE.formElement} htmlFor="last_name">Password</label>
            <div style={STYLE.formElement}>
                <input 
                id="password" 
                style={{backgroundColor:formValidityData.passwordError ? "pink" : ""}} 
                onChange={(e) =>setFormData({type:"UPDATE_PASSWORD", payLoad:e.target.value})}
                onBlur={(e) => setFormValidityData({type: "VALIDATE_PASSWORD", payLoad: formData})}
                type="password"/>
            </div>
           <label style={STYLE.formElement} htmlFor="age">Age</label>
            <div style={STYLE.formElement}>
                <input 
                id="age" 
                style={{backgroundColor:formValidityData.ageError ? "pink" : ""}} 
                onChange={(e) =>setFormData({type:"UPDATE_AGE", payLoad:e.target.value})} 
                onBlur={(e) => setFormValidityData({type: "VALIDATE_AGE", payLoad: formData})}
                type="number"/>
            </div>
            <div style={STYLE.formElement}>
                <input disabled={!formValidityData.isFormValid} type="submit" value={""+formValidityData.isFormValid}/>
            </div>
        </form>
        </div>
    )
}
const STYLE = {
    container: {
        borderRadius: "5px",
        backgroundColor: "#f2f2f2",
        padding: "20px",
        maxWidth:"240px"
    },
    formElement: {
        padding: "6px 24px"
    }
}
```

## useRef + Form

```
import React, { useRef } from "react"

export default function App() {
  const nameRef = useRef();
  const emailRef = useRef()
  const passwordRef = useRef()

  function handleSubmit(e) {
    e.preventDefault()
    //output the name
    console.log(nameRef.current.value)
    //output the email
    console.log(emailRef.current.value)
  }

  return (
    <div className="container">
      <form onSubmit={handleSubmit}>
        <div className="input_group">
          <label>Name</label>
          <input type="text" ref={nameRef}/>
        </div>
        <div className="input_group">
          <label>Email</label>
          <input type="text" ref={emailRef}/>
        </div>
        <div className="input_group">
          <label>Password</label>
          <input type="password" ref={passwordRef}/>
        </div>
        <input type="submit"/>
      </form>
    </div>
  )
}
```













