# ObjectDestructing
ES6 feature object destructing to initialise variables

**A simple non-nested object can be destructured like this:**
```
const data = { a: 'ananas', b: 'banana'};
let { a } = data;
// a === 'ananas'
```

If you have nested data you need to specify that you want to destructure an internal object. You do this by specifying the name of the object you want to destructure, just like a normal destructure

```
  let { anObject } = data;
```

and then to destructure its content you add another destructure syntax after a colon

```
  let { anObject: { a } } = data;
```

which means you want to access/destructure the property a within the object specified by the property anObject.

```
let data = {
  anObject: {
    c: 'car',
    d: 'dandelion'
  }
};

let { anObject } = data;
console.log(anObject);

//let { c } = anObject;
//console.log( c );

let { anObject: { c } } = data;
console.log( c );
```

Credit goes to **Fredrik Nygren**
