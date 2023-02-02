# 1. Introduction

This book(note->book) is all about **[lomorage](https://lomorage.com)** android app developer notes while developing the App.

And the developer record everything when he start to develop the lomorage since he has no experience on Android development.

Via this notes, you can learn a lots esp. on how to start android app development from scratch.

But everything on this book is just my notes, so I name this book:

 **"My Android App development notes with Kotlin"**

Enjoy the reading.

**You can search the content via the left-top search box.**

~aisnote at gmail dot com.


**Reference：**
1. [gitbook config](https://www.mapull.com/gitbook/comscore/others/book.html)
2. cmd:
   > gitbook install

   > ./run.sh

3. My Windows Dev Env:
   
```Shell
    $ node --version
    v18.13.0

    $ npm --version
    8.19.3
```

4. If you meet gitbook polyfill issue on **graceful-fs**, please comments out as below:

```JavaScript
    c:\Users\Elliot\AppData\Roaming\npm\node_modules\gitbook-cli\node_modules\npm\node_modules\graceful-fs\polyfills.js

    fs.chmodSync = chmodFixSync(fs.chmodSync)
    fs.fchmodSync = chmodFixSync(fs.fchmodSync)
    fs.lchmodSync = chmodFixSync(fs.lchmodSync)

    //fs.stat = statFix(fs.stat)
    //fs.fstat = statFix(fs.fstat)
    //fs.lstat = statFix(fs.lstat)

    fs.statSync = statFixSync(fs.statSync)
    fs.fstatSync = statFixSync(fs.fstatSync)
    fs.lstatSync = statFixSync(fs.lstatSync)
```