# SL_Ai

**An offline AI tutor and study planner for Android. No data, no signal, no subscription.**

FNB App of the Year Hackathon 2026 · Team ONE OF ONE · Junior Douglas Mthethwa

Demo video (89 seconds): https://youtu.be/evDIHMLNits

## What it does

SL_Ai puts a tutor, a maths solver and a planner in one app that runs with the device in airplane mode.

- **Offline tutor.** Chat or talk to a Qwen 2.5 AI that runs on the device and knows the learner's progress.
- **Exact solver.** Step by step maths and physics up to university level, with graphs. Our own maths engine works out the answer, and the AI only explains it.
- **Check my working.** Scan your pages of working and SL_Ai shows the exact line that went wrong, with a tip.
- **Lessons that adapt.** SL_Ai learns which teaching style works for each subject (worked example first, picture it, story and more).
- **Exam booth, Doc Master, review cards, mastery map and a weekly progress report** for parents and teachers.
- **Planner.** Tasks, calendar, goals, notes, a focus timer and brain games, including Morabaraba.
- **Private.** No account, no analytics. Everything stays on the device.

## Try it

1. Download `SL_Ai.apk` from the [latest Release](../../releases/latest) and install it. You may need to allow "Install unknown apps".
2. Open SL_Ai and tap **Explore with sample data** at the top right. You meet Lerato, a sample learner. No login or password is needed, and the app lock is off.
3. For the AI, go to Settings › Ai and tap **Get** on SL_Ai Light (547 MB, once on Wi-Fi). After that, everything works offline.

If the in-app download is slow, the model files are also attached to the Release. Download one and use **Import a model file (.task)** in Settings › Ai.

### Recommended device

SL_Ai is designed tablet first. We built and tested it on a Huawei MatePad SE 11:

- 10 to 11 inch screen, 1920 x 1200
- 8-core processor (Kirin 710)
- 4 GB memory
- Android 10 or newer
- About 1 GB free storage for the app and SL_Ai Light (2.5 GB for SL_Ai Smart)

SL_Ai also runs on phones with its own compact layout. The tablet shows the full experience.

## AI models

| Model | Size | Best for |
|---|---|---|
| SL_Ai Light: Qwen 2.5 0.5B Instruct | 547 MB | Recommended. Fast and stable on 4 GB devices |
| SL_Ai Smart: Qwen 2.5 1.5B Instruct | 1.6 GB | Better teaching, needs 6 GB of memory or more |

Both run on the CPU by default. The graphics chip is an optional switch in Settings.

## How it is built

- **App:** Kotlin and Jetpack Compose, with phone and tablet layouts
- **AI engine:** Qwen 2.5 running on MediaPipe LLM Inference, with a watchdog that restarts a stuck answer
- **Maths engine:** our own Kotlin solver, graph analysis, 22 diagram templates and the work checker
- **Scanning:** CameraX and ML Kit text recognition, live and on the device
- **Voice:** the device's own text-to-speech; speech recognition with Moonshine through sherpa-onnx

## Credits and licences

- Qwen 2.5 by the Qwen team, Alibaba Cloud (Apache 2.0)
- MediaPipe by Google (Apache 2.0)
- ML Kit text recognition by Google (ML Kit terms)
- CameraX and Jetpack Compose by Google (Apache 2.0)
- sherpa-onnx by k2-fsa (Apache 2.0) and the Moonshine speech model by Useful Sensors (MIT)
- Background music in the demo video is original

The repository and release stay available until at least 30 November 2026.
