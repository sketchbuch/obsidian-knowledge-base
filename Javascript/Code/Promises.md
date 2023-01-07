# Promises

Infromation about promises in Javascript.

---

## Promise example

```js
import 'babelify/polyfill'  
  
function loadImage(url) {  
	return new Promise((resolve, reject) => {  
		let image = new Image()  
		  
		image.onload = function() {  
			resolve(image)  
		}  
		  
		image.onerror = function() {  
			let message =  
			'Could not load image at ' + url  
			reject(new Error(msg))  
		}  
		  
		image.src = url  	  
	})  
}

export default loadImage  
  
---
  
import loadImage from './load-image'  
  
let addImg = (src) => {  
	let imgElement =  
	document.createElement("img")  
	imgElement.src = src  
	document.body.appendChild(imgElement)  
}  
  
Promise.all([  
	loadImage('images/cat1.jpg'),  
	loadImage('images/cat2.jpg'),  
	loadImage('images/cat3.jpg'),  
	loadImage('images/cat4.jpg')  
]).then((images) => {  
	images.forEach(img => addImg(img.src))  
}).catch((error) => {  
	// handle error later  
})
```

## Sequentially calling promises - one after the other

```js
const values = [1, 2, 3, 4, 5].filter((num) => num % 2)  
  
function sendNextRequest() {  
	const value = values.shift()  
	
	if (value) {  
		doNetworkCall(value).then(sendNextRequest)  
	}  
}  
  
const values = [1, 2, 3, 4, 5].filter((num) => num % 2)  
  
const doNetworkCall = (value) => { return Promise.resolve() }  
  
const sendRequest = (index) => {  
	if (values[index]) {  
		doNetworkCall(values[index]).then(() => sendRequest(index + 1))  
	}  
}  
  
sendRequest(0)  
  
  
=====  
  
anArray  
.filter(x => x % 2) // odd only  
.reduce(  
	(chain, x) => chain.then(() => networkCall(x)), // network call using an odd  
	Promise.resolve()  
)  
.then(() => console.log('all done')) // all calls complete
```

## Simulate a delay using a promise

```js
Delay Method  
const delay = seconds => new Promise(resolve => setTimeout(resolve), seconds * 1000);
```
