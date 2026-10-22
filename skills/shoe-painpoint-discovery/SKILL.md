---
name: shoe-painpoint-discovery
description: Before you make AI images of a real shoe, turn photos of that shoe into its fact sheet, the parts AI is likely to break and a prompt snippet for this exact shoe.
---

# shoe-painpoint-discovery

The step before [shoe-check](../shoe-check/). Find what can go wrong on your shoe before you generate anything.

## What you need

- Photos of the real shoe from every side: outer, inner, back, top and sole.
- Close-ups of every small detail: badges, labels, hole fields, dots, lacing.
- Your own photos, or brand photos you are allowed to use.

Fewer sides means fewer facts. In our runs, three photos without a side view gave us a logo on the wrong part.

## Discovery prompt

Attach the photos, then paste this:

```
I attach photos of one real shoe from several sides. Write its fact sheet: everything an AI image of this shoe has to get right.

Go part by part: toe, both sides, tongue, laces, collar, heel, back, sole. List every part a viewer counts, matches, reads or places:
- every logo: on which side and which part it sits (outer side, inner side, tongue, collar, heel, sole)
- lace stations: openings a lace actually passes through, per side. Holes next to the laces that no lace goes through are not lace stations.
- holes, dots, studs: the total and the rows (for example 5, 6, 4 from the top), plus anything that looks similar but is not counted
- tabs and loops: flat webbing or rope, where they stand
- every badge or label: the exact text, letter by letter. If you cannot read it, write UNREADABLE, never guess.
- materials and colours of each panel, the sole and its pattern
Write where each part sits relative to another part ("low on the outer forefoot, just above the sole", "below the tongue tab").

Then flag the parts AI image tools usually break. In our own runs these broke: a logo moved to the wrong part (side logo put on the tongue), a logo left out, badge text garbled, hole rows wrong while the total was right, counts off by one.

Output:
1. A fact sheet table: part | where it sits | what it is | count and counting rule | exact text | risk (high or low)
2. Anything you could not see in these photos (which side or detail is missing).
3. A prompt snippet of 60 to 80 words for this shoe: each risky part with its exact count, its position anchored to another part, its material, how parts connect and what must not appear. Keep every count in the snippet and add that each count must be checked by eye.
```

## Fact sheet template

| Part | Where it sits | What it is | Count and counting rule | Exact text |
|---|---|---|---|---|
| Side logo | outer side, low on the forefoot, just above the sole | small, embroidered | 1, outer side only | none |
| Lace stations | along the tongue | openings a lace passes through | 5 per side; unused holes do not count | none |
| Badge | on the tongue, below the pull tab | round, woven | 1 | the text, letter by letter |

One row per part a viewer counts, matches, reads or places. Every position is anchored to another part.

## Worked example from our run

A purple mid-top sneaker. Our fact sheet said, in words:
- A logo patch sits on the outer side of the ankle collar, not on the tongue.
- A small logo sits low on the outer forefoot, just above the sole.
- 5 lace stations per side: 4 holes in the upper plus one fitting at the top. Holes next to the laces that no lace passes through are not counted.
- 15 larger holes in a stitched side panel, in rows of 5, 6 and 4 from the top.
- 9 raised dots on the heel cage in a tilted 3 by 3 grid.

The first AI image, made from three photos and a vague prompt, put the collar logo on the tongue and left the forefoot logo out. With photos from every side and this fact sheet in the prompt, both placements came out right.

## Then run shoe-check

Take the fact sheet and the snippet, generate your images, then check each one with [shoe-check](../shoe-check/).
