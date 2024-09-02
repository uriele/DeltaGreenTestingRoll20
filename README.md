# DeltaGreenTestingRoll20
New Sheet for Playtest

## New Features

- Advanced Weapon Rolls
- Modifier roll using key binding (Shift by default, Ctrl, Meta, Alt also available)
- Global Modifier option (for people using iPads)
- Roll parser (the attacks that allow for a roll only accept numbers or dice or any operation between the 2
- Navigation Anchors
- Ritual rolls (allows multiple types of expenditure for the ritual, including stats, wp, and hp)
- Ritual rolls can be used to attack or heal (the attack or heal button will appear)
- Bonds now automatically update willpower and bond score when rolled
- When a bond reaches 0, the button will turn to grey and will not be usable anymore (broken bond)
- It is possible to automatically keep track of low willpower (-20 to all rolls except sanity and luck) and 0 willpower (all rolls automatically fail)
- The handler can keep track only of the skills they are interested in by pinning them to the sheet
![image](https://github.com/user-attachments/assets/53ff29e9-3fa0-4a6c-9f99-4c752dee5aab)
- Advanced features for the weapons include: shotgun (+20%) and the possibility to have different damages at different distances, blast radius (+20%), accessories, and selective fire
- The sheet can keep track of the bullet spent (assumed 1 per shot, except the selective fire that uses 3,5,10,20 to add higher lethality)
- The sheet can automatically keep track of the new breaking points

## Fixes
- [x] Wrong logic in tracking bullets
- [x] Label to lethality buttons
- [x] Add ammunition label to bullets
- [x] Fixed wrong numbering in the sheet
- [x] Add an option in the settings to switch from character creation bonds (created with rank==CHA) to in-game bonds (created with rank==CHA/2)
- [ ] Setting button to hide the rituals in the character sheet (the CSS does not seem to work on the repeating section for some reason)
- [x] Add numbering to the pinned named skills (now they show as Art 1, Art 2, etc... Adding the entire name would have required more coding, risking introducing bugs)
- [x] Fixed bug with the versioning function that did not copy the correct name of the weapon while updating to the new version
- [x] Versioning will move the repeating_skills of an NPC that match existing named weapons to the named skill, pin them on the sheet, and remove the repeating skill field. NOTE: The skill parsing is CASE INSENSITIVE but SPACE SENSITIVE. If there is a leading space or multiple spaces between words, it will not port them automatically. Also, if spelling errors or names differ from the official ones, it will not work.
- [x] Add experimental handler sheet. Work in progress. By putting an Agent's name, the sheet will track their STATS, WP, HP,SAN and possible breaking points and adaptations. NOTE: the name must be unique, at least when inserted in the sheet. After the name is registered, the unique character_id will be used instead to track the player's information.
- [ ] Add a button to refresh the handler information: at the moment, since the pieces of information are not present on the sheet itself but are read using starRoll, the sheet is only updated when reopened. To fix this I will add a button on the top of the handler sheet to "refresh" the information on click.
