##Issues and Ideas

#### *Issue* Console.logs was not happening
**Reason =>** In setupTests.js, global.console. was set to jest.fn(), commenting that fixed it.

#### Alert Feature - Using Material UI Snackbars with redux (without notistack)
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