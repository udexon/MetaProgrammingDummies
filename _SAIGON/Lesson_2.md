### Lesson 2: Adding Code to Button

[ Table of Contents ](https://github.com/udexon/MetaProgrammingDummies/blob/master/_SAIGON/0_Table_of_Contents.md)

In the [previous lesson](https://github.com/udexon/MetaProgrammingDummies/blob/master/_SAIGON/README.md), we learned how to add a button to an Android app without coding.

In this lesson, we will learn how to add code to the new button. However, we will not do much. We will simply duplicate the function of the first button and attach it to the new button.

The code concerned is in [this file](https://github.com/udexon/MetaProgrammingDummies/blob/master/app/src/main/java/com/example/parsaniahardik/kotlinselectimagegallery/MainActivity.kt). The lines concerned are:

```
33        btn = findViewById<View>(R.id.btn) as Button
34        imageview = findViewById<View>(R.id.iv) as ImageView
35
36        btn!!.setOnClickListener { showPictureDialog() }
```
