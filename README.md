# Ifra's Bestie Life 🏡💜

*The Little World of Ifra*: a cozy 3D life-simulation game made just for Ifra. Built with React, Vite, Three.js / React Three Fiber, Drei, Tailwind, Framer Motion, Lucide and Howler.js.

**Play it live:** https://ifras-bestie-life.vercel.app

Every push to `main` deploys automatically to Vercel.

## Run it

```bash
npm install
npm run dev      # play at http://localhost:5173
npm run build    # static site in dist/
```

## Personalise it

Everything Ifra reads lives in **`src/config/gameConfig.js`**. That includes her name, the title, every dialogue line, the cafe menu, heart and key messages, NPC lines, easter eggs, achievements, her default look, the wardrobe options and the final letter (including who it is signed by). Edit that file only; the engine doesn't need to change.

## Ifra's avatar

Ifra has a detailed avatar: expressive eyes with lashes and highlights, arched brows, glossy lips, soft layered waves with caramel highlights, a cardigan set, sneakers and gold hoops. In the wardrobe (bedroom or Shopping Street) you can change:

- Outfit colour and style (cardigan set, dress, hoodie)
- Skin tone, hair colour and hairstyle
- Accessories, hats and bags

## Controls

| Desktop | Phones & tablets |
|---|---|
| WASD / arrows to walk, Shift to run, Space to jump | Joystick (bottom-left), jump button |
| E to interact, drag the mouse to look, mouse wheel to zoom | ★ button to interact, drag the screen to look |
| Esc for the pause menu (achievements, settings, restart) | Pause button (top right) |

## Map of the code

- `src/config/gameConfig.js`: all text and options
- `src/store/useGame.js`: progression, quests, achievements (zustand)
- `src/game/layout.js`: world positions, colliders, interactables, collectibles
- `src/game/collision.js`: circle-vs-box collision + camera clipping
- `src/audio/sound.js`: every sound and both music loops are synthesised at runtime (no audio files)
- `src/components/scene/*`: 3D world (Town, Bedroom/Cafe, Park, Shops, SecretHouse, SecretRoom, Character, Player, CameraRig)
- `src/components/ui/*`: intro, HUD, minimap, dialogs, cafe and shop panels, pause menu, touch controls, finale
