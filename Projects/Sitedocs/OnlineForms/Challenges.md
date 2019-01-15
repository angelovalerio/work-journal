#### Challenges

- Restructuring of state Forms and Template reducers:
  - Main Issues
    - Forms and Template states were combined in single object though they were not related
    - state object was too complex.
        - Usually its a practise to keep reducer per primitive value but with such an expanded structure the number of files will too much, so its better to combine primitives related to one action set into in an object and update that state in a single reducer file.
        - Earlier structure
          ```
            {
              forms:{
                loading,
                template {
                  list,
                  loading,
                  images,
                  signatures
                  ...dataFromApi
                }
                list,
              }
            }
          ```

          New Structure
          ```
            {
              forms:{
                loading,
                list,
                error
              }
              template {
                list {
                  [id] {
                    loading,
                    error,
                    data
                  }
                }
                images,
                signature {
                  isSignatureModalVisible,
                  list {
                    loading,
                    error,
                    data
                  }
                },
                UI {
                  loading,
                  error,
                  details: {
                    ...dataFromApi
                  }
                },
                submitRequest {
                  loading,
                  error,
                  success
                }
              }
            }
          ```
          Each object with its on reducer