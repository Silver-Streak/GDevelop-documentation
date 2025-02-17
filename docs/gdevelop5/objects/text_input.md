---
title: Text Input
---
# Text Input

A Text Input displays a field where the player can enter some text. This can be used for example to ask for the player name, get their email, create a search bar, enter a password, etc...

Text Inputs can be customised and are using the native platform user interface to be rendered on top of the game. According to the platform, small variations can happen in the rendering of the field. On touch devices (Android, iOS), a keyboard will be shown on screen, reducing the size available for the game. The player can use the keyboard as usual (as well as select the text, copy, paste, insert emojis, as in any other app).

![](/gdevelop5/objects/text_input/pasted/20220310-005743.png)

## Note about the rendering of this object

!!! warning

    Read this part carefully to understand the limitations of the object.

Because the object is not rendered by the same hardware accelerated renderer as the rest of the game, the object has some limitations. It is rendered on top of the game using the user interface toolkit of the platform the game is running on (the browser, itself using the operating system of the device).

This means:

- You can't change the **Z order** of the object.
- You can't use **effects** with the object.
- Be careful if you use the object in a scene with a moving camera or if you rotate/move the object. It might be slightly desynchronised from the rest of the rendered game. This can create a weird effect for the player.

In general, prefer to use the object on **a static screen** and ensure the keyboard on mobile devices won't hide critical information.

## Input type

The field can be:

* A **single line** text input (default)
* A **multiline** text input (also called a "text area")
* Or a special single line text input: *password, email, search field, number, phone number, url*. 

According to the type, some devices might display visual helps or **a different keyboard** to the user (especially on mobile). Password inputs will also hide the character that the user is writing.

## Reading the text entered by the player

After adding a Text Input object, put an instance on the scene. You can then use the expression `Text` on the object in the events to read the text. For example, this event copies the content of the field into a [Text object](/gdevelop5/objects/text) (to display it somewhere else on the screen):
![](/gdevelop5/objects/text_input/pasted/20220310-010309.png) 

## Read-only and disabled fields

You can set, either from the object properties or using actions, the field as :

* Read-only. Text can still be selected and usually the appearance of the field does not change, but the text can't be modified.
* Disabled. Text can't usually be selected, nor modified, and some devices or platforms will gray the input.
