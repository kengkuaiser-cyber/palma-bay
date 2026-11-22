# Palma Bay — Top-Down Open-World Crime Game

First-version playable game for the make.fun bounty "Make GTA 6" ($1,666).
Original story, city and art only — no Rockstar assets, no external requests.

## Play it

Open `index.html` in a desktop browser. No build step, no server, no network needed.
Progress (money, missions completed) saves in `localStorage`.

## Controls

- **WASD** — move on foot / drive
- **Shift** — sprint
- **E** — enter / exit a car
- **Mouse click or Space** — shoot toward the mouse
- **P or Esc** — pause
- **R** — restart after Wasted / Busted / Story Complete

## What is in the game

- A 2400×1800 city with a road grid, buildings, parks, traffic cars and pedestrians
- On foot and by car: enter/exit cars, drive, traffic that follows the roads
- Car theft: stealing a moving traffic car raises your wanted level; parked cars are free to take
- Wanted level 0–5 stars: police cars chase and ram you, officers on foot chase, shoot and arrest you
- Combat: shoot, police return fire, pedestrians flee, fallen pedestrians drop $20
- HUD: health, money, wanted stars, mission objective, driving/on-foot state, minimap
- Start screen, pause, Wasted / Busted lose states, Story Complete win state

## Missions (story: Marco owes a debt in Palma Bay)

1. **First Wheels** — steal a car, drive it to Dana's Garage. Reward $250.
2. **The Pickup** — drive to the north pickup point, bring the package back to Dana. Reward $500.
3. **The Getaway** — grab the cash at the bank (wanted level jumps to 3), escape to the safehouse. Reward $800.

## Verified locally

- `node --check` on the extracted game script: passes, no syntax errors.
- Headless smoke test (stubbed canvas/DOM): 120 frames update + draw with no errors,
  20 cars, 14 pedestrians, 20 buildings; missions 1–3 play through in order,
  money totals $250 + $500 + $800 = $1,550 and the win screen triggers.

## Unfinished / known limits

- No sound, no mobile/touch controls (desktop keyboard + mouse only).
- Traffic follows simple road rules and can occasionally clip a building corner.
- No in-game settings menu; difficulty is fixed.
- Nothing has been submitted to make.fun — this is local code only, by design.
