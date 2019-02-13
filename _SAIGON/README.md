### SAIGON Metaprogramming for Dummies

Hardik Parsania made an excellent tutorial for [selecting image from gallery](https://demonuts.com/pick-image-gallery-camera-android/) on Android phone with a Kotlin app, which we cloned [here](https://github.com/udexon/MetaProgrammingDummies).

We demonstrate to how to add a button to Parsania's original app, without involving any coding, to illustrates some basic principles of SAIGON Metaprogramming. For more information about the [SAIGON project](https://github.com/udexon/SAIGON) itself, please click [here](https://github.com/udexon/SAIGON). 


| Before        | After           | 
| ------------- |:-------------:| 
| <img src="https://github.com/udexon/MetaProgrammingDummies/blob/master/_SAIGON/Screenshot_2019-02-13-11-25-28-31.png" width="200"> | <img src="https://github.com/udexon/MetaProgrammingDummies/blob/master/_SAIGON/Screenshot_2019-02-13-11-13-30-16.png" width="200"> | 

You might be wondering what significance there is compared to literally thousands of Android programming tutorial out there. 

The full answer is a complicated one. A short answer would be:

- We need a simpler way of developing app -- so simple that *EVERYONE* can code.

Now you be wondering, how is that possible? Read on ...

We will leave the lengthy discussions to the end. We will just show now how the change is done:

1. The original `layout/activity_main.xml` file is [here](https://github.com/udexon/MetaProgrammingDummies/blob/master/app/src/main/res/layout/activity_main.xml).

2. Add the following text to `layout/activity_main.xml`:

```
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btn1"
        android:layout_gravity="center_horizontal"
        android:layout_marginTop="40dp"
        android:textAppearance="?android:attr/textAppearanceLarge"
        android:text="Select or Capture Image 20190213" />
```

3. You can download the new `layout/activity_main.xml` [here](https://github.com/udexon/MetaProgrammingDummies/blob/master/_SAIGON/activity_main.xml). Just replace the old file with the new one. Rebuild your APK in Android Studio (or your preferred methods). 

So what are the novelties behind such a trivial change?

1. There might have been new Android app development tools aimed at making it easier to develop Android apps. However, these tools never expose the fundamentals thus making it troublesome for beginners to progress, plus there would have been planty of restrictions imposed by the simplified platforms. (e.g. Kivy Python for Android)

The philosophy of SAIGON Metaprogramming is such that we do not change the fundamental mechanisms of how to make an Android app, but make them easier to understand and easier to use by "creating a program to modify other programs" (metaprogramming). This approach has the following advantages:

- It uses the fundamental mechanisms of app development as they are, thus imposing no restrictions.
- It makes it easy for beginners to understand and use the existing app development infrastructure.
- It is platform independent. The example shown here is for Android Kotlin. But it can be easily portable to other platforms, including iOS, Mac Xcode, JavaScript, PHP, Web applications, GNOME Desktop app, Python etc. 

The reason SAIGON is platform independent is because it deals with the most fundamental level in software development and programming: the text files of source code and configuration files themselves. This may sound too abstract for beginners and even some experienced programmers. However, in this post-iPhone-X era, progress in software engineering has all but stagnated. A beginner will find nothing new to learn after 6 months. 

Metaprogramming -- to write a program to modify another program -- is perhaps the only untouched and unexplored area in programming and software engineering, due to a series of complex reasons which we will explain eventually.

Back to the Kotlin Android image selection app above, the Kotlin Android development platform could have taken a more "visual" approach, i.e. to organize the files according to the visual output, and let programmers work on the source files accordingly. However, this was not the case as Kotlin Android is very much a "patch up" work based on Android Java, the initial app development platform for Android, which was designed with other priorities in mind. This is how SAIGON Metaprogramming can bypass whatever design assumptions the tools designers have, and create a brand new, users and visual oriented development approach.

For the button adding example above, the amount work to edit the file is negligible. So we probably do not need any tool (a program) to help us do that. But the complexity of Android app or any app in 2019 will spiral out of control very quickly. Nonetheless, the example above illustrates some fundamental issues concerning Android app development and metaprogramming.

This seems like a good point to conclude this article, as we look forward to the next.
