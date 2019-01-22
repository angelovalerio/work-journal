#### Resources
- https://github.com/acdlite/react-fiber-architecture
  - https://reactjs.org/blog/2015/12/18/react-components-elements-and-instances.html
- https://reactjs.org/blog/all.html


#### Concepts
- New Concepts
  - Continuation
  - monads
  - Algebraic Effects
- React creates elements as objects with just two properties
  - type => It can be string or class
    - string => Tag name
    - class or function name => Custom Component
  - props
  Example 1
  ```
    {
      type: 'b',
      props: {
        children: 'Hello World'
      }
    }

    <b>Hello World</b>
  ```
  Example 2
  ```
    {
      type: 'div',
      props: {
        children: [
          {
            type: 'b',
            props: {
              children: 'Hello World'
            }
          },
          {
            type: 'input',
            props: {
              type: 'text'
            }
          }
        ]
      }
    }

    <div>
      <b>Hello World</b>
      <input type='text'>
    </div>
  ```

  Example 3
  ```
    {
      type: Button
      props: {
        color: 'success'
        children: 'Submit'
      }
    }

    <Button color="success">Submit</Button>
  ```
- Reconcillation
  - if type changes, then entire tree is removed and built from scratch
  - if attributes change for DOM elements of same type, then only props gets 
  - if props change for Component elements of same type, props changes for underlying instance
  - if an item is prepended to list its costlier than appending to list. In order to resolve this, keys are introduced. When children have keys, react use them to do the matching
    - Key should be stable, predicatable and unique
    - Keys with indexes tends to create issues while reordering, filtering  because if index is changed, key also changed and we can not benefit from React diffing algorithm as it will not optimize the render