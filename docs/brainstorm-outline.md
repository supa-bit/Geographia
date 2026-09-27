# Geographia — Brainstorming Outline

A desktop app for learning the **geography**, **geology** and **history** of the world, with a
rich profile for every country and territory.

This is a working outline for brainstorming sessions. Each section lists ideas to explore and
**open questions** to settle. Nothing here is decided yet.

---

## 1. Vision & Goals

- **One-line pitch (draft):** "An explorable atlas of Earth — its land, its rocks and its
  people — that you can learn from, not just look at."
- **Core goals**
  - Make the world *explorable*: zoom from planet to region to country to landmark.
  - Connect the three lenses: *where* things are (geography), *why* the land looks the way it
    does (geology), and *what happened there* (history).
  - Turn browsing into lasting knowledge (quizzes, spaced repetition, progress tracking).
  - Work fully offline once installed.
- **Non-goals (to confirm)**
  - Not a turn-by-turn navigation or GIS analysis tool.
  - Not a news/current-events feed.
- **Open questions**
  - Is this primarily a *reference atlas with learning features* or a *learning app with a
    reference atlas*?
  - What is the one feature that makes someone choose this over Google Earth, Wikipedia or
    Seterra?

## 2. Target Audiences

| Audience | Needs | Implications |
|---|---|---|
| Students (middle school → university) | Curriculum-aligned facts, exam prep | Quizzes, lesson paths, printable sheets |
| Teachers | Classroom demos, assignments | Presenter mode, shareable lesson sets |
| Lifelong learners / trivia fans | Curiosity, challenge | Games, streaks, deep-dive articles |
| Travelers | Country briefings | Quick-facts cards, culture & practical info |
| Home-schooling families | Structured, safe content | Guided courses, parental progress view |

- **Open questions:** Which *one* audience defines the MVP? Age range and reading level?

## 3. Knowledge Domains

### 3.1 Physical Geography
- Continents, oceans, seas, gulfs, straits
- Mountain ranges, peaks, plateaus, valleys
- Rivers, lakes, drainage basins, waterfalls
- Deserts, forests, grasslands, tundra, ice sheets
- Climate zones (Köppen), biomes, ecoregions
- Natural hazards: earthquakes, volcanoes, cyclones, floods

### 3.2 Human Geography
- Political borders, capitals, administrative divisions
- Population, density, urbanization, major cities
- Languages, religions, ethnic groups
- Economy: GDP, industries, exports, resources
- Infrastructure: major ports, rail, airports
- UNESCO World Heritage Sites

### 3.3 Geology
- Plate tectonics: plates, boundaries, hotspots, rift zones
- Rock types and geologic provinces; bedrock maps
- Geologic time scale (eons → ages) with an interactive timeline
- Formation stories of landmark features (Himalayas, Great Rift Valley, Grand Canyon, Iceland)
- Paleogeography: Pangaea → today, animated continental drift
- Mineral and energy resources and why they are where they are
- Seismic and volcanic activity (historical and recent)

### 3.4 History
- Deep-time human history: migrations, early civilizations
- Empires and their extents over time (animated borders)
- Exploration routes, trade routes (Silk Road, spice routes)
- Colonization and independence movements
- Wars and treaties that reshaped borders
- Per-country history timeline with key events and figures
- **Open question:** How to present contested history neutrally and with sources?

### 3.5 Cross-Domain Connections (the differentiator)
- "Why is this city here?" — rivers, harbors, passes, resources
- "How did the land shape history?" — mountains as borders, deltas and early farming
- "How did geology create wealth?" — oil, gold, diamonds, fertile volcanic soil
- Story-driven "journeys" that combine all three lenses

## 4. Country & Territory Profiles

### 4.1 Scope of Entities
- 193 UN member states + 2 observer states
- Dependent territories, overseas regions, Crown dependencies
- Partially recognized states, disputed areas, and places where most people want independence
  (shown as countries — see 4.2 Statehood Policy)
- Antarctica and uninhabited territories
- Reference list: ISO 3166-1 (249 codes) as a baseline, with extensions
- **Open questions**
  - Confirm the numbers in the evidence standard (4.2): 50% minimum turnout, and how many polls
    over how many years make tier 2?
  - Include subnational units (states, provinces) in v1 or later?

### 4.2 Statehood Policy
- **Decision:** if a majority of a place's population wants independence, Geographia shows it as
  a country, whether or not other states recognize it. Everyone has the right to
  self-determination.
- The place gets a full country profile, its own color on the political map, and a place in
  country quizzes and rankings.
- Each profile states its recognition status plainly: which states or bodies recognize it, and
  who claims the territory.
- The profile cites the evidence of majority support, such as a referendum result or a
  representative poll, with its date.

#### Evidence Standard
A free, fair and recent referendum is the strongest evidence; consistent polling is a weaker
second tier, labeled as such. Party votes and declarations never count on their own.

