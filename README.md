# Run Android Testify Screenshot Tests on Bitrise <img width="48px" height="48px" align="absbottom" src="./assets/icon.svg"/>

Run the android-testify tests annotated with [`@ScreenshotInstrumentation`](https://github.com/ndtp/android-testify/blob/main/Library/src/main/java/dev/testify/annotation/ScreenshotInstrumentation.kt) on an emulator hosted by Bitrise and report the test results.

Features:

- Configures the emulator for optimal performance with Testify
- Runs Android Testify tests
- Save failed test images to the workflow [Artifacts](https://devcenter.bitrise.io/en/builds/managing-build-files/build-artifacts-online.html)
- Prepares a JUnit XML test report which can be viewed with [Bitrise Test Reports](https://devcenter.bitrise.io/en/testing/test-reports.html#ot-lst-cnt)


Learn more at https://testify.dev

## Prerequisites

You must have an emulator configured and ready prior to invoking this step.

It is recommend that you follow [this guide](https://devcenter.bitrise.io/en/steps-and-workflows/workflow-recipes-for-android-apps/-android--run-tests-using-the-emulator.html#ot-lst-cnt) to [create an emulator](https://www.bitrise.io/integrations/steps/avd-manager) and [wait for it to be booted](https://www.bitrise.io/integrations/steps/wait-for-android-emulator).


You can also export the test results and failed images using an [Export test results to Test Reports](https://www.bitrise.io/integrations/steps/custom-test-results-export) add-on Step and a [Deploy to Bitrise.io Step](https://www.bitrise.io/integrations/steps/deploy-to-bitrise-io) to make the test results available in the Test Reports add-on.


## Configuration Inputs

### adb_command

The command-line statement to run with adb

### app_apk

The full path to the application apk under test. For library projects, this will be the test apk.

### app_package

The package name of the app. For example, `com.sample`

### target_apk

The file name of the test runner .apk

### target_package

The package name of test runner .apk
For example, `com.sample.test`

### test_runner

The fully qualified class name for the Instrumentation test runner. e.g. `androidx.test.runner.AndroidJUnitRunner`

### module

The gradle project module name. For example, `:app`

### verbose

You can enable the verbose log for easier debugging.

---

# License

    MIT License
    
    Modified work copyright (c) 2022 ndtp
    Original work copyright (c) 2021 Daniel Jette
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
