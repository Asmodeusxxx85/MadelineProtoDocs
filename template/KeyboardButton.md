Clicking these buttons:

To click these buttons simply run the `click` method:  

```php
$result = $%s->click();
```

`$result` can be one of the following:


* A string - If the button is a keyboardButtonUrl

* [Updates](Updates.html) - If the button is a keyboardButton, the message will be sent to the chat, in reply to the message with the keyboard

* [messages.BotCallbackAnswer](messages.BotCallbackAnswer.html) - If the button is a keyboardButtonCallback or a keyboardButtonGame the button will be pressed and the result will be returned

* `false` - If the button is an unsupported button, like keyboardButtonRequestPhone, keyboardButtonRequestGeoLocation, keyboardButtonSwitchInlinekeyboardButtonBuy; you will have to parse data from these buttons manually


You can also access the properties of the constructor as a normal array, for example `$button['name']`
