# Ava-Virtual-Entity

Ava is an Online Virtual Entity I'm building using Node.js and the Following Javascript Bot Ui

BotUI
Join the chat at https://gitter.im/BotUIChat/botui npm npm newsletter

A JavaScript framework to create conversational UIs.

Main Site - Read Docs - Examples

Showcase 🎇✨
We are listing all the cool projects that people are building with BotUI, here. See others' and add yours!

Quick look
preview

<div class="botui-app-container" id="botui-app">
  <bot-ui></bot-ui>
</div>
var botui = new BotUI('botui-app'); // give it the id of container

botui.message.bot({ // show first message
  delay: 200,
  content: 'hello'
}).then(function () {
  return botui.message.bot({ // second one
    delay: 1000, // wait 1 sec.
    content: 'how are you?'
  });
}).then(function () {
  return botui.action.button({ // let user do something
    delay: 1000,
    action: [
      {
        text: 'Good',
        value: 'good'
      },
      {
        text: 'Really Good',
        value: 'really_good'
      }
    ]
  });
}).then(function (res) {
  return botui.message.bot({
    delay: 1000,
    content: 'You are feeling ' + res.text + '!'
  });
});
License
MIT License - Copyrights (c) 2017 - Moin Uddin
