# shoe-painpoint-discovery

The step before [shoe-check](../shoe-check/). Give it photos of your real shoe from every side and it writes the shoe's fact sheet, flags the parts AI usually breaks and writes a prompt snippet for this exact shoe.

## How to use it

- **No setup:** open [SKILL.md](SKILL.md), attach your photos (outer, inner, back, top, sole and close-ups of small details) to any AI chat that reads images and paste the discovery prompt.
- **As a Claude skill:** add this folder to your Claude skills, then ask "find the pain points of this shoe".
- Then generate your images and check each one with [shoe-check](../shoe-check/).

## Make the prompt your own

The discovery prompt is kept plain on purpose so it works in any AI chat. You can make it stronger with the usual prompt techniques: give the model a role (for example a footwear product photographer or a quality inspector), add constraints for your shop (output language, table format, which parts matter most to your buyers) or add an example fact sheet of a shoe you already checked. That is beyond the scope of this skill.

## Tested

Tested once on 4 real photos of one sneaker: it found 14 of the 16 facts of our checked fact sheet, got none wrong and left 2 open (badge text, hole rows) instead of guessing.

by Long//Labs, [longlabs.tech](https://longlabs.tech)
