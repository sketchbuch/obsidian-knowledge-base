# Overwrite inherited prop

How to override an inherited prop.

---

```ts
export interface InterfaceA {
  value: string
}

export interface InterfaceB extends Omit<InterfaceA, 'value'> {
  value: boolean
  value2: string
}

const testA: InterfaceA = {
  value: "test",
}

const testB: InterfaceB = {
  value: true,
  value2: "test2",
}
```