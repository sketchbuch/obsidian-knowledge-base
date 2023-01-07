# Tuple as argument in Typescript

An example from [BytesDev](https://bytes.dev/archives/101)

---

```ts
function addTriple(inputs: number[]): number {  
	return inputs[0] + inputs[1] + inputs[2];  
}  
```

TypeScript will warn us if we pass anything but an array of numbers to that function, but if the array has less than 3 items in it, the third item will be undefined and our function will return NaN. TypeScript can’t know how many items are in the array, so it can’t warn us.  
  
There are many solutions to this. One would have us change our type signature to be a tuple type instead of an array. TypeScript can then warn us if our array doesn’t have enough options.  
  
```ts
function addTriple(inputs: [number, number, number]): number {  
	return inputs[0] + inputs[1] + inputs[2];  
}  
```

Another option is to enable the noUncheckedIndexedAccess TypeScript compiler option, which will force us to check that each item isn’t undefined.  
  
```ts
function addTriple(inputs: number[]): number {  
	if (  
	inputs[0] === undefined ||  
	inputs[1] === undefined ||  
	inputs[2] === undefined  
	) {  
		throw new Error("Invalid input");  
	}  
	  
	return inputs[0] + inputs[1] + inputs[2];  
}
```