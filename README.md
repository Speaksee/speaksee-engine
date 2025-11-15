<img src="https://github.com/user-attachments/assets/912ce733-a8cb-4fc7-9a0a-9d33b4331525" alt="banner" width="100%"/>
<div align="center">
  <h1>Speaksee</h1>
  <h4>AI-powered Speaker Following Subtitles</h4>
  <p>An AI system that detects the active speaker and renders dynamic, speech-bubble-style subtitles that follow each person on screen.</p>
  <img src="https://github.com/user-attachments/assets/07bfe0c7-5897-41c4-ad7f-8e9070bfbea1" alt="demo" width="800" height="auto" />
</div>

<br />

<!-- Table of Contents -->
# Table of Contents

- [About the Project](#star2-about-the-project)
  * [Description](#notebook-description)
  * [Features](#dart-features)
- [Argument & Usage](#gear-argument--usage)
  * [Customization Options Arguments](#art-customization-options-arguments)
  * [Usage Example](#computer-usage-example)
- [Contributors](#busts_in_silhouette-contributors)
</br >

## :star2: About the Project

### :notebook: Description
<strong>Speaksee: AI-Powered Speaker-Following Subtitles</strong>
<br/>
Speaksee is an AI system that elevates video communication by automatically detecting who is speaking and displaying dynamic, speech-bubble-style subtitles that follow each speaker on screen.
Whether in movies, TV dramas, recorded podcasts, or interviews, Speaksee helps audiences stay engaged by clearly linking every spoken line to the correct person — no more guessing who said what.

Leveraging multi-modal audio–visual processing, Speaksee identifies active speakers, tracks their position frame-by-frame, and renders clean, responsive subtitles in real time or during post-production. This makes content far easier to watch, especially in multi-speaker environments.
<br/>

### :dart: Features
<strong>1️⃣ Core Functionality</strong>
- Dynamic Subtitle Placement — Speech-bubble-style subtitles that follow each speaker on screen
- Multi-modal Active Speaker Detection — Accurately identifies speakers using both video and audio
- Automatic STT & Segment Processing — Extracts text from audio and matches it to each speaker per segment
- Non-intrusive Layout — Calculates optimal subtitle positions without obscuring other people’s faces

<strong>2️⃣ Customization Options</strong>
Allows users to personalize subtitle appearance and layout to suit their preferences and viewing comfort.
- Font Size & Thickness — Adjust text size and boldness
- Font Color — Choose text color (BGR format)
- Bubble Color & Transparency — Customize speech bubble background and opacity
- Padding — Set distance between text and bubble border
</br >

## :gear: Argument & Usage
### :art: Customization Options Arguments

#### Video Processing Parameters
`--videoName`
- **Type**: `str`
- **Default**: `"sample"`
- **Description**: Specifies the name of the demo video to process. Often used as the filename (e.g., `sample.mp4`) without the extension.

`--videoFolder`
- **Type**: `str`
- **Default**: `"demo"`
- **Description**: Specifies the folder path where input videos, temporary files, and output result files will be stored.

#### Text Style Parameters

`--fontSize`
- **Type**: `float`
- **Default**: `1.0`
- **Description**: Sets the font size to apply to subtitles or text. Corresponds to the `fontScale` value used in OpenCV's `cv2.putText`.

`--fontColor`
- **Type**: `int`, `nargs=3`
- **Default**: `[255, 255, 255]` (B, G, R)
- **Description**: Sets the text color. Input in BGR order, which is OpenCV's default color format.
  - Example: `[255, 255, 255]` → White
  - Example: `[0, 255, 0]` → Green

`--thickness`
- **Type**: `int`
- **Default**: `2`
- **Description**: Sets the thickness of text or outlines. Works identically to the `thickness` value in OpenCV's `cv2.putText`.

#### Speech Bubble Style Parameters

`--bubbleColor`
- **Type**: `int`, `nargs=3`
- **Default**: `[0, 0, 0]` (B, G, R)
- **Description**: Background color of the speech bubble. Input in BGR order.
  - Default `[0, 0, 0]` → Black

`--bubbleAlpha`
- **Type**: `float`
- **Default**: `0.7`
- **Description**: Represents the **transparency (alpha value)** of the speech bubble.
  - `0.0` → Fully transparent
  - `1.0` → Fully opaque
  
  Controls the transparency ratio when the speech bubble is composited with the background video.

`--padding`
- **Type**: `int`
- **Default**: `10`
- **Description**: Sets how much spacing the text should have inside the speech bubble. Internal padding value of the bubble box.

### :computer: Usage Example

```bash
python speaksee.py --videoName "my_video" \
                 --videoFolder "videos" \
                 --fontSize 1.5 \
                 --fontColor 0 255 0 \
                 --thickness 3 \
                 --bubbleColor 50 50 50 \
                 --bubbleAlpha 0.8 \
                 --padding 15
```
<br />

## :busts_in_silhouette: Contributors

### Team Members
- 김하늘
- 이주승
