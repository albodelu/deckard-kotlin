# Deckard
[![Build Status](https://travis-ci.org/seadowg/deckard-kotlin.svg?branch=master)](https://travis-ci.org/seadowg/deckard-kotlin)

Deckard is the simplest possible Android application project that uses Robolectric for testing and Gradle to build. It has one Activity and a single Robolectric test of that Activity.

Deckard imports easily into the latest editions of Android Studio with minimal setup.

## Setup

*Note: These instructions assume you have a Java 1.8 [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed.*

To start a new Android project:

1. Install [Android Studio 1.5.1](http://developer.android.com/sdk/index.html).
2. Run the [Android SDK Manager](http://developer.android.com/tools/help/sdk-manager.html) and install `API 23`, `Build-tools 23.0.2` and the support library. You can also install the packages from the terminal, using [android](https://developer.android.com/tools/help/android.html) from your `sdk/tools/` directory:
```bash
android update sdk --all --no-ui --filter build-tools-23.0.2 && \
android update sdk --all --no-ui --filter android-23 && \
android update sdk --all --no-ui --filter extra-android-support && \
android update sdk --all --no-ui --filter extra-android-m2repository
```
3. Download Deckard from GitHub:
```bash
wget https://github.com/seadowg/deckard-kotlin/archive/master.zip
unzip master.zip
mv deckard-kotlin-master my-new-project
```
4. Create a `local.properties` [file](http://tools.android.com/tech-docs/new-build-system/user-guide#TOC-Simple-build-files) in the root of the project that points to
5. In the project directory you should be able to run the Robolectric tests:
```bash
./gradlew clean test
```
6. Change the names of things from 'Deckard' to whatever is appropriate for your project. Package name, classes, build.gradle, and the AndroidManifest are good places to start.
7. Build an app. Win.

## Android Studio Support

### Compatibility
Deckard is designed to run against Android Studio 1.5.1 with [Unit Testing support](https://sites.google.com/a/android.com/tools/tech-docs/unit-testing-support) enabled in Studio's Gradle settings.

### Importing
Import the project into Android Studio by selecting 'Import Project' and selecting the project's `build.gradle`. When prompted, you can just pick the default gradle wrapper.

### Running the Robolectric Test
To run Robolectric tests (example can be found in `DeckardActivityTest`) open Studio's
"Build Variants" pane and change the "Test Artifact" to "Unit Tests". You can then run
Robolectric tests using the JUnit test runner.
