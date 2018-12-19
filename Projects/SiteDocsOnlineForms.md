##Issues, Ideas and Tasks


#### Webforms Phase (Accepted Stories)

- [] [Update V2 API to be able to Load DocumentTemplates by locationId](https://www.pivotaltracker.com/story/show/160000160)
Not working as expected => Forms that have visibility of 2 locations only, is visible on other locations as well. Example `New Form For Report`
- [x] [Publish a dev version of html fill forms](https://www.pivotaltracker.com/story/show/159895120)
- [] [Set up V1 to Allow CORS](https://www.pivotaltracker.com/story/show/160268031)
Not sure if it works on other domains or not
- [x] [Update V2 API to be able to load List items](https://www.pivotaltracker.com/story/show/160587976)
- [x] [User can login and see a list of forms they can sign](https://www.pivotaltracker.com/story/show/159023665)
- [] [User can filter forms to sign by => Searching by folder name is not available](https://www.pivotaltracker.com/story/show/159023672)
Searching by folder name is not available
- [x] [Web Forms - show pdf in modal with zoom functionality](https://www.pivotaltracker.com/story/show/161484930)
- [x] [User can upload photos on submissions](https://www.pivotaltracker.com/story/show/159023492)
- [x] [User can annotate photos](https://www.pivotaltracker.com/story/show/159023495) => Duplicate (161931165)
- [] [Web Forms - form items CSS tweaks](https://www.pivotaltracker.com/story/show/161299881),
[Web Forms - select modal CSS tweaks](https://www.pivotaltracker.com/story/show/161446295),
[Web Forms - select multiple form item CSS tweaks](https://www.pivotaltracker.com/story/show/161299944),
[Web Forms - change GPS form item](https://www.pivotaltracker.com/story/show/161586593) 
-- [] Select ones are showing checkboxes. It is confusing. It should be radio buttons
-- [] Change button to ‘Done’  with background color - #42AF48 and text color #ffffff => its different
-- [] Invert button colors on the form and remove margin-top so it’s tighter to question
-- [] View on Map ==> Show on Map
- [x] [Annotations on Photos](https://www.pivotaltracker.com/story/show/161931165)
- [] [](https://www.pivotaltracker.com/story/show/)

#### *Issue* Console.logs was not happening

**Reason =>** In setupTests.js, global.console. was set to jest.fn(), commenting that fixed it.

#### Alert Feature - Using Material UI Snackbars with redux (without notistack)

- One item exists and second one comes
-- Actions
--- ADD_MESSAGE_TO_QUEUE => adds message to queue
--- HIDE_CURRENT_MESSAGE => set is open to false and removes first message from queue
--- SHOW_CURRENT_MESSAGE => pulls first message in queue and set isOpen to true.
-- When to call these actions (Example)
--- On signature submit success, ADD_MESSAGE_TO_QUEUE, SHOW_CURRENT_MESSAGE
--- On form submit success, ADD_MESSAGE_TO_QUEUE, HIDE_CURRENT_MESSAGE, 
--- Auto hide after 6 secs, HIDE_CURRENT_MESSAGE
--- On Exit of last message, SHOW_CURRENT_MESSAGE

