https://github.com/MunGell/awesome-for-beginners#javascript

### Libraries I use
- React
- React Router
- Redux
- Webpack
- Babel
- Ramda
- ESlint
- Jest
- MaterialUI

### Ideas to start with
  - Feature add to Ramda 
    - ArrayToObj => already exists `indexBy`
    - Cases
      - CamelCase
      - pascalCase
      - dash-case / kebab
      - Dash-Upper-Case / train
      - snake_case
      - Snake_Upper_Case
    - camel case <=> pascal case
    - split string word with hyphen
    - string with hyphen to camel case
    - string with hyphen to pascal case
  - Go through React code deeply and then try to see how can you contribute

### Ramda
- ToDo
  - [ ] Create Feature Request and discuss
  - [ ] Code
  - [ ] Submit PR
- Feature request => any string to CamelCase
  ```
    toCamel
    yashika => Yashika
    yashikagarg => YashikaGarg

    input =>
      string,
      index
  ```

  or idea could be to create a transform function that takes, string, arrayOfIndexes, and tranformation to apply on string at those index example

  R.toCamel('yashikagarg', [7]) => YashikaGarg
  R.toCamel('yashika-garg') => YashikaGarg
  R.toCamel(yashika_garg) => YashikaGarg



  R.toPascal('yashikagarg', [7]) => yashikaGarg
  R.toKebab('yashikagarg', [7]) => yashika-garg
  R.toTrain('yashikagarg', [7]) => Yashika-Garg
  R.toSnake('yashikagarg', [7]) => yashika_garg
  R.toSnakeUpper('yashikagarg', [7]) => Yashika_Garg