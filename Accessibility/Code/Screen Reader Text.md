# Screen Reader Text

How to make screen reader only text that is in the Document Object Model ([DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)) for Screen Readers to see but is not visible to normal users.

---
## Styled Components

An example for [Styled Components](https://styled-components.com/).

```js
export const ScreenreaderTextSpan = styled.span`  
	border: 0;  
	clip-path: inset(50%);  
	clip: rect(0, 0, 0, 0);  
	height: 1px;  
	margin: -1px;  
	overflow: hidden;  
	padding: 0;  
	position: absolute;  
	white-space: nowrap;  
	width: 1px;  
`
```
