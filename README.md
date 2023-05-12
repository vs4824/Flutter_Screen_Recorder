# Flutter Screen Recorder

This is a package to create recordings of Flutter widgets. The recordings can be exported as GIFs.

This is pure Flutter/Dart implementation without any dependencies on native or platform code. Thus it runs on all supported platforms.

Please note, that the encoding of the GIF takes a lot of time. On web it is basically useless because it takes so much time.

## 🚀 Getting Started

### Setup

First, you will need to add screen_recorder to your pubspec.yaml:

   ```
   dependencies:
  flutter:
    sdk: flutter
  screen_recorder: x.y.z # use the latest version found on pub.dev
   ```

Then, run flutter packages get in your terminal.

## Example

Wrap your widget which should be recorded in a ScreenRecorder:

   ```
   ScreenRecorder(
  height: 200,
  width: 200,
  background: Colors.white,
  controller: ScreenRecorderController(
    pixelRatio: 0.5,
    skipFramesBetweenCaptures: 2,
  ),
  child: // child which should be recorded
);
   ```

Then use ScreenRecorderController.start() to start recording and ScreenRecorderController.stop() to stop the recording. final gif = await ScreenRecorderController.export() gives you the result which can be written to disk.
