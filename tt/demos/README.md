# Dev-Health

## Problem
- Arthritis, poor digestion, back pain, and increased risk of cardiovascular disease are all associated with prolonged improper posture
- 86% of American workers have sedentary jobs that essentially foster poor posture
- In addition, people can develop poor posture through common day-to-day activities such as watching TV, driving, and using their cell phone

## Our Solution
- We created DevHealth to help tech workers avoid succumbing to poor posture. Sitting and coding in front of a computer screen for several hours on end can, over time, lead to severe health consequences.
- DevHealth runs in the background on your computer and analyzes changes in your posture. If you are shifting into poor posture, DevHealth notifies you of this by playing an alert bell sound. 

## A Bright Future
- We worked on a “tint” feature that tinted the user’s screen to a certain degree of redness depending on how long they held poor posture. The intention was to make it increasingly difficult for them to see the screen in order to prevent them from holding poor posture for too long. 
- However, we couldn’t implement the feature on time because we had trouble getting the necessary computer privileges to dim the screen, which we later found out was a known issue with Electron.
- We also want to continue spreading awareness on the health hazards of long-term improper posture. We believe our product should be used at every company because it can help the significant amount of workers working sedentary jobs avoid posture-related health complications.

## Dependencies
- Yarn
- Babel
- Node.JS
- TensorFlow (Posenet)
- Electron JS


## How to try it out
Unfortunately, as of 2020, recent versions of posenet seem to have made Dev-Health pose tracking extremly slow, leaving the app almost unusable. This app is also no longer being developed, although the team may get together soon and try to rebuild it with an eye more towards scalability (after all, we built it originally in 72 hours). You can still try it out by cloning this repo, running yarn in this folder, and then running npm start, but no promises on performance.


Below this is the PoseNet read me:

# PoseNet Demos

## Contents

### Demo 1: Camera

The camera demo shows how to estimate poses in real-time from a webcam video stream.

<img src="https://raw.githubusercontent.com/tensorflow/tfjs-models/master/posenet/demos/camera.gif" alt="cameraDemo" style="width: 600px;"/>


### Demo 2: Coco Images

The [coco images](http://cocodataset.org/#home) demo shows how to estimate poses in images. It also illustrates the differences between the single-person and multi-person pose detection algorithms.

<img src="https://raw.githubusercontent.com/tensorflow/tfjs-models/master/posenet/demos/coco.gif" alt="cameraDemo" style="width: 600px;"/>


## Setup

cd into the demos folder:

```sh
cd posenet/demos
```

Install dependencies and prepare the build directory:

```sh
yarn
```

To watch files for changes, and launch a dev server:

```sh
yarn watch
```

## If you are developing posenet locally, and want to test the changes in the demos

Cd into the posenet folder:
```sh
cd posenet
```

Install dependencies:
```sh
yarn
```

Publish posenet locally:
```sh
yarn build && yarn yalc publish
```

Cd into the demos and install dependencies:

```sh
cd demos
yarn
```

Link the local posenet to the demos:
```sh
yarn yalc link @tensorflow-models/posenet
```

Start the dev demo server:
```sh
yarn watch
```

To get future updates from the posenet source code:
```
# cd up into the posenet directory
cd ../
yarn build && yarn yalc push
```
