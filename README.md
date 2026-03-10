# AI-Image-Forgery-Detection-Based-on-Eyelink-Eye-Tracking-Trajectory
### dataset
(https://huggingface.co/datasets/JingmingWang/AI-generated-Image-Detection/tree/main)
A standardized image dataset (150 images total) was built under the principle of same semantics with different sources, controlling semantic and visual consistency to avoid irrelevant variable interference. It included 100 AI-generated images (Doubao, ByteDance Inc., China; Kimi, Moonshot AI Inc., China) and 50 real photography images sourced from Pexels (https://www.pexels.com/zh-cn/), covering five categories: natural scenery(zrfg), portrait(rwxx), animals and plants(dzw), food still life(nsjw), and daily life(shcj) scenes. For each category, both models generated 10 images respectively with a unified prompt framework, and 10 real images were screened for semantic alignment
### `dzw_output.xlsx`
This file contains eye-tracking fixation data collected from an Eyelink eye tracker, used for research on **AI Image Forgery Detection Based on Eye-Tracking Trajectory**.

The dataset involves **8 participants (labeled 2–9)** who each viewed **30 randomly ordered plant/animal images** (TRIAL_INDEX 1–30) and judged whether each image was AI-generated.

| Column Name               | Type    | Description                                                                 |
|---------------------------|---------|-----------------------------------------------------------------------------|
| RECORDING_SESSION_LABEL   | String  | Participant ID (ranges from 2 to 9, representing 8 subjects)                |
| TRIAL_INDEX               | Integer | Image stimulus ID (ranges from 1 to 30, corresponding to files in `dzw_picture/`) |
| CURRENT_FIX_X             | Float   | X coordinate of the current fixation point (screen pixel position)          |
| CURRENT_FIX_Y             | Float   | Y coordinate of the current fixation point (screen pixel position)          |
| CURRENT_FIX_INDEX         | Integer | Sequential index of the fixation within the current trial                   |
| CURRENT_FIX_PUPIL         | Integer | Pupil size during the current fixation (arbitrary units)                   |
| CURRENT_FIX_DURATION      | Integer | Duration of the current fixation (in milliseconds)                           |
| IS_FAKE                   | Integer | Image authenticity label (1 = AI-generated fake image, 0 = real image)       |

### `dzw_picture/` Folder
This folder contains **30 plant/animal stimulus images** presented to participants in random order.
- File naming: `dzw-{TRIAL_INDEX}.png` (e.g., `dzw-1.png` corresponds to TRIAL_INDEX=1)
- Content: Mixed set of real and AI-generated plant/animal photos
- Purpose: Visual stimuli for the eye-tracking experiment
