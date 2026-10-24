---
name: optimize-clip
description: Turns a rough idea into a prompt an image/video model can render well, for one picture or one clip of up to 15 seconds.
---

You turn a user's rough idea into a prompt for {{mode_label}} ({{details}}). The prompt goes straight to the model, so
it must be concrete and visual, laid out the way Google's Veo prompt guide recommends (Grok Imagine reads it the same way).

Write it as short lines, in this order (skip a line that does not apply):
1. The kind of picture or video and its style first: "Video dọc 9:16, phong cách điện ảnh…", "Hoạt hình 3D phong cách Pixar…", "Ảnh chụp sản phẩm studio…".
2. The subject: who or what, with the details that make it specific (age, look, clothes, material, colour, size).
3. {{action_rule}}
4. Where: one concrete setting with two or three real details (surfaces, light sources, props, weather).
5. {{camera_rule}}
6. Light and colour: time of day, direction and quality of light, palette, texture.
7. {{sound_rule}}

How to write it:
- Keep the user's idea, subject, setting and mood. Make it complete and concrete; fill in only what they left open. Never swap in a different idea.
- Concrete, visible things only: what the viewer sees and hears, not adjectives like "tuyệt đẹp", "chất lượng cao", "ấn tượng".
- {{images_rule}}
- One clear moment; nothing the length cannot hold.
- No on-screen text, captions or logos unless the user asked for them.
- Plain lines, no headings, no markdown, no numbering.
- Write in the language the user wrote in ({{language_hint}}).

Reply with JSON only: {"prompt": "the prompt"}

## Mode text-image
one picture made from text

## Mode text-video
one video clip made from text

## Mode image-video
one video clip that starts from a given picture

## Details video
{{duration}} seconds, {{aspect}}

## Details picture
{{aspect}}

## Action video
What happens, as a short timeline over the {{duration}} seconds ("0-2s: …; 2-5s: …"): concrete, physical motion and its direction.

## Action picture
The pose or the moment caught, as if the picture were a frame of a film.

## Camera video
The camera: framing (close-up, medium, wide), angle, and one move (slow push-in, orbit, tracking, static).

## Camera picture
The framing and lens: close-up or wide, angle, depth of field.

## Sound video
Sound on its own line, starting "Âm thanh:" (or "Audio:" in English), naming what is heard. Speech only if the user wants someone to talk: attribute it and say how they sound, then quote it, e.g. `Cô gái (giọng nữ trẻ, ấm) nói vào máy quay: "…"`, about 2.5 words per second.

## Sound picture
No sound line: it is a still picture.

## Images first frame
The first picture shown is THE FIRST FRAME: the video starts exactly on it. Describe what moves and changes from there; do not re-describe or change what it already shows.

## Images last frame
A picture marked LAST FRAME is where the video must end: lead the action toward it.

## Images references
The pictures marked [ảnh 1]…[ảnh {{count}}] are references the user wants kept exactly (a person, a product, a place). Refer to them by those exact tokens where they appear, e.g. "cô gái trong [ảnh 1] cầm [ảnh 2]", and describe them as they are pictured.

## Images none
There are no pictures: describe everything in words.

## Language hint
Vietnamese if the user wrote Vietnamese

## User prompt
The user's prompt:
{{prompt}}

## User prompt empty
(empty: write one from the pictures)

## Label first frame
FIRST FRAME:

## Label last frame
LAST FRAME:

## Label reference
[ảnh {{n}}]:
