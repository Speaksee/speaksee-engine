# Arguments Documentation

## Video Processing Parameters

#### `--videoName`
- **Type**: `str`
- **Default**: `"sample"`
- **Description**: Specifies the name of the demo video to process. Often used as the filename (e.g., `sample.mp4`) without the extension.

#### `--videoFolder`
- **Type**: `str`
- **Default**: `"demo"`
- **Description**: Specifies the folder path where input videos, temporary files, and output result files will be stored.

## Text Style Parameters

#### `--fontSize`
- **Type**: `float`
- **Default**: `1.0`
- **Description**: Sets the font size to apply to subtitles or text. Corresponds to the `fontScale` value used in OpenCV's `cv2.putText`.

#### `--fontColor`
- **Type**: `int`, `nargs=3`
- **Default**: `[255, 255, 255]` (B, G, R)
- **Description**: Sets the text color. Input in BGR order, which is OpenCV's default color format.
  - Example: `[255, 255, 255]` → White
  - Example: `[0, 255, 0]` → Green

#### `--thickness`
- **Type**: `int`
- **Default**: `2`
- **Description**: Sets the thickness of text or outlines. Works identically to the `thickness` value in OpenCV's `cv2.putText`.

## Speech Bubble Style Parameters

#### `--bubbleColor`
- **Type**: `int`, `nargs=3`
- **Default**: `[0, 0, 0]` (B, G, R)
- **Description**: Background color of the speech bubble. Input in BGR order.
  - Default `[0, 0, 0]` → Black

#### `--bubbleAlpha`
- **Type**: `float`
- **Default**: `0.7`
- **Description**: Represents the **transparency (alpha value)** of the speech bubble.
  - `0.0` → Fully transparent
  - `1.0` → Fully opaque
  
  Controls the transparency ratio when the speech bubble is composited with the background video.

#### `--padding`
- **Type**: `int`
- **Default**: `10`
- **Description**: Sets how much spacing the text should have inside the speech bubble. Internal padding value of the bubble box.

## Usage Example

```bash
python script.py --videoName "my_video" \
                 --videoFolder "videos" \
                 --fontSize 1.5 \
                 --fontColor 0 255 0 \
                 --thickness 3 \
                 --bubbleColor 50 50 50 \
                 --bubbleAlpha 0.8 \
                 --padding 15
```

![Image](https://github.com/user-attachments/assets/07bfe0c7-5897-41c4-ad7f-8e9070bfbea1)
