# Material Dialog v1.2.2

This is an Android library, I call it MaterialDialog. It's very easy to use. 
Just `new` it & call `show()` method, then the beautiful AlertDialog will show automatically. It is artistic, conforms to Google Material Design. I hope that you will like it, and enjoys it. ^ ^

## Screenshots

<img src="/screenshots/s1.png" alt="screenshot" title="screenshot" width="270" height="486" /><img src="/screenshots/s2.png" alt="screenshot" title="screenshot" width="270" height="486" />
<img src="/screenshots/s3.png" alt="screenshot" title="screenshot" width="270" height="486" /><img src="/screenshots/s4.png" alt="screenshot" title="screenshot" width="270" height="486" />

You can also change the background with a image what you like. it's very easy!:

<img src="/screenshots/s5.png" alt="screenshot" title="screenshot" width="270" height="486" /><img src="/screenshots/s6.png" alt="screenshot" title="screenshot" width="270" height="486" />

And with the v1.0.6, you can use the `setContentView()` to change the `message view` to your custom view.

Example:

<img src="/screenshots/s7.png" alt="setContentView" title="setContentView" width="270" height="486" /><img src="/screenshots/s8.jpg" alt="setContentView" title="setContentView" width="270" height="486" />
## Usage
### Step 1
####Gradle

```groovy
dependencies {
    compile 'me.drakeet.materialdialog:library:1.2.8'
    // I have uploaded v1.2.8 on 2015-11-22, if it doesn't take effect or your 
    // gradle cannot find it in maven central, you may try v1.2.2.
}
```

If it doesn't work, please send me a email, drakeet.me@gmail.com

####Or

Import the library, then add it to your `/settings.gradle` and `/app/build.gradle`, if you don't know how to do it, you can read my blog for help.

[Android Studio 简介及导入 jar 包和第三方开源库方法](http://drakeet.me/android-studio)

### Step 2

It's very easy, just like this:

```java
MaterialDialog mMaterialDialog = new MaterialDialog(this)
    .setTitle("MaterialDialog")
    .setMessage("Hello world!")
    .setPositiveButton("OK", new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            mMaterialDialog.dismiss();
            ...
        }
    })
    .setNegativeButton("CANCEL", new View.OnClickListener() {
        @Override
        public void onClick(View v) {
            mMaterialDialog.dismiss();
            ...
        }
    });

mMaterialDialog.show();

// You can change the message anytime. before show
mMaterialDialog.setTitle("提示");
mMaterialDialog.show();
// You can change the message anytime. after show
mMaterialDialog.setMessage("你好，世界~");
```
With the first initial and `mMaterialDialog.show()`, it will show automatically.

In addition, you can call `setView (View v) ` & `setContentView()` to set a View what you like or
custom after the instantiation. This replaces the title and message.
```java
EditText contentView = new EditText(this);
MaterialDialog mMaterialDialog = new MaterialDialog(this).setView(contentView);

mMaterialDialog.show();
```


## 1.2.8
* Fix the problem of soft keyboard repeat display
* Fix the action buttons became dismiss when scroll view height is too long.
* Add get buttons so that you can custom them.
* Update the versions of gradle and some build tools.

## 1.2.1
* Now, It has been able to run perfectly on L.
* Fix the button style on L.
* Fix the problem, so that it can correctly use `AutoCompleteTextView` & `EditText`.

## 1.1.0
* Fix the keyboard/input bug when more show. 

## 1.0.9
* If title is null, no show it, but I think it is ugly without title...;
* Add set Button's text by string resId, e.g. `setPositiveButton(android.R.string.yes, new View.OnClickListener() `

## 1.0.8
* Add every method return `this`

## 1.0.7
* Fix the BUG of `Can not show soft keyboard automatically when focus is on an EditText.`
* Add `setCanceledOnTouchOutside()` // You should set it before `show()`, otherwise, it can't take effect.
* Add `setContentView()`
* Add Button press style;
* ...

I recently was too busy, if you have any Suggestions for the library, I encourage you to read the source code, and try to achieve your requirements, and then I'll merger it. We create good world together.

## BUG

## DEMO

[demo apk v1.2.8](/demo-debug.apk)

============

    Copyright 2014 drakeet

	Licensed under the Apache License, Version 2.0 (the "License");
	you may not use this file except in compliance with the License.
	You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.

