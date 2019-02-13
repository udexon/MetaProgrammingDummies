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

Two new lines of code are inserted at line 34 and line 39:

```
33        btn = findViewById<View>(R.id.btn) as Button
34        btn1 = findViewById<View>(R.id.btn1) as Button
35
36        imageview = findViewById<View>(R.id.iv) as ImageView
37
38        btn!!.setOnClickListener { showPictureDialog() }
39        btn1!!.setOnClickListener { showPictureDialog() }
```

The new `MainActivity.kt` is available [here](https://github.com/udexon/MetaProgrammingDummies/blob/master/_SAIGON/MainActivity.kt).

You can now replace the old `MainActivity.kt` with the new one and rebuild your APK.

As you can see, the example given above is still manageable manually. But I hope you are convinced that the effort will become more complicated and tedius as we proceed. In fact, our plan is the merge the above with the [OpenCV Kotlin Starter project](https://github.com/ramonrabello/OpenCV-Kotlin-Starter). I will leave it to the readers to explore it and I am sure by now you already have an idea of the tedium and complications involved in Android app development.

Fear not! SAIGON Metaprogramming is invented to solve this exact problem!
