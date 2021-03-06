## Foundation

[JavaScript to Know for React](https://kentcdodds.com/blog/javascript-to-know-for-react)

### Rest/Spread

```
 Math.max(...arr)
 // is the same as
 Math.max.apply(null, arr)
```

```
 console.log({...obj1, ...obj2})
 // is the same as
 console.log(Object.assign({}, obj1, obj2))
```

### Dynamic Import

```
// dynamic import of a React component
const BigComponent = React.lazy(() => import('./big-component'))
// big-component.js would need to "export default BigComponent" for this to work
```

### Array Methods

```
dogs.find(dog => dog.name === 'Bernese Mountain Dog')
// {id: 'dog-2', name: 'Bernese Mountain Dog', ...etc}

dogs.some(dog => dog.temperament.includes('Aggressive'))
// false

dogs.some(dog => dog.temperament.includes('Trusting'))
// true

dogs.every(dog => dog.temperament.includes('Trusting'))
// false

dogs.every(dog => dog.temperament.includes('Intelligent'))
// true

dogs.map(dog => dog.name)
// ['Poodle', 'Bernese Mountain Dog', 'Labrador Retriever']

dogs.filter(dog => dog.temperament.includes('Faithful'))
// [{id: 'dog-1', ..etc}, {id: 'dog-2', ...etc}]

dogs.reduce((allTemperaments, dog) => {
  return [...allTemperaments, ...dog.temperament]
}, [])
// [ 'Intelligent', 'Active', 'Alert', ...etc ]
```

### Nullish coalescing operator (??)

```
const foo = x ?? 'default string';
console.log(foo);
// expected output: "default string" if x is null/undefined

```

## Into React

[Imperative vs Declarative](https://ui.dev/imperative-vs-declarative-programming/)

> An imperative approach (HOW): “I see that table located next to the tree decoration is empty. My husband
> and I are going to walk over there and sit down.”

> A declarative approach (WHAT): “Table for two, please.”

- React: responsible for creating React elements (kinda like document.createElement())
- ReactDOM: responsible for rendering React elements to the DOM (kinda like rootElement.append())

## How JSX gets compiled to JavaScript,

[check out the online babel REPL here](https://babeljs.io/repl#?builtIns=App&code_lz=MYewdgzgLgBArgSxgXhgHgCYIG4D40QAOAhmLgBICmANtSGgPRGm7rNkDqIATtRo-3wMseAFBA&presets=react&prettier=true).
