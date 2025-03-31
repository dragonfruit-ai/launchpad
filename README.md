
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

## Build a Computer Vision App in Seconds

This guide provides simple, vibe-coding instructions to help you build a
computer vision app in seconds, using Dragonfruit AI's Launchpad. Even
an 8-year-old can do it!

### Lovable Instructions

Lovable is an AI-powered platform that turns prompts into code. Here's how
to use Lovable to build your first computer vision app:

1. **Sign up for Lovable**
    - Sign up for [lovable.dev](https://lovable.dev)

2. **Generate your Component**
    - In the lovable interface, submit the following prompt to create your project:

      `````markdown
      Write a simple pure React component called LPSafety, without using pre-existing imports. Only `antd` and `axios` can be used.

      The component must accept the following props:
      ```
      inferface LPSafetyProps {
        host: string; // domain of the API server.
        customer_id: string;  // Customer ID with the application installed.
        app_id: number;  // Global identifier for this application.
        getAuthToken: () => Promise<string>;  // Get an authorisation token for making requests.
      }
      ```

      Add a button called "Fetch License Plates" which, when clicked, calls the "get_plates" endpoint using axios, authenticating with the token obtained from getAuthToken(). The endpoint URL is constructed using the host prop.

      The button will fetch results containing a list of JSON objects like this one:
      ```json
      {
        "plate_number": "OSE5J50",
        "site": {"name": "Site name", "site_id": 66},
        "channel": {"name": "Channel name", "channel_id": 1},
        "thumbnail_url": "https://{thumbnail_url}",
        "timestamp": 1734908445
      }
      ```

      Render the fetched data in an antd table.
      `````

3. **Collect your component**
   - In the lovable chat for your new project, submit the following prompt:
     `````markdown
     Give me a single react component for LPSafety all in one file.
     `````

4. **Create your Launchpad App**
   1. Open a text editor (e.g. Notepad, VS Code) and paste the generated code.
     Save the file as `LPSafety.tsx` in a folder named `LPSafety.dfapp` on your computer.
   2. Add a `config.yaml` file to the `LPSafety.dfapp` folder with the following content:
      ```yaml
      appName: LPSafety
      appDisplayName: License Plate Safety
      ```

5. **Upload your Launchpad App**
   - Zip the `LPSafety.dfapp` folder and upload it to [Dragonfruit Launchpad](https://app.dragonfruit.ai/apps/120).
     Your app will be deployed after approval by the Dragonfruit team.


### ChatGPT Instructions

ChatGPT is an AI chat tool that can generate code from natural language. Here’s how to
create an equivalent version of the LPSafety component using ChatGPT:

1. **Sign up for ChatGPT**
    - Sign up for [chat.openai.com](https://chat.openai.com)

2. **Generate your Component**
   - Enter the same prompt as step 2. in the Lovable instructions above, and submit it to ChatGPT.
   - ChatGPT will create a new canvas containing your code for the component.

3. **Create and Upload your Launchpad App**
   - Follow steps 4. and 5. from the Lovable instructions above to create and upload your Launchpad app.


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

