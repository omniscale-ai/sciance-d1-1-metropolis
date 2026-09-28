# Materials Intelligence Metropolis — SCIANCE D1.1

**Live view:** https://omniscale-ai.github.io/sciance-d1-1-metropolis/

An interactive 3D city that maps the **Materials Science chapter** of the Horizon Europe SCIANCE
Deliverable D1.1 (*State of the art for scientific research using AI for each pilot scientific area*,
Task 1.1 landscape report, chapter revision v3). The chapter's five research themes become districts
along a south-to-north corridor, following its own integrated workflow:

1. **AI-Enabled Materials Modelling** — 10⁻¹⁰ m (Ångström)
2. **Intelligent Materials Design** — 10⁻⁹ m (unit cell → macromolecule)
3. **Data-Driven Materials Characterisation** — 10⁻⁹ – 10⁻⁶ m (atom column → grain)
4. **Closed-Loop Experiment Acceleration** — 10⁻³ – 10⁻¹ m (droplet → bench)
5. **AI for Responsible & Scalable Production** — mg → kg → Fab

## How to read the map

| On the map | Meaning |
| :--- | :--- |
| **Spires** | Infrastructures, model families and platforms named in the chapter. Height = maturity as the report grades it (routine › specialist › emerging); contested claims sit low. |
| **Highways** ⚡ | Flows of data, models, recipes or materials between spires, with one-way arrows. ⛴️ **Ferries** are weak or episodic flows; 🚧 **planned roads** are called for by the report but do not exist yet. |
| **Traffic** | A constraint on a flow: congestion builds up before an incident pin. On a planned road the constraint is a ⛔ barrier — the reason it is not built. |
| **Queues** | A slow step inside a platform: backlog cubes and a wait-time chip at the spire (e.g. 232-min GC batches, ~3.9 % robot faults). |
| **Weather** | A cross-cutting problem over whole districts: a coloured tape along the border of every district it affects, and a forecast chip in the district's corner. |
| **Priorities** 🎯 | Research challenges and recommendations as destinations: a ground target with a pin above it (height = impact). Green arcs are spires that advance it, red arcs are constraints that block it. |

Click anything for its card and relations; use **🧭 Route** to see every incident between two spires.
Numbers on chips are taken from the source text only.

## Contents

| Path | What |
| :--- | :--- |
| `index.html`, `city-data.js` | The static viewer served by GitHub Pages (MapLibre GL, no build step) |
| `spec/01-domain-profile.yaml` | Discovery-stage domain profile extracted from the chapter |
| `spec/02-city-spec.json` | Semantic city specification (schema v2) the viewer is compiled from |

## Rebuilding

This site is generated with [Metropolis-Kit](https://github.com/omniscale-ai/metropolis-kit)
(`examples/sciance-materials/`). To regenerate after editing the spec:

```bash
git clone git@github.com:omniscale-ai/metropolis-kit.git
cd metropolis-kit
python3 -m cli.compiler --spec examples/sciance-materials/02-city-spec.json --web-dir ../sciance-d1-1-metropolis/
```

## Source & licence

Content is derived from the SCIANCE D1.1 Materials Science chapter (Horizon Europe SCIANCE, grant
101293570; chapter author Andrey Ustyuzhanin, contributor Vitalii Kapitan), which is licensed by the
SCIANCE Consortium under CC BY 4.0. The deliverable is a draft; the map reflects chapter revision v3.
