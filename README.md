# Fin-___

Registry index for the Fin repo family (formerly Fin-CM-___) (company sites and finance projects) - same model as `CG-___`, `Projects-___` and `cloudy-___`. This repo is an INDEX, not a container: it holds `repos.json` (the registry, a subset of _git-repos-master/repos.json), `clone.sh` (pick which repos to have locally) and one committed relative symlink per member (`<member> -> ../<member>`); the actual clones live as siblings in `~/git/`.

## Members

- [Fin-CM-mqpm](https://github.com/diegonmarcos/Fin-CM-mqpm) - MQPM / StochBates: README and deployer wiring skeleton, no content yet (#1224).
- [Fin-Corporate](https://github.com/diegonmarcos/Fin-Corporate) - Corporate finance (Nexus.z, Field Finance, Project Corporate). Created 2026-10-28.
- [Fin-CM-Blmbrg](https://github.com/diegonmarcos/Fin-CM-Blmbrg) - Blmbrg (fin terminal, market watch, news): README and deployer wiring skeleton; the matching front-labtools projects b-Nxs_Blmmbrg/* move here with the labtools split (#1218). #1224.

## Usage

```
./clone.sh                list what exists and what does not
./clone.sh <name>...      clone those, then link them
./clone.sh --all          clone every member
./clone.sh --link         relink whatever is already cloned
./clone.sh --relink       rewrite every link from the registry
./check-repos-sot.sh      verify repos.json against _git-repos-master
```

`repos.json` is a SUBSET of `~/git/_git-repos-master/repos.json` (the superset index of every repo this account owns): identical name/url/private/doc fields, checked by `./check-repos-sot.sh`.
