# Ocarina experiments 🏺🎶

Brainstorm + project plans, inspired by Mattias Krantz's
["Ukulele that transforms into a guitar mid-performance"](https://youtu.be/O42Vz0488fs).

Spirit of the project: take a familiar instrument, ask an absurd question about it,
then actually build the answer through many failed prototypes.

## The idea pile

### Aleksi's ideas

- **Shoecarina** — ocarina that's also a shoe (+ detachable wheels, scope creep welcome 😁)
- **Electric ocarina**
- **Tunable ocarina** — one exists with a sliding stick inside; other mechanisms surely possible
- **Inflatable shirt as ocarina**
- **Oca-guitar** — ocarina that attaches to a guitar neck
- **Handless ocarina** — still playable across an octave (≥4 holes needed)
- **Polyphonic ocarina** — mechanism plays a harmony note (e.g. E sounds when you blow C);
  default to triads, modulate a half step up/down as a starting point
- **Mouth-as-chamber ocarina** — the player's mouth is (part of) the resonating chamber
- **Inflatable ocarina** — holes leak air, but maybe an inflatable *inside* modulates tone?
- **Other-gas ocarina** — played with a gas other than air

### Claude's batch 1

1. **Mitosis ocarina** — transforms mid-performance by splitting into two smaller ocarinas;
   solo becomes duet. Hard part: two acoustically valid chambers that also form one valid
   chamber when joined.
2. **Fire ocarina** — thermoacoustic (Rijke tube): a flame/heater drives the oscillation, so it
   drones with no breath at all; you just finger the holes. Must warm up before it can play.
3. **Drinkable ocarina** — chamber partly filled with a beverage; pitch range rises as you drink.
   Compose the piece around the sips.
4. **Poi / Doppler ocarina** — ocarina on a tether you swing; scoop-fed airflow sounds it
   (handless *and* lungless), swing speed = breath pressure, Doppler gives free vibrato.
5. **Talking ocarina** — second squishable silicone chamber in series acts as an artificial
   mouth; hand-shaped formants → vowels, "wah", almost-words. Fully acoustic talk box.
6. **Walk-in ocarina** — room-sized; the player stands inside the chamber, bellows/fan provides
   air, person-sized shutters are the finger holes. Sub-bass ocarina.

### Claude's batch 2

1. **Ice ocarina** — cast from ice; warm breath thins walls and widens holes, so tuning drifts
   as the piece is played. A song composed for the instrument's own melting.
2. **Grown ocarina** — grow a gourd inside a 3D-printed mold shaped like a tuned chamber
   (square-watermelon technique), dry it, cut the voicing.
3. **Perpetual ocarina** — two chambers with one-way valves: one sounds on exhale, one on
   inhale. The note never stops; circular breathing with zero technique.
4. **Hurdy-gurdy ocarina** — you blow, a music-box-style crank barrel covers/uncovers the holes.
   Swap barrels like cartridges; punch-card ocarina programming.
5. **Applause ocarina** — squeeze-bulb ocarina in a glove; clapping pumps the air.
   Make twenty and the audience's ovation is the final chord.
6. **Bird-playable ocarina** — birdfeeder whose perches sit on the holes of a wind-fed chamber;
   compose the probabilities by seed placement, wild birds play it.
7. **Steam ocarina** — kettle whose spout is a voiced ocarina; rising pressure uncovers holes in
   sequence so it plays a melody, and the final note means tea's ready.
8. **Weather ocarina** — rooftop installation; wind vane feeds the fipple, weather sensors drive
   hole shutters. The day's weather is the score.

## Current favorites

- Shoecarina
- Icecarina
- Inflate-carina
- Mitosis / transform-carina
- Generally: things that **increase functionality** — tunability, better vibrato/texture,
  more sounds playable by one human, combinable/transforming instruments

## Project plans

### Step 0 (shared foundation): print a boring ocarina

Nearly every idea lives or dies on the **fipple** (windway + sharp labium edge). Print a known-good
open-source ocarina, get it singing, then deliberately mess with it: tape over holes, shove things
in the chamber, sand the labium. A week of this builds the acoustic intuition everything else needs.

Good starting STLs (all free):

- [Single Print Ocarina (Julius3E8, Printables)](https://www.printables.com/model/249011-single-print-ocarina) —
  full octave, no supports, no gluing/tuning; the low-friction first print
- [12-hole playable Ocarina (Mikolas Zuza, Printables)](https://www.printables.com/model/65399-12-hole-playable-ocarina) —
  tuned A4–F6, standard 12-hole fingering
- [Updated 12 Hole Ocarina (RobSoundtrack, Thingiverse)](https://www.thingiverse.com/thing:2755765) —
  remix with improved voicing window, labium edge and airway
- More via [STLFinder: 6-hole](https://www.stlfinder.com/3dmodels/6-hole-ocarina/) /
  [12-hole](https://www.stlfinder.com/3dmodels/12-hole-ocarina/)

Acoustics background (the ocarina is a **Helmholtz resonator**):

- Pitch is set by the ratio of *total open hole area* to *chamber volume* — hole position barely
  matters, hole size is everything. This is why weird chamber shapes (shoe! ice!) are fair game.
- [Ocarina physics (Ocarina Wiki)](https://ocarinas.fandom.com/wiki/Physics)
- [Tone production & acoustics (ocarinas.org)](https://www.ocarinas.org/tone-production-acoustics/)
- [Helmholtz resonator notes (UIUC Physics 406, PDF)](https://courses.physics.illinois.edu/phys406/sp2017/Lab_Handouts/Helmholtz_Resonators.pdf)
- [Vessel flute (Wikipedia)](https://en.wikipedia.org/wiki/Vessel_flute) — why ocarinas sound
  "overtoneless": the resonator amplifies essentially one frequency
- Deep end: [compressible LES simulation of ocarina sound (arXiv)](https://arxiv.org/pdf/0911.3567)

### Project 1: Inflate-carina (= the tunability project) — weekend mod

A bladder *inside* the chamber changes effective air volume → changes pitch. So the inflatable idea
is secretly the tunable-ocarina idea.

- **Build:** printed ocarina + one extra port + small balloon + squeeze bulb (aquarium tubing).
- **Gives you:** continuously variable tuning, squeeze-wobble vibrato, expressive pitch bends.
- **Do this first:** cheapest build, directly serves the vibrato/texture goal, teaches Helmholtz
  intuition by feel.

### Project 2: Icecarina — reusable mold, freezer-cheap iteration

A reusable silicone mold makes it reproducible: refill with water, freeze overnight, every failed
prototype costs ~nothing.

- **Mold:** 3D-print a two-part master, cast silicone around it. The chamber needs a pullable
  core — design the master with that in mind.
- **Tuning:** near-freezing air has a lower speed of sound, so an ice ocarina plays *flat* vs. the
  same geometry in plastic. Tune the master sharp to compensate. (Measure the offset by playing the
  Step-0 ocarina cold out of the fridge — a very funny experiment.)
- **Killer issue:** warm moist breath hits the windway first, so the fipple — the one part needing
  a crisp edge — melts fastest. Options: embed a small plastic windway insert in the ice (hybrid,
  easiest), blow through a long tube so breath cools en route, or feed with a hand pump.
- **Clear ice matters:** bubbles at the labium wreck the voicing → directional freezing (clear-ice
  cube technique: insulated cooler, freeze top-down).
- **Deliverable:** one piece composed for the melt, filmed as the tuning drifts and the
  instrument dies. Retakes are free because: mold.

### Project 3: Mitosis ocarina — the flagship

Buildable version: one printed body, **two fipples, removable partition wall** down the middle
(O-ring/gasket seals).

- Partition **in** → two independent small chambers, two players, duet.
- Partition **out** → one doubled chamber at a lower register; the same motion that removes the
  wall plugs the second windway.
- **V1:** prove both states play in tune. **V2:** make the split elegant (twist-and-pull, magnets).

### Shoecarina — the anytime palate cleanser

- Air-cushioned soles already contain a sealed air chamber → **the sole is the chamber**, holes
  along the outsole edge.
- **V1:** a shoe you hold and blow into (funny).
- **V2:** heel-bellows so each step provides breath — play a bassline by walking (much funnier).
- Wheels remain in scope. Obviously.

### Bonus: multi-chamber + bladder = drone-that-bends

Real makers get polyphony from multi-chamber ocarinas (2–3 chambers, each with its own fipple, mouth
covers all windways at once). Apply the Project-1 bladder to one chamber of a double-chamber print →
melody + a drone that can bend. A genuinely novel instrument from two known pieces.

### Suggested order

Step 0 → Inflate-carina → Icecarina → Mitosis, with Shoecarina between as the palate cleanser.

## Where to 3D print (Aalto / Helsinki area)

Verified Aug 2026:

### Aalto Fablab (Otaniemi, Otakaari 7 / Aalto Studios) — probably the best bet

- Free machine use for anyone in the Aalto community; you pay only for materials. Open to
  students/staff during opening hours, plus public open days for everyone.
- 3D printers, laser cutter, vinyl cutter, desktop CNC, electronics bench — laser cutter is handy
  later for bellows/mold parts.
- They run intro sessions for specific machines.
- [aalto.fi/services/aalto-fablab](https://www.aalto.fi/en/services/aalto-fablab) ·
  [studios.aalto.fi/fablab](https://studios.aalto.fi/fablab/) ·
  [fablab.aalto.fi](https://fablab.aalto.fi/)

### Aalto Design Factory / DF Labs (Viima building)

- Was indeed closed for student access over summer (18 Jun – 16 Aug 2026); **normal access resumes
  17 Aug 2026**, doors 7:45–15:30 (student access doesn't work after hours without the course).
- Independent/after-hours access to DF Labs requires the prototyping course
  **MEC-E3900 "Prototyping Tools at the Design Factory"** (online self-study + face-to-face
  workshop).
- [designfactory.aalto.fi/access](https://designfactory.aalto.fi/access/) ·
  [facilities](https://designfactory.aalto.fi/facilities/)

### ARTS workshops / Vilhon Paja (Väre)

- Finland's biggest print farm: ~35 Ultimakers set up for self-service use after an intro course
  ([ARTS 3D Print](https://www.aalto.fi/en/workshops-aalto-school-of-arts-design-and-architecture/3d-print),
  [Vilhon Paja](https://vilhonpaja.aalto.fi/en/facilities),
  [intro course on OpenLearning](https://openlearning.aalto.fi/course/view.php?id=175)).
- Course reservations get priority, but capacity is unmatched — good for batch-printing prototypes.

### Public libraries (free-ish, no Aalto affiliation needed)

- **Oodi (Helsinki):** makerspace with 3D printers + laser cutters, free to use, small material
  fee per print. [Helmet makerspaces](https://helmet.finna.fi/Content/pajat-ja-verstaat?lng=en-gb)
- **Espoo: Iso Omena & Sello:** free makerspaces, printers reservable via Varaamo (one at a time).
  Note: as of spring 2026 Espoo centralised all library 3D printers to these two — Entresse,
  Lippulaiva and Tapiola no longer have them.
  [Espoo makerspaces](https://www.espoo.fi/en/culture-and-leisure/libraries/makerspaces-espoo-city-library) ·
  [centralisation news](https://www.espoo.fi/en/news/2026/03/libraries-3d-printers-be-centralised-iso-omena-and-sello-libraries)
- Iso Omena's paja also has Formlabs resin printers — relevant if a fipple ever needs finer detail
  than FDM gives.

### Practical plan

Fablab or a library for the Step-0 ocarina this week; ARTS farm for batch iterations; consider
MEC-E3900 once the mitosis build starts and after-hours DF access becomes worth it.
