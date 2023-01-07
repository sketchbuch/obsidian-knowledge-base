# Types from Arrays

How to create types from arrays - use instead of enums.

---

```ts
export const fields = ['birthday', 'email', 'firstName', 'lastName', 'salutation'] as const  
type FieldsTuple = typeof fields  
export type Fields = FieldsTuple[number]  
  
export const BreakpointSizes = ['xs', 'sm', 'md', 'lg', 'xl'] as const;  
  
export type BreakpointSizesType = typeof BreakpointSizes[number];  
  
export interface Breakpoints {  
	keys: BreakpointSizesType[];  
	values: { [Key in BreakpointSizesType]: number };  
}
```
