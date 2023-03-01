# API (Application Programming Interface)

```
API is an abbreviation for Application Programming Interface which is a collection of communication protocols and subroutines 
used by various programs to communicate between them.
A programmer can make use of various API tools to make its program easier and simpler. 
Also, an API facilitates the programmers with an efficient way to develop their software programs.
```

## How we fetch the data from API 

## Using Fetch Method:

```
import React from "react";
import './App.css';
class App extends React.Component {

	// Constructor
	constructor(props) {
		super(props);

		this.state = {
			items: [],
			DataisLoaded: false
		};
	}

	// ComponentDidMount is used to
	// execute the code
	componentDidMount() {
		fetch(
"https://jsonplaceholder.typicode.com/users")
			.then((res) => res.json())
			.then((json) => {
				this.setState({
					items: json,
					DataisLoaded: true
				});
			})
	}
	render() {
		const { DataisLoaded, items } = this.state;
		if (!DataisLoaded) return <div>
			<h1> Pleses wait some time.... </h1> </div> ;

		return (
		<div className = "App">
			<h1> Fetch data from an api in react </h1> {
				items.map((item) => (
				<ol key = { item.id } >
					User_Name: { item.username },
					Full_Name: { item.name },
					User_Email: { item.email }
					</ol>
				))
			}
		</div>
	);
}
}

export default App;
```

## Output:

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20210817165343/out.gif" />

# Using Axios
```
Use npm i axios to install axios and then add it as an import to your parent component. 
I’m going to use axios to get all of my notes, which I stored in a database.
```
## Output:

<img src="https://levelup.gitconnected.com/fetch-api-data-with-axios-and-display-it-in-a-react-app-with-hooks-3f9c8fa89e7b" />

## Fetch API using async/await:

```
import React, { useState, useEffect } from 'react'
import axios from 'axios';

function App() {

	const [loading, setLoading] = useState(false);
	const [posts, setPosts] = useState([]);

	useEffect(() => {
		const loadPost = async () => {

			// Till the data is fetch using API
			// the Loading page will show.
			setLoading(true);

			// Await make wait until that
			// promise settles and return its result
			const response = await axios.get(
			"https://jsonplaceholder.typicode.com/posts/");

			// After fetching data stored it in posts state.
			setPosts(response.data);

			// Closed the loading page
			setLoading(false);
		}

		// Call the function
		loadPost();
	}, []);

	return (
		<>
			<div className="App">
				{loading ? (
					<h4>Loading...</h4>) :
					(posts.map((item) =>
						// Presently we only fetch
						// title from the API
						<h4>{item.title}</h4>)
					)
				}
			</div>
		</>
	);
}

export default App;

```

## Output:

<img src="https://www.geeksforgeeks.org/how-to-fetch-data-from-apis-using-asynchronous-await-in-reactjs/" />











