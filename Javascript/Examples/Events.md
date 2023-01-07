# Events

Information about events in Javascript.

---

## Event Binding

```js
const wsElements = document.getElementsByClassName('list__element');  
  
window.addEventListener('unload', () => {  
	Array.from(wsElements).forEach((element) => {  
		element.removeEventListener('click', handleElementClick);  
	});  
});
```