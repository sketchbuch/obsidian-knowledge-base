# Force a non-nullable value for children

How to make sure a property is non-nullable in an interface, like React children for example

---

```ts
children: NonNullable<React.ReactNode>
```