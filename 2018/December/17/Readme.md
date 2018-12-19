**2nd Week at SiteDocs :) and first day of Journal inspired by Jermiah(colleague)**

## Personal Website
#### Target
- [] Complete Portfolio Section
-- [X] Create Template for item
-- [] Create all items

#### LeftOvers
- About me
-- Talk about experience skills and projects one para each
-- Mention recommendations
- Blog Post
-- Fix Headers
-- Remove Header Image
- Universal Typography and colors for website
- Work with me section
-- What services you want to provide
-- Write about them

### Things happend
- Created template for portfolio item. 
-- Image at one side and description, resposnsibilities, tech stack and View Project button on the other side. Carousel below.
-- Techstack items have custom css
```HTML
  <div class="tech-stack">
    <ul class="list">
      <li class="list-item">ReactJS</li>
      <li class="list-item">HTML5</li>
      <li class="list-item">CSS3</li>
    </ul>
  </div>
```
- Found settings for default colors, typography


## SiteDocs Web Forms

- Continued writing tests for Alert feature
-- **Issue =>** Console.logs was not happening
   **Reason =>** In setupTests.js, global.console. was set to jest.fn(), commenting that fixed it.

- Alert Feature
-- One item exists and second one comes
--- Actions
---- ADD_MESSAGE_TO_QUEUE => adds message to queue
---- HIDE_CURRENT_MESSAGE => set is open to false and removes first message from queue
---- SHOW_CURRENT_MESSAGE => pulls first message in queue and set isOpen to true.
--- When to call these actions (Example)
---- On signature submit success, ADD_MESSAGE_TO_QUEUE, SHOW_CURRENT_MESSAGE
---- On form submit success, ADD_MESSAGE_TO_QUEUE, HIDE_CURRENT_MESSAGE, 
---- Auto hide after 6 secs, HIDE_CURRENT_MESSAGE
---- On Exit of last message, SHOW_CURRENT_MESSAGE
