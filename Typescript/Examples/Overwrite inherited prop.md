```ts
export interface InterfaceA {  
	value: string  
}  
  
export interface InterfaceB extends Omit<InterfaceA, 'value' | 'value2'> {  
	value: boolean  
	value2: string  
}
```
