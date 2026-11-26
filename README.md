# Citadel of the Azure Tide

An interactive, self-contained WebGL 2 voxel artwork depicting a terraced Mediterranean cliffside harbor sanctuary and celestial lighthouse rising straight from an endless azure sea — built in a single zero-dependency HTML file.

![Interactive WebGL 2 Voxel Artwork](https://img.shields.io/badge/WebGL2-Zero%20Dependencies-2b62c4) ![Single HTML File](https://img.shields.io/badge/Format-Standalone%20HTML-e56b46)

## Highlights

- **Architectural Craftsmanship**: An octagonal travertine-and-terracotta **Astral Lighthouse** with corbelled gallery, rotating crystal Fresnel beacon, and verdigris-copper cupola; an attached **Observatory** crowned with a rotating golden **Armillary Sphere**; a triple **Cobalt-Domed Aegean Chapel** with bell-gable; sixteen cascading whitewashed, peach, and ochre coastal villas with carved balconies, flower boxes, and pergolas; a 5-arch classical limestone **Aqueduct** feeding a tiered waterfall and turning wooden waterwheel; two ridge **Windmills**; a 3-arch stone **Harbor Bridge**; and a monumental natural **Limestone Sea-Arch**.
- **Seamless Voxel Ocean & Reflections**: Half-resolution planar water reflections with half-voxel mosaic ripple refraction, depth-based turquoise-to-sapphire absorption, animated sunlight caustics across the sandy cove seabed and sunken marble columns, boat wakes, shoreline surf lines, and a gap-free endless ocean stretching to distant Aegean caldera ridges.
- **24-Hour Lighting & Volumetric Lighthouse Beam**: Continuous solar/lunar cycle (*Dawn*, *Day*, *Sunset*, *Night*, plus free 24-hour scrubbing and *Let time pass*), backed by 4096px Vogel-PCF shadows, baked 3D flood-filled local light & sky-visibility volumes, multi-pass voxel albedo color bounce, HDR 4× MSAA, 6-level bloom, crepuscular god rays, close-up depth of field, and twin additive volumetric light beams sweeping across twilight and night skies.
- **Four Seasonal Transformations**: Radial wave transitions radiating outward from the lighthouse across **Spring** (bougainvillea & citrus blossoms), **Summer** (sun-drenched cobalt sea & golden warmth), **Autumn** (Tuscan russet/amber vines & falling leaves), and **Winter** (high-elevation Aegean snowfall, Mistral coastal sea-spray, and cozy glowing hearths).
- **Living Ecosystem & World-Driven Spatial Audio**: Turning windmill sails, nested armillary rings, lateen-sailed yacht gliding cleanly beneath the natural sea-arch, cove rowboat with dipping oars, moored fishing boats, leaping southern-bay dolphins, submerged manta ray and reef fish, soaring seagulls, distant horizon sails, fluttering harbor bunting, waterfront café string-lights, evening candle lanterns, curling hearth smoke, and an offline-ready diegetic Web Audio + ElevenLabs spatial coastal soundscape — where every distinct sound is tied to a real object, movement, location, or time event (localized Aqueduct waterfall, windmill blade sweeps, cove rowboat oar strokes, dolphin breaches, live 3D soaring gull calls, dawn/sunset chapel bronze bell, altitude-filtered coastal sea air, seasonal Mistral gusts, and optional acoustic music that ducks gently near active landmarks).

## Live Playable Version

Play the artwork directly in any WebGL 2 desktop or mobile browser at:
**[https://ashmit0014.github.io/citadel-of-the-azure-tide/](https://ashmit0014.github.io/citadel-of-the-azure-tide/)**

## Opening & Playing Locally

No build step, server, or internet connection is required:

1. Download or clone this repository.
2. Open `index.html` directly in any modern WebGL 2 browser (Chrome, Edge, Safari, Firefox) on desktop or mobile.
3. Open **More → Coastal sound** (and adjust **Volume** or toggle **Acoustic music**) to experience the spatial Mediterranean soundscape.

### Controls

| Input | Action |
|---|---|
| **Drag / 1-finger drag** | Orbit camera |
| **Scroll / Pinch** | Zoom in and out |
| **Right-drag / Shift-drag / 2-finger drag** | Pan camera |
| **Arrow keys / `+` / `-`** | Orbit and zoom |
| **`H`** | Toggle minimal / hidden interface |

## Technical Architecture

- **Volume & Meshing**: `288 × 216 × 288` voxel grid chunked into `3 × 3 × 3` frustum- and direction-culled draw groups with 8-byte packed vertices and anisotropy-free ambient occlusion quad triangulation.
- **Lighting Pipeline**: Precomputed half-resolution 3D light (`uLV`) and albedo-bounce (`uBV`) textures, cached directional shadow map, planar reflection FBO, HDR `RGBA16F` 4× MSAA render target, dual-filter bloom, radial god rays, and adaptive resolution scaling for smooth desktop and mobile frame rates.
- **Offline Audio**: All soundscape assets are mastered locally, seamlessly loop-crossfaded, and embedded directly inside `index.html` for zero-dependency offline Web Audio playback — no runtime API calls, external hosts, or credentials required.

## Licensing & Audio Attribution

- **Source Code**: Provided for personal, educational, and open showcase use.
- **Embedded Audio Assets**: Sound effects and acoustic music were generated using [ElevenLabs](https://elevenlabs.io) under an active paid subscription and are embedded strictly as an integral part of this interactive artwork. They may not be extracted or redistributed as standalone stock audio, sound packs, or music libraries.

