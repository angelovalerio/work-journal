## Issues, Ideas and Tasks


- #### Scroll to first error message
  - Current Scenario => Form validation occurs in Template and error is displayed in ItemWrapper
  ```
    <Template>
      <Section>
        <ItemWrapper>
        </ItemWrapper>
        <ItemWrapper>
          <p className="error">Error</p>
        </ItemWrapper>
      </Section>
      <Section>
        <ItemWrapper>
          <p className="error">Error</p>
        </ItemWrapper>
      </Section>
    </Template>
  ```
  - Requirement
    - [ ] Find first error message and scroll to it's item wrapper
    - [ ] If possible use cleaner way of using ref and forwardRef
  - Solution
    - Create `ref` in `<Template />`
    - Save first error section id and item id 
    - pass `ref` and first error section id and item id to Section
    - if any `<ItemWrapper />` in `<Section />` matches given error section id and item id, then pass ref to it
    - Set ref to first `<div />` in `<ItemWrapper />`
    - On form validation in `<Template />`, after setting state, call `scrollIntoView` on the ref


- #### Webforms Phase (Accepted Stories)
  - [x] [Update V2 API to be able to Load DocumentTemplates by locationId](https://www.pivotaltracker.com/story/show/160000160)
    - [ ] Not working as expected => Forms that have visibility of 2 locations only, is visible on other locations as well. Example `New Form For Report`. 
    - [x] Post on #dev-stuff to sameer
  - [x] [Publish a dev version of html fill forms](https://www.pivotaltracker.com/story/show/159895120)
  - [x] [Set up V1 to Allow CORS](https://www.pivotaltracker.com/story/show/160268031)
      Not sure if it works on other domains or not
  - [x] [Update V2 API to be able to load List items](https://www.pivotaltracker.com/story/show/160587976)
  - [x] [User can login and see a list of forms they can sign](https://www.pivotaltracker.com/story/show/159023665)
  - [x] [User can filter forms to sign by](https://www.pivotaltracker.com/story/show/159023672)
      Searching by folder name is not available
  - [x] [Web Forms - show pdf in modal with zoom functionality](https://www.pivotaltracker.com/story/show/161484930)
  - [x] [User can upload photos on submissions](https://www.pivotaltracker.com/story/show/159023492)
  - [x] [User can annotate photos](https://www.pivotaltracker.com/story/show/159023495) => Duplicate (161931165)
  - [ ] [Web Forms - form items CSS tweaks](https://www.pivotaltracker.com/story/show/161299881),
[Web Forms - select modal CSS tweaks](https://www.pivotaltracker.com/story/show/161446295),
[Web Forms - select multiple form item CSS tweaks](https://www.pivotaltracker.com/story/show/161299944),
[Web Forms - change GPS form item](https://www.pivotaltracker.com/story/show/161586593)
    - [ ] Select ones are showing checkboxes. It is confusing. It should be radio buttons
    - [ ] Change button to ‘Done’  with background color - #42AF48 and text color #ffffff => its different
    - [ ] Invert button colors on the form and remove margin-top so it’s tighter to question
    - [ ] View on Map ==> Show on Map
    - [ ] Angelo will discuss with Tom and will come back with answers
  - [ ] [User can fill in all form item types online](https://www.pivotaltracker.com/story/show/158811777)
    - [ ] Short answer has multiline
    - [ ] Select Single => Why Checkbox
    - [ ] Date => No year
    - [ ] Image File => Failed to load PDF file 
  - [x] [User can add photos to form items (as per app)](https://www.pivotaltracker.com/story/show/159023660) => As per app details
  - [x] [User can add comments to form items (as per app)](https://www.pivotaltracker.com/story/show/159023571) => As per app details
  - [x] [User can duplicate sections](https://www.pivotaltracker.com/story/show/159427709)
  - [x] [User can sign and submit a new form](https://www.pivotaltracker.com/story/show/159023667)
  - [x] [Web Forms - select workers form item using the select multiple modal](https://www.pivotaltracker.com/story/show/161446211)
    - [x] How is location filtered by company
  - [ ] [web forms form data is validated ](https://www.pivotaltracker.com/story/show/161168646) 
    - [ ] Create documentation of list of validations
    - [ ] What are the validations added?
  - [ ] [User can switch location](https://www.pivotaltracker.com/story/show/162652495)
    - [ ] Not Working - Send the User to the Form List page when they switch Locations.
    - [ ] Not Working - If a worker switches a location ‘mid-form’ the location for that form is updated while preserving the data.
  - [x] [webforms should show a message for the user using snackbars](https://www.pivotaltracker.com/story/show/162645763)
  - [x] [web forms allows you to see what user you're logged in as](https://www.pivotaltracker.com/story/show/162643422)
  - [x] [Latest value for the pass fail counter is not uploaded with the signed form.](https://www.pivotaltracker.com/story/show/162719339)
  - [ ] Remove all console logs

- #### Webforms Phase 4 (Accepted Stories)
  - [x] [Annotations on Photos](https://www.pivotaltracker.com/story/show/161931165)
  - [x] [Comments on Photos](https://www.pivotaltracker.com/story/show/161931099)
  - [x] [Deleting a Photo](https://www.pivotaltracker.com/story/show/161931313)
  - [x] [Adding Multiple Photos](https://www.pivotaltracker.com/story/show/161931387)

- #### *Issue* Console.logs was not happening
  *Reason =>* In setupTests.js, global.console. was set to jest.fn(), commenting that fixed it.

- #### Alert Feature - Using Material UI Snackbars with redux (without notistack)
  - One item exists and second one comes
    - Actions
      - ADD_MESSAGE_TO_QUEUE => adds message to queue
      - HIDE_CURRENT_MESSAGE => set is open to false and removes first message from queue
      - SHOW_CURRENT_MESSAGE => pulls first message in queue and set isOpen to true.
    - When to call these actions (Example)
      - On signature submit success, ADD_MESSAGE_TO_QUEUE, SHOW_CURRENT_MESSAGE
      - On form submit success, ADD_MESSAGE_TO_QUEUE, HIDE_CURRENT_MESSAGE, 
      - Auto hide after 6 secs, HIDE_CURRENT_MESSAGE
      - On Exit of last message, SHOW_CURRENT_MESSAGE

