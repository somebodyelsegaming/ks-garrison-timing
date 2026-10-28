# Kingshot Garrison Reinforcement Timing

Enter your walk time to the castle you're reinforcing, your best guess of the
enemy rally lead's walk time, and how many seconds before (or after) the enemy
hit you want to land. The page tells you when to send.

## Running it

Live at **https://somebodyelsegaming.github.io/ks-garrison-timing/**

One file, `index.html`, with no build step, no backend and no outside links.
Opening it straight from disk works.

## The math

```
enemy hits = rally countdown + enemy walk time
I land     = when I send + my walk time

send at rally countdown = my walk - enemy walk + gap   (land before)
                        = my walk - enemy walk - gap   (land after)
```

If that comes out below 0:00, the rally has already marched. Send when the
enemy march shows `my walk + gap` (before) or `my walk - gap` (after) seconds
left. If that is also below 0, send that many seconds after the hit.

## Credits

Built by Somebody Else, the gnome you know.