| Tier | Evidence | Shown as country? | Profile label |
|---|---|---|---|
| 1 | Referendum that passes every quality test below | Yes | Majority support (referendum, year) |
| 2 | Several reputable, independent polls showing a majority over several years, with a plain "do you want independence?" question | Yes | Majority support (polling) |
| 3 | Votes for pro-independence parties | Only as support for tier 1 or 2 | — |
| Not evidence | Declarations by governments, leaders or armed groups; protest size | No | — |

A referendum counts as tier 1 only if it is:

1. **Free and fair:** independent observers, no military occupation, no coercion.
2. **Boycott-proof:** turnout of at least 50% of registered voters, so a boycott cannot decide it.
3. **Clear:** a plain question with a real independence option.
4. **Current:** the latest valid vote wins; a later valid "no" overrides an earlier "yes".

**Whose majority:** where displaced people, refugees, settlers or boundary lines are contested,
the profile shows the dispute openly instead of picking an answer. Western Sahara's referendum
has stalled since 1991 largely over who belongs on the voter roll.

#### Test Cases
Figures are approximate, from memory, and must be verified before they go into the app.

| Case | Result | Passes the standard? | Outcome under the policy |
|---|---|---|---|
| Bougainville 2019 | ~98% yes | Yes | Shown as a country (not yet independent) |
| South Sudan 2011 | ~99% yes | Yes | Country (independent since 2011) |
| Montenegro 2006 | ~55.5% yes | Yes | Country (independent since 2006) |
| Scotland 2014 | ~55% no | Yes | Not shown as a country |
| Quebec 1995 | ~50.6% no | Yes | Not shown as a country |
| New Caledonia 2021 | ~96% no, turnout ~44% | No: independence side boycotted | Earlier valid votes (2018, 2020) were no |
| Catalonia 2017 | ~90% yes, turnout ~43% | No: turnout below 50%, unionists boycotted | Needs tier 2 polling evidence |
| Crimea 2014 | ~97% yes (official) | No: held under military occupation | Not evidence |
| Greenland (polls) | Majority yes in principle; falls if living standards drop | Depends on the question's wording | Tier 2 review |

### 4.3 Profile Sections (draft data model)
- **Identity:** official & common names, native names, flag, coat of arms, anthem, motto
- **Codes:** ISO alpha-2/alpha-3/numeric, calling code, internet TLD, currency code
- **Location:** continent, region (UN M49), coordinates, borders/neighbors, coastline length
- **Physical:** area, highest/lowest point, major rivers & lakes, climate, biomes
- **Geology:** tectonic setting, dominant rock types, notable formations, hazards, resources
- **People:** population, growth, density, life expectancy, languages, religions, ethnic groups
- **Government:** system, capital, head of state/government, administrative divisions,
  independence date, memberships (UN, EU, AU, ASEAN…)
- **Economy:** GDP, GDP per capita, main sectors, exports/imports, currency
- **History:** summary, timeline of key events, historical names/borders
- **Culture:** cuisine, festivals, sports, arts, notable people, World Heritage Sites
- **Practical:** time zones, driving side, plug type, visa notes (maybe)
- **Media:** photos, maps, audio pronunciation of names
- **Sources & last-updated date** on every data field

### 4.4 Profile Features
- Side-by-side country comparison
- "Similar countries" and "Neighbors" navigation
- Rankings (largest, most populous, highest…) with map highlighting
- Historical slider: see the country's borders and name at any year

## 5. Core App Features

### 5.1 Map & Globe
- 3D globe and 2D map with smooth switching; multiple projections
- Toggleable layers: political, physical/relief, tectonic plates, geology, climate, biomes,
  population density, historical borders, trade routes
- Label density controls; hover tooltips; click-through to profiles
- Measure distance and area; draw/annotate (for teachers)

### 5.2 Timeline
- Unified time slider spanning geologic time → human history → present
- Logarithmic/zoomable scale to handle billions of years and recent decades
- Events pinned to map locations

### 5.3 Search & Discovery
- Global search (countries, cities, features, events, people)
- Filters and faceted browsing
- "Random place" / "Place of the day"

### 5.4 Articles & Media
- Short, layered articles (summary → detail → deep dive)
- Illustrated diagrams (e.g., how a subduction zone works)
- Optional narration / text-to-speech

## 6. Learning & Engagement

- **Guided courses:** "Countries of Africa", "Rocks & Plates 101", "Empires of the Ancient World"
- **Quiz types:** click-the-map, flags, capitals, outlines, multiple choice, timeline ordering,
  "which is bigger", rock/feature identification
- **Spaced repetition** for facts the learner gets wrong
- **Progress tracking:** mastery per region/topic; "fog of war" map that reveals as you learn
- **Gamification:** streaks, achievements, passport stamps, collections
- **Difficulty levels** and age-appropriate modes
- **Teacher tools:** custom quiz builder, class codes, export results (later phase)
- **Open questions:** Single-player only, or local multiplayer / classroom competitions?

