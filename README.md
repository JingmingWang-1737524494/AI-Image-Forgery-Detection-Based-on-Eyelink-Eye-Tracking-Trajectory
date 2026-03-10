# AI-Image-Forgery-Detection-Based-on-Eyelink-Eye-Tracking-Trajectory
### Complete Stimulus Image Dataset

https://huggingface.co/datasets/JingmingWang/AI-generated-Image-Detection/blob/main/dataset.zip

A standardized image dataset (150 images total) was built under the principle of same semantics with different sources, controlling semantic and visual consistency to avoid irrelevant variable interference. It included 100 AI-generated images (Doubao, ByteDance Inc., China; Kimi, Moonshot AI Inc., China) and 50 real photography images sourced from Pexels (https://www.pexels.com/zh-cn/), covering five categories: natural scenery(zrfg), portrait(rwxx), animals and plants(dzw), food still life(msjw), and daily life(shcj) scenes. For each category, both models generated 10 images respectively with a unified prompt framework, and 10 real images were screened for semantic alignment

## Our eye-tracking data were collected using an **Eyelink 1000 Plus** system.

### `dzw_output.xlsx`
This file contains eye-tracking fixation data collected from an Eyelink eye tracker, used for research on **AI Image Forgery Detection Based on Eye-Tracking Trajectory**.

The dataset involves **8 participants (labeled 2–9)** who each viewed **30 randomly ordered plant/animal images** (TRIAL_INDEX 1–30) and judged whether each image was AI-generated.

| Column Name               | Type    | Description                                                                 |
|---------------------------|---------|-----------------------------------------------------------------------------|
| RECORDING_SESSION_LABEL   | String  | Participant ID (ranges from 2 to 9, representing 8 subjects)                |
| TRIAL_INDEX               | Integer | Image stimulus ID (ranges from 1 to 30) |
| CURRENT_FIX_X             | Float   | X coordinate of the current fixation point (screen pixel position)          |
| CURRENT_FIX_Y             | Float   | Y coordinate of the current fixation point (screen pixel position)          |
| CURRENT_FIX_INDEX         | Integer | Sequential index of the fixation within the current trial                   |
| CURRENT_FIX_PUPIL         | Integer | Pupil size during the current fixation (arbitrary units)                   |
| CURRENT_FIX_DURATION      | Integer | Duration of the current fixation (in milliseconds)                           |
| IS_AI                   | Integer | Image authenticity label (1 = AI-generated fake image, 0 = real image)       |

The 30 plant/animal images presented in random order during the experiment are available at the following link (https://huggingface.co/datasets/JingmingWang/AI-generated-Image-Detection/blob/main/dzw_picture.zip).

The images displayed during the experiment differ slightly from the original dataset. They were resized and stretched from the original 4:3 aspect ratio to 16:9, with all pixels uniformly adjusted to a resolution of 1920×1080.

- File naming: `dzw-{TRIAL_INDEX}.png` (e.g., `dzw-1.png` corresponds to TRIAL_INDEX=1)
- Content: Mixed set of real and AI-generated plant/animal photos
- Purpose: Visual stimuli for the eye-tracking experiment
