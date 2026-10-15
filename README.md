# Fatherload

A browser remake of the classic Flash mining game *Motherload*, written in plain JavaScript and shipped as a **single HTML file** — no build step, no dependencies.

**Play it:** open `index.html` in any modern browser, or visit the GitHub Pages site at https://sylvainroy.github.io/Fatherload/

## How to play

Pilot a mining pod, dig for minerals, fly back up to sell them, and spend the money on upgrades so you can dig deeper, faster and safer. Reach the core without running out of fuel or wrecking your hull.

| Key | Action |
|-----|--------|
| `←` `→` (or `A`/`D`, `Q`/`D`) | Move; dig sideways when standing on the ground |
| `↓` (or `S`) | Dig down |
| `↑` (or `W`/`Z`/`Space`) | Fly — uses fuel |
| `1`–`6` | Use an item from the junk shop |
| `E` | Re-open the shop you are standing on |
| `M` | Mute / unmute |
| `Esc` | Close a dialog |

Land on a building at the surface to open it:

- **Fuel station** — buy fuel (running dry underground is game over).
- **Mineral processing** — sell your cargo.
- **Junk shop** — reserve fuel tank, repair nanobots, dynamite, plastic explosives, quantum teleporter, matter transmitter.
- **Repair shop** — fix your hull.
- **Upgrade shop** — drill, hull, engine, fuel tank, radiator and cargo bay, six tiers each.

Underground you'll find ten minerals of increasing value and depth (Ironium → Amazonite), undrillable rock (which falls when you dig out the tile under it — it rests on your pod and dents the hull if it drops from a height), lava that burns your hull (radiators help), and gas pockets that explode. Hard landings dent the hull too.

The game is saved to `localStorage` every time you enter a shop; the title screen offers to continue a saved game.

On touch devices an on-screen D-pad and item buttons appear.

## Development

Everything lives in `index.html`. A small debug hook is exposed as `window.FL` in the console (`FL.P` is the player state, `FL.setT(col,row,tile)` edits the world, `FL.openShop('upg')` opens a shop, etc.).

## The end

At the very bottom of the pit lies the Devil's lair. Break into it and he wakes: he hurls fireballs (three at a time once wounded) and charges at your pod. Hurt him with Dynamite / Plastic Explosives detonated close to him, or ram him with your drill (better drills hit harder). Kill him to claim the Fatherload — a $1,000,000 bonus and the victory screen.
