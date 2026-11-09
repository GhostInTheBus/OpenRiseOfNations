# Running on the 2003 retail disc data

This branch lets the engine read the original 2003 Rise of Nations retail data (not the Steam Extended Edition). You supply your own game files from your own disc: this repo and its app contain no game data.

What differs in the 2003 data, and how this branch copes:
- Fewer nations, techs, resources, buildings, units, crafts and bonuses than the Extended Edition. The loader pads the missing slots with empty entries and prints a note per table.
- Scenarios are `.sce` (the launcher lists them next to `.scx`).
- Older script dialect: `(real)` casts, scripts called before they are defined, float to int assignment, untyped parameters, and implicit locals that live for the whole script.
- Crash guards for nameless unit types (no graphics, zero collision radius).

Status: the six tutorials and Chess Exercises load. The retail disc ships no skirmish maps and the engine has no random map generator yet. Rule constants come from the Extended Edition executable, so combat and economy numbers may differ from 2003.

Play: open the app, choose the folder that holds your copy of the game (the one containing `data` and `scenario`), then pick a tutorial.
