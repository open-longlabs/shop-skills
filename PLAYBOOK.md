# Shoe playbook

Every shop sells different shoes. This playbook has a prompt template and a check for 9 shoe types.
Pick your type, attach photos of your real shoe from every side, fill in the brackets and check every image before it goes out.

| Shoe type | How it held up in our test |
|---|---|
| [Lace-up sneaker](playbook/templates/01-lace-up-sneaker.md) | Not passed yet: the logo fix held, but 6 eyelets came out instead of 5 on both images. |
| [Running shoe](playbook/templates/02-running-shoe.md) | One of 2 images failed: an extra logo and 6 eyelets instead of 5. |
| [Hiking or work boot](playbook/templates/03-hiking-boot.md) | Not passed yet: the logo landed beside the top hook on 4 of 4 images. Lacing held on 3 of 4. |
| [Dress shoe](playbook/templates/04-dress-shoe.md) | One of 2 images failed: 6 lace holes instead of 5. The sole text held on 2 of 2. |
| [Loafer or slip-on](playbook/templates/05-loafer.md) | One of 2 images failed: the strap cut-out came out almond shaped, not a half moon. |
| [Sandal or slide](playbook/templates/06-sandal-slide.md) | Passed 2 of 2 after one fix: round buckles, 2 straps, 5 toes on every foot. |
| [Heel or pump](playbook/templates/07-heel-pump.md) | One of 2 images failed: a print on the insole that the prompt said not to add. |
| [Clog or mule](playbook/templates/08-clog-mule.md) | Not passed yet: the heel strap rivet sat at the collar edge on 4 of 4 images. The hole rows held on 3 of 4. |
| [Fashion boot](playbook/templates/09-fashion-boot.md) | No fail in 2 images, but the back seam was never visible at this angle. |

## How we tested

One invented shoe per type, text only (no reference photos), 2 images per round. Every numbered point was checked by eye on tight crops. Every count and placement we marked as passed on the final images was counted a second time, item by item.
A point that failed on both images got one changed line and one more round. Hidden or too small to see counts as unsure, never as a pass.
On our real test sneaker, photos from every side put every logo on the right part in one round. Counts and small text still needed an eye there too.

## What we learned across types

1. **Say which side. Then say the other side is empty.** Logos turned up on the inner side of 3 types. On the lace-up sneaker, "the inner side has none" fixed it on 2 of 2 images.
2. **Count every image.** Counts of 3 to 6 were off by one on at least 6 of the 26 images, even when the prompt gave the exact number.
3. **A shape word is a weak word.** "Round" drifted to oval until the prompt also said "not oval".
4. **Some positions won't move from a prompt.** A logo beside the top hook and a rivet at the collar edge stayed put after one changed line. On our real sneaker, fixes like that took an edit on a crop.
5. **The angle decides what you can check.** Ask for the view that shows the part.

## Then check it

Use [shoe-check](skills/shoe-check/) to compare each image with photos of the real shoe. Use [shoe-painpoint-discovery](skills/shoe-painpoint-discovery/) first to write the fact sheet for your own shoe.

by Long//Labs, [longlabs.tech](https://longlabs.tech)
