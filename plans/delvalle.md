## Status

* I have my development environment up and have worked through the sample test cases.


## Goals

* Get more comfortable writing test cases.

* Attempt to implement the feature of automatically unlocking the device screen as soon as the device turns on, or at any time for that matter, as discussed in https://github.com/selendroid/selendroid/issues/752.


## Plan

1. See if there is a way to call 'adb shell keyevent 82' from selendroid (this android command unlocks the screen).
1. If not, look into how Appium unlocks the device screen
1. Implement something similar
1. Verify that the solution works with different Android versions.
1. I am then going to share my code with Luke for feedback.
1. Submit pull request if all goes well.
