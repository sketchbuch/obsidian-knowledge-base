```ts
interface WithAriaLabel {  
	  ariaLabel: string  
	  ariaLabelledby?: never  
}  
  
interface WithAriaLabelledby {  
	  ariaLabel?: never  
	  ariaLabelledby: string  
}  
  
export type FormProps = {  
	action?: string  
	autocomplete?: 'off' | 'on'  
	children: ReactNode  
	enctype?: 'application/x-www-form-urlencoded' | 'multipart/form-data' | 'text/plain'  
	id?: string  
	method?: 'post' | 'get' | 'dialog'  
	novalidate?: boolean  
	onSubmit?: (event: FormEvent<HTMLFormElement>) => void  
	testId?: string  
} & (WithAriaLabel | WithAriaLabelledby)
```
