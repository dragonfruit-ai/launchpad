
<h1 align="center">Dragonfruit AI Launchpad 🚀</h1>

<p align="center">
    <i>Documentation, Components and Examples</i>
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

## Start a Company

Dragonfruit AI is the platform for you to bring your ideas to the world on an enterprise scale.

- Launchpad gives company builders the ability to build and distribute computer vision
  applications, with most of the CV heavy lifting done by Dragonfruit
- Mix-and-match platform capabilities around managed hardware, managed inference, managed compute
  and managed app canvas (including mobile), with your own business logic
- Distribution of your products across select enterprise verticals like retail and manufacturing
  is also possible

----------------------

## Experiment with Real-time CV

Use Dragonfruit AI's live inference capabilities to quickly run real-time
inference over your live video cameras, and receive results sent to a
configured webhook in real-time.

> [!TIP]
> Get started by signing up for Launchpad:
> 1. Visit the Launchpad homepage at [app.dragonfruit.ai/launchpad](https://app.dragonfruit.ai/launchpad)
> 2. Register by completing the (1) video ingestion, (2) account creation, and (3) pre-payment steps.
> 3. Login to the Dragonfruit App at [app.dragonfruit.ai](https://app.dragonfruit.ai)

### Configuration

Various configuration options are available to customize your live inference experience.

#### Config - Video Sources

Launchpad currently supports video ingestion from the following sources:
- Live Webcam Streaming (Via compatible browsers)
- Live RTSP streams (IP cameras) via `rtsp://<user>:<pass>@<host>:<port>/<path>` URLs

> [!NOTE]
> _If you selected the "webcam" option during registration, a streaming option will be available 
> when you open the Launchpad app. You will need to grant permissions to access your webcam, and 
> manually start the stream using the UI._

#### Config - Inference Modes

Launchpad has the ability to run different kinds of inference on your live video streams.
This currently includes:
- Real-time scene to text descriptions
  - `captioning`
- Real-time object detection with bounding boxes
  - `people`
  - `vehicles`
  - `license plates`

#### Config - Webhook Responses

Launchpad sends real-time inference results to a self-hosted webhook of your choice.
The format depends on the chosen inference mode.

> [!TIP]
> Using webhooks in this way allows you to integrate Launchpad with your own applications and services.