## 7. UX & Design

- Information architecture: Globe (home) → Region → Country → Topic
- Keyboard shortcuts and fast navigation for power users
- Light/dark themes; map style consistent with theme
- Accessibility: screen-reader labels, colorblind-safe palettes, scalable text,
  non-map alternatives for map quizzes
- Localization: UI translation, localized place names, right-to-left support
- **Open questions:** Visual identity — classic atlas, modern minimal, or playful?

## 8. Content & Data Sources (to evaluate licensing)

| Domain | Candidate sources |
|---|---|
| Boundaries & base maps | Natural Earth, OpenStreetMap, geoBoundaries |
| Places & names | GeoNames, Wikidata |
| Country statistics | World Bank Open Data, UN Data, CIA World Factbook (public domain) |
| Elevation & bathymetry | SRTM, GEBCO, ETOPO |
| Geology & tectonics | USGS, OneGeology, PB2002 plate boundaries, GPlates reconstructions |
| Volcanoes & earthquakes | Smithsonian Global Volcanism Program, USGS earthquake catalog |
| Historical borders | CShapes, historical-basemaps, Wikidata |
| Heritage & culture | UNESCO World Heritage list, Wikipedia/Wikimedia Commons |
| Flags & symbols | Wikimedia Commons (check per-file licenses) |

- **Open questions**
  - Licensing compatibility (CC BY-SA share-alike vs. commercial distribution)
  - Editorial process: who writes/reviews articles? AI-assisted drafting + human review?
  - Update cadence and how updates ship to offline users

## 9. Technical Architecture (options to compare)

- **Desktop shell:** Tauri (small, Rust) vs. Electron (mature, heavier) vs. native
  (Qt, .NET MAUI, SwiftUI) vs. Flutter desktop
- **Map rendering:** MapLibre GL (2D/vector), CesiumJS (3D globe), deck.gl (data layers),
  or a custom WebGL/three.js globe
- **Data storage:** SQLite for facts and progress; PMTiles/MBTiles for offline vector tiles
- **Content format:** Markdown/MDX articles + structured JSON/YAML per country
- **Data pipeline:** scripts that fetch, clean, merge and version data into a release bundle
- **Updates:** app auto-update + separate delta content packs
- **Platforms:** Windows, macOS, Linux (tablet/web later?)
- **Open questions**
  - Install size budget (full offline globe can be several GB — tiered downloads?)
  - Any cloud features (sync, accounts) or strictly local?

## 10. Business & Distribution

- Models: one-time purchase, freemium with paid course packs, free/open-source,
  education licenses
- Channels: direct download, Microsoft Store, Mac App Store, Steam, school procurement
- **Open question:** Open-source the data pipeline and content to build a contributor community?

## 11. Phased Roadmap (draft)

1. **Prototype** — interactive globe, political layer, 250 country quick-fact cards, search
2. **MVP** — full country profiles, physical layer, flags/capitals/map quizzes, progress
   tracking, offline mode
3. **Geology release** — tectonic & geology layers, geologic timeline, formation stories
4. **History release** — historical borders slider, empires, per-country timelines
5. **Learning depth** — guided courses, spaced repetition, achievements
6. **Classroom** — teacher tools, presenter mode, class progress
7. **Expansion** — subnational regions, localization, community content

## 12. Risks & Challenges

- Political sensitivity: disputed territories, names and historical narratives
- Data accuracy and staleness; conflicting sources
- Licensing constraints on maps, images and text
- Scope creep — three huge domains at once
- Performance of 3D globe with many layers on older hardware
- Content production cost (writing, illustration, fact-checking)

## 13. Success Metrics

- Learning: quiz mastery gains, retention over 30/90 days
- Engagement: sessions per week, courses completed, streak length
- Content: coverage completeness per country, source freshness
- Quality: crash-free sessions, startup time, reported data errors

## 14. Brainstorming Session Prompts

- If a user opens the app for 5 minutes, what should they walk away knowing?
- What does the *perfect* country page look like? Sketch it.
- Which three "journeys" best showcase geography + geology + history together?
- What would make a teacher recommend this to their whole class?
- What should we deliberately leave out of v1?
- How do we make rocks and plate tectonics as exciting as flags and capitals?
- How should the app behave when facts are disputed or uncertain?

## 15. Next Steps

- [ ] Pick the primary audience and the MVP feature set
- [ ] Verify the test-case figures and draw up the first list of places the statehood policy covers
- [ ] Audit data sources and licenses; choose the baseline datasets
- [ ] Prototype the globe with two candidate rendering stacks
- [ ] Draft the country profile schema and fill 5 sample countries end-to-end
- [ ] Sketch wireframes for Globe, Country Profile and Quiz screens
