# Reusable JSON Prompt: Tamil Cultural Scene (Chettinad Kolam)

A structured-prompt assignment for **Week 2 · Day 2** of the SE AI Program. It describes one authentic Tamil cultural moment as a **JSON prompt** for AI image and video generators: a Nagarathar woman drawing a pulli kolam at dawn in a Chettinad mansion courtyard during Margazhi.

## Why JSON?

A JSON prompt splits a scene into named fields. That makes it:

- **Reusable:** swap `subject`, `setting` or `time_of_day` and keep everything else
- **Precise:** camera, lighting and palette are set separately instead of being buried in one paragraph
- **Usable for images and video:** still-image fields plus motion and audio fields for video models
- **Safer from clichés:** an explicit `avoid` list keeps out "exotic India" stereotypes and inaccurate regional details

## Schema

| Field | What it controls |
|---|---|
| `subject` | Who is in the frame and what they wear and do (Kandangi saree, rice-flour kolam, poosanipoo) |
| `setting` | Kanadukathan, Chettinad: mutram courtyard, Burma teak pillars, Athangudi tiles |
| `time_of_day` | Pre-dawn, Margazhi, floor still wet |
| `lighting` | Blue-hour sky light plus one brass agal lamp, no artificial fill |
| `camera` | 35mm, f/2.8, eye level, three-quarter view |
| `palette` | Slate blue stone, white flour, mustard and maroon saree, amber lamp |
| `style` | Unposed documentary photograph |
| `aspect_ratio` | 9:16 |
| `avoid` | Wrong regional elements, tourist staging, colour-grade clichés, AI artefacts |
| `duration_seconds`, `camera_motion`, `subject_motion`, `environment_motion`, `audio` | Video-only fields: slow push-in, flour stream, lamp flicker, distant Tiruppavai |

Full prompt: [`tamil_reusable_json_prompt.json`](tamil_reusable_json_prompt.json)

## Generated outputs

| Dawn Kolam in a Chettinad Courtyard | Golden Courtyard Kolam Tradition | Rain-Glossed Courtyard Kolam Ritual |
|---|---|---|
| ![](Dawn%20Kolam%20in%20a%20Chettinad%20Courtyard.png) | ![](Golden%20Courtyard%20Kolam%20Tradition.png) | ![](Rain-Glossed%20Courtyard%20Kolam%20Ritual.png) |

Video output: [`483e6ca5-438f-4bff-b2fa-723879f49cf5.mp4`](483e6ca5-438f-4bff-b2fa-723879f49cf5.mp4)

## How to reuse

1. Copy the JSON.
2. Change the fields for your own scene. Keep the `avoid` list and extend it for your region.
3. Paste it into an image model, or a video model to use the motion and audio fields.

---
Part of my [SE AI Program](https://github.com/pdineshkumar55/SE-AI-Program) coursework.
