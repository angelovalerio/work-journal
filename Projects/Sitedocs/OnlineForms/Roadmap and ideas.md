#### Fundamentals

- Current Situation
  - Minimal state
    - Bad `<Template />` Component
    - `<Annotator />` state
      ```
        class Annotator extends Component {
          state = {
            width: 400,
            height: 400,
            ctx: null,
            tile: null,
            imageEditor: null
          }```
  - Extracting state to upper level rather than passing it to and fro.
    - Bad Example => Passing value from `Modal.js` to `MultiSelect.js` to `Select.js` and maintaining it in state for all of them
  - Why we have `whiteTheme` and `darkTheme`
  - Currently MaterialUI is completely scattered. WMay be we can do something around this
  - Is it possible to go `No Component State` mode. Its easier with redux
  - Also perhaps we have complicated our states. May be can simplify by breaking it in separate files
  - Can we collect typography of application at one place? Let's assume we get a reqyuest to change the color code for application. Can we change it from one single place rather than editing 50 different file
  - Use confluence for roadmap
    - Tests
    - Architecture Improvements
      - State Refactoring and Architecture
    - Update libraries
    - Design Improvements
      - Typography
      - design Palette
    - Optimizations to increase speed - YSLOW, google audits
    - FB Bots
    - Server Side Rendering
    - Do we need to have ability to open web pages on mobile
    - GraphQL
    - TypeCheck
    - Tree shaking, Code splitting



- Future
  - Bi-Weekly discuss over call, what we can do to improve code and developer experience
  - 