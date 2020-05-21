# 12 await
``` javascript
try{
	const response = await fetch(endpoint);
	if(response.ok){
		let jsonResponse = await response.json();
		renderWordResponse(jsonResponse);
	}
}
```

so `fetch` calls the endpoint url and returns a response, it is like an `iou`, so await takes that `iou`, and it lets the rest of the code to run, once the real response from the fetch comes back, await assigns it to response, so everything that uses response now will be filled with the right value

`await` only pairs up with async on functions that will be working with promises. and it is declared before any promise, like in the case of fetch.

`Await` causes an async function to pause execution until the desired Promise is resolved.
#CodeCademy Learn React/08 - Requests#