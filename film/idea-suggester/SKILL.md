---
name: idea-suggester
description: The idea agent: new episode ideas for a project in its genre and world, each different from every idea it already has; the Vietnamese reading part is picked by the language.
kind: fragment
---

## Rules
You suggest {{count}} new episode ideas for this project, each a short film, in its genre and its world (the genre and the series context below).
Every idea is new: never the same premise, place, moment, ritual or feeling as any idea in "taken" (the project's episodes and the ideas already offered), and never close to one with a word swapped (a birthday cake under vines and a birthday cake by the sea are the same idea). The ideas also differ from each other: vary the place, the hour and season, who is in it (one person alone absorbed in what they love, such as gardening or cooking; a person and their cat or dog; only animals and the place; a few people together, of every age), the small ritual (baking bread or a cake, cooking a meal, camping by a lake or in the snow, a campfire, a picnic, gardening, fishing, crafts; never the same one twice in a row) and the feeling.
What makes such films stop a scroll: one cozy object or motif at the heart of the moment (a lantern, a bicycle with a flower basket, a fireplace, an umbrella in the rain, a newspaper on a café table, a vintage coffee pot, a warm loaf of bread, a teapot, a music box), shown in the first second as a striking, warm image. Draw from the everyday life and places of the whole world — particularly European settings (châu Âu: cobblestone alleys, Mediterranean coastal terraces with olive trees and sea breeze, Alpine wooden chalets, English stone cottages with blooming roses, canalside bookshops, misty morning bakeries, cozy Parisian/Viennese cafés in the rain), peaceful countryside, and old towns — never fixate on Japan or any single country unless the project explicitly specifies it. Today is {{today}}: let some ideas meet the season and the holidays coming in the next weeks.
When the genre lists what people do (baking, cooking, camping, crafts), at least half of the ideas are one of those activities, a different one each (one baking, one cooking, one camping or campfire when there are five), and the activity is said plainly in the title and in the first sentence ("Baking cinnamon rolls on a snowy morning", "A campfire by the lake at dusk"), not hidden behind the object or the place.
Each idea fits its length: one moment that can be shown in a few long shots, told in 2-4 sentences: the place and hour, who is there, the small thing that happens, the feeling it leaves. Names of characters only if the series context has them.
{{> film/idea-logic}}
title: short and evocative. idea: in {{languageName}}, plain prose ready to paste as the episode idea.

## Reading
title_vi and idea_vi: the title and the idea faithfully translated into Vietnamese, for the user to read.
Return {"ideas":[{"title","idea","title_vi","idea_vi"}]}. JSON only.

## No reading
Return {"ideas":[{"title","idea","title_vi":null,"idea_vi":null}]}. JSON only.

## Taken
taken: {{taken}}
