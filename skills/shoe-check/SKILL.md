---
name: shoe-check
description: Check an AI image of a real shoe against photos of the real shoe and find what is wrong (logos, counts, badge text, pair, ground) before it goes on a shop page or an ad.
---

# shoe-check

## Why AI shoes still break

At full size an AI shoe looks perfect. Up close the logo sits on the wrong part, one hole is missing or the badge reads nothing.
Image tools copy the look of a shoe, not its parts list, so small counted and written details drift.

## Check any AI shoe image

1. **Zoom.** Never judge the whole picture. Look at the toe, both sides, tongue, collar, heel and sole up close.
2. **Compare with the real photo.** Put the same part of the real shoe next to it, from the same side.
3. **Count without assuming.** Count holes, eyelets, dots and straps one by one in both images, row by row. Do not decide the number first.
4. **Logos per side.** Each logo on the right part and the right side, none missing, none added.
5. **Text letter by letter.** Read every badge and label in both images. Garbled is wrong.
6. **Pair and ground.** One left and one right shoe, mirror images. The shoe stands on the ground with a shadow.

Anything hidden, blurry or too small to read is unsure, never a pass.

## Pick your shoe type

| Shoe type | What breaks | The one check |
|---|---|---|
| Lace-up sneaker | eyelet count, logo moved or missing, badge text | count eyelets per side in both images |
| Running shoe | tread melts into swirls, mesh turns to plastic | zoom the sole edge and the mesh |
| Hiking or work boot | eyelets and speed hooks, tread lugs | count eyelets and hooks separately |
| Dress shoe | lace stations, stamped text, perforation pattern | count only openings a lace goes through |
| Loafer or slip-on | hardware missing or moved, suede shines | find each strap, bit or tassel on the real photo |
| Sandal or slide | strap count, extra or melted toes | count toes and straps on every foot |
| Heel or pump | heel shape, floating shoe, buckle placement | zoom where heel tip and toe touch the floor |
| Clog or mule | hole and dot rows, heel strap hinge | count rows, not only the total |
| Fashion boot | zipper and seam position, shaft shape | trace the zipper from top to bottom |

The sneaker row comes from our own runs. The other rows are the usual failure points we collected, not measured rates.

## Prompt snippets: fix what a prompt can fix

Formula: part + exact count + position anchored to another part + material + how the parts connect + what must not appear.
Write every count into the prompt, but any count can still come out off by one, small or large. Check every count by eye.

Template (attach the real photos from every side, then fill in your shoe, or let shoe-painpoint-discovery write the list for you):

```
The reference photos show the [shoe] from every side plus close-ups of every detail. Copy it exactly, do not redesign:
1. [Main logo]: [colour, size], on [which side and part]. Nowhere else.
2. [Second logo or badge]: on [its part]. Not on [where AI puts it].
3. [Tabs or straps]: [how many], [flat or rope].
4. Eyelets: exactly [number] per side.
5. [Holes or dots]: exactly [number] in [rows].
6. A left shoe and a right shoe, mirror images.
No extra logos, no changed colours.
```

The same template filled in for our test sneaker, the prompt we used (shortened, brand names replaced with plain part names):

> The reference photos show the sneaker from every side plus close-ups of every detail. Copy it exactly, do not redesign:
> 1. Small logo: yellow, on the outer side of the forefoot, low. Nowhere else.
> 2. Triangle logo: on its own black patch on the outer side of the ankle collar. Not on the tongue.
> 3. Pull tabs: two flat black webbing tabs. Flat straps, not rope.
> 4. Eyelets: exactly 5 per side.
> 5. Side holes: exactly 15 in 3 rows, 5, 6 and 4 from the top.
> 6. Heel cage: exactly 9 raised round dots in a tilted 3 by 3 grid.
> 7. A left shoe and a right shoe, mirror images.
> No extra logos, no changed colours.

With photos from every side, a prompt like this got every logo on our test sneaker onto the right part. Small text and exact counts still needed the check below.

A full template for each of 9 shoe types: [Shoe playbook](../../PLAYBOOK.md).

## Issue-finder prompt

Attach the real photos first, the AI image last, then paste this:

```
I attach photos of a real shoe and one AI image of the same shoe. The LAST image is the AI image. All other images are real photos.
Shoe type: [your shoe type, for example casual lace-up sneaker].

Find every place where the AI image does not match the real shoe. Work in this order:
1. From the real photos, list every part a buyer could check: each logo and the side it sits on, every badge or label and its exact text, everything you can count (eyelets, holes, dots, studs, straps, hooks) and how it is arranged, the sole, the heel, the material, the pair (one left, one right).
2. Find each part in the AI image. Look at that region up close in both images side by side, not at the whole picture.
3. Counts: count in the real photo and in the AI image separately, one item at a time, row by row. Do not decide in advance what the number should be. Then check the pattern spot by spot: for every position in the real pattern, is there an item in the same spot in the AI image? An empty, flat or smeared spot is a FAIL. If you cannot see every item clearly, the answer is UNSURE.
4. Text and logos: for each letter, first describe its strokes in the real photo (closed bowl, stem, tail, bar), then the same letter in the AI image. A missing stroke, a letter that turned into another letter, or a smeared letter is a FAIL. A logo that is missing, moved or added is a FAIL. If the letters are too small to describe stroke by stroke, the answer is UNSURE, never PASS.
5. Then shape, material, pair, ground contact and toes if a foot shows.

Answer with one line per part:
part | where | real photo | AI image | PASS, FAIL or UNSURE | why
Only write PASS when you saw the part clearly and it matches. Hidden, blurry or too small to read is UNSURE, never PASS.
End with one line: VERDICT: FIX (any FAIL), CHECK BY EYE (any UNSURE) or LOOKS RIGHT. Then list what a person still has to check by eye.
```

Treat its answer as a list of places to look, then decide by eye. It can miss a single missing dot or hole.

## What no check can prove

- Parts that are hidden at this angle. Hidden is unsure, never a pass.
- Exact colour under different light, real material, fit, comfort or durability.
- That a model answer is right. It is a second pair of eyes. A person makes the final call on a tight crop next to the real photo.
