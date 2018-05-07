## Coding Taste

\*The following documented some coding style that can't be enforced by a linter, we called it coding taste.

*\*Of course we can write a plugin for that, but we have more important stuff to do.*

1. Use ES6 export when exporting class

```js
// WE DO

  export default class Foo extends Bar {
    ...
  }

  export class Foo extends Bar {
    ...
  }

// WE DON'T

  class Foo extends Bar {
    ...
  }

  export default Foo;

  // OR

  module.exports = Foo;
```

2. Use spread operator when the parameter's name and its value's expression are the same.

```js
// WE DO

  <Text
    {...{ foo, bar }}
  />

  <Text
    foo={foo1}
    {...{ bar }}
  />

// WE DON'T

  <Text
    foo={foo} bar={bar}
  />

  <Text
    foo={foo1}
    bar={bar}
  />
```

3. Some naming we use in our specs.

```js
// WE DO

const wrapper = shallow(<div>hello</div>);

// WE DON'T

const div = shallow(<div>hello</div>);
```

4. Some jest expectation we use.

```js
// GIVEN
const onClick = jest.fn();
const wrapper = shallow(<div {...{ onClick }}></div>);
```

```js
// WE DO

const onClick = jest.fn();
const wrapper = shallow(<div {...{ onClick }}></div>);

wrapper.simulte('click');
expect(onClick).toHaveBeenCalledTimes(1);

// WE DON'T

wrapper.simulte('click');
expect(onClick.mock.calls.length).toEqual(1);

```
