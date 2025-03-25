
<h1 align="center">Dragonfruit AI Launchpad 🚀</h1>

<p align="center">
    <i>Launch Your Real-Time Computer Vision Company <br/> -- Documentation and Examples --</i>
</p>

<p align="center">
    <a href="https://app.dragonfruit.ai/launchpad" target="_blank">
        <img alt="DragonFruit AI Logo" src="docs/copyright/df-logo.png" width=284/>
    </a>
</p>


----------------------

## Overview

Dragonfruit AI's Launchpad is a platform that enables you to build and deploy
real-time computer vision applications in minutes. This repository contains
documentation and examples to help you get started with using and developing
for the platform.

----------------------

## Launchpad Live Inference

Use Dragonfruit AI's live inference capabilities to quickly run real-time
inference over your live video cameras, and receive results sent to a
configured webhook in real-time.

Get started by signing up for Launchpad:
1. Visit the Launchpad homepage at [app.dragonfruit.ai/launchpad](https://app.dragonfruit.ai/launchpad)
2. Register by completing the (1) video ingestion, (2) account creation, and (3) pre-payment steps.
3. Login to the Dragonfruit App at [app.dragonfruit.ai](https://app.dragonfruit.ai)

### Configuration

Various configuration options are available to customize your live inference experience.

#### Config - Video Sources

Launchpad currently supports video ingestion from the following sources:
- Live Webcam Streaming (Via compatible browsers)
- Live RTSP streams (IP cameras) via `rtsp://<user>:<pass>@<host>:<port>/<path>` URLs

_If you selected the "webcam" option during registration, a streaming option will be available
when you open the Launchpad app. You will need to grant permissions to access your webcam, and
manually start the stream using the UI._

#### Config - Inference Modes

Launchpad has the ability to run different kinds of inference on your live video streams.
This currently includes:
- Real-time scene to text descriptions
  - _captioning_
- Real-time object detection with bounding boxes
  - _people_
  - _vehicles_
  - _license plates_

#### Config - Webhook Responses

Launchpad sends real-time inference results to a self-hosted webhook of your choice.
The format depends on the chosen inference mode.
- Using webhooks in this way allows you to integrate Launchpad with your own applications and services.

----------------------

## Launchpad Custom App Development

Dragonfruit AI is the platform for you to bring your ideas to the world on an enterprise scale.

Launchpad provides the ability for 3rd party developers to build and integrate custom
applications into the platform. This allows custom functionality to be added and for
developers to leverage the platform's real-time inference capabilities combined with
their own services.

For more information on how to build your own launchpad applications, see the
example application: [dragonfruit-ai/launchpad-example-app](https://github.com/dragonfruit-ai/launchpad-example-app)
