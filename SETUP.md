These are my personal notes on how I got the projects setup and working on my Mac OS 10.9.5 laptop.

### Global Settings

1. Install Java 1.7 SDK [Java SE 7u75/76](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
1. Install [IntelliJ 14 Community Edition](https://www.jetbrains.com/idea/download/)
1. Install [Homebrew](http://brew.sh/) `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
1. Install Maven: `brew install maven`

### Running IntelliJ

The instructions below will say **Run IntelliJ**.  When running it for the first time:

1. Choose: I do not have a previous version of IntelliJ IDEA or I do not want to import my settings
1. Check out from Version Control > Github
1. enter github username/password > Login
1. setup master password > OK

If you have already used IntelliJ for another project:

1. VCS > Checkout from Version Control > Github

### Setup JDK

Make sure the project has JDK 1.7 configured by navigating through:

1. File > Project Structure... > Project
1. Select JDK 1.7.  If there is no JDK
    1. New... > JDK
    1. Macintosh HD > Library > Java > JavaVirtualMachines > jdk1.7.0_75.jdk > Choose
1. Project language level: 7

### iOS-Driver Setup

1. Install [Xcode](https://developer.apple.com/xcode/)
1. Go to https://github.com/ios-driver/ios-driver and [Fork](https://github.com/ios-driver/ios-driver/fork) it
1. [Run IntelliJ](#running-intellij)
1. choose my ios-driver fork from the dropdown list:  `https://github.com/mmccartney/ios-driver.git`
1. Clone (*note that this is creating* `~/IdeaProjects/ios-driver`)
1. Would you like to open it? > Yes
1. [Setup JDK](#setup-jdk)
1. View > Tool Windows > Project
1. In a terminal window
    1. `cd ~/IdeaProjects/ios-driver/`
    1. `git submodule init`
    1. `git submodule update`
    1. `export JAVA_HOME=$(/usr/libexec/java_home -v 1.7+)`
    1. `export MAVEN_OPTS="-Xss10m -Xms512m -Xmx512m"`
    1. `mvn package -DskipTests=true`
    1. `java -jar server/target/ios-server-standalone-*-with-dependencies.jar`
1. See server status at http://localhost:5555/wd/hub/status
1. Run the server to test the sample app:
    1. `curl -O http://ios-driver.github.io/ios-driver/files/InternationalMountains.app.zip`
    1. `unzip InternationalMountains.app.zip`
    1. `java -jar server/target/ios-server-standalone-*-with-dependencies.jar -app InternationalMountains.app`

### Selendroid Setup

*These instructions are missing the setup of the AVD -- the wrong one breaks the test*

1. Go to https://github.com/selendroid/selendroid and [Fork](https://github.com/selendroid/selendroid/fork) it
1. Install [Android Studio](http://developer.android.com/sdk/index.html)
    * This has the side effect of installing the Android SDK in `~/Library/Android/sdk`
1. [Run IntelliJ](#running-intellij)
1. choose my selendroid fork from the dropdown list:  `https://github.com/mmccartney/selendroid.git`
1. Clone (*note that this is creating* `~/IdeaProjects/selendroid`)
1. Would you like to open it? > Yes
1. [Setup JDK](#setup-jdk)
1. View > Tool Windows > Project
1. In a terminal window
    1. `cd ~/IdeaProjects/selendroid/`
    1. `export JAVA_HOME=$(/usr/libexec/java_home -v 1.7+)`
    1. `export MAVEN_OPTS="-Xss10m -Xms512m -Xmx512m"`
    1. `export ANDROID_HOME=~/Library/Android/sdk`
    1. `export PATH=$ANDROID_HOME/tools:$ANDROID_HOME/platform-tools:$PATH`
    1. `android update sdk --no-ui --obsolete --force`
    1. `(cd third-party/cordova-3.7.0 && ./mvnInstall.sh)`
    1. `mvn package`
    1. `java -jar selendroid-standalone/target/selendroid-standalone-*-with-dependencies.jar`
1. See server status at http://localhost:4444/wd/hub/status
1. Run the server to test the sample app:
    1. `java -jar selendroid-standalone/target/selendroid-standalone-*-with-dependencies.jar -app selendroid-test-app/target/selendroid-test-app-*.apk`

### Setup Adium for IRC

1. Download, Install, and Run [Adium](https://adium.im/)
1. Decline to import contacts
1. Continue
1. Service: IRC (Internet Relay Chat)
1. Create a nickname
1. Continue
1. specify the IRC server: `chat.freenode.net`
1. File > Join Group Chat... > `#selendroid`
1. File > Join Group Chat... > `#ios-driver`

