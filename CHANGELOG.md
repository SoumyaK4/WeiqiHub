# Changelog

## 0.2.6+78
- Added a cumulative estimated HumanSL rank to Game Focus Dashboard Home. Each completed rank-aware analysis contributes a bounded phase-balanced sample of the app user's moves across 20k–9d, and deleting a game immediately removes its evidence from the recalculated estimate.
- Made Game Focus rank-aware analysis status accurate, including explicit partial/unavailable objective fallbacks, and normalized OGS numeric rankings so unclear SGF ranks can use the discovered account rank.
- Unified KataGo, Career, and Game Focus opening/midgame/endgame labels with fixed per-board-size move cutoffs, migrated saved Game Focus drill phases without reanalysis, and made the Career/Game Focus AI Top 5 metric a literal top-five match.
- Made Performance Report rank output clearer and more honest: it now reports a HumanSL style fit with its full uncertainty range, while two-symmetry raw-policy probes reduce noise without changing normal KataGo analysis workloads.
- Hardened stats and leaderboard sync with restore-before-upload startup and manual Me-page syncing, acknowledged score retries, rolling periods, compressed per-user snapshots, and conflict-safe multi-device merges while retaining compatibility with pre-v0.2.7 clients.
- Renamed the Train and Home destinations to Puzzles and Tools, moved Joseki and Global Leaderboards into their owning sections, capped both tile grids at three columns, put Me first in the wide navigation rail, added a direct Game Focus Profile action, and hid the stats-sync key on screen.
- Replaced Game Tsumegos with Game Focus: import complete local or supported public-account games, analyze them in a resumable KataGo queue, review saved results offline, and turn mistakes into full-board drills with their own two-week schedule.
- Added Game Focus Profile, combining configured public EGD/server identities into source-filterable rank-progress and win/loss charts, cached locally without starting KataGo.
- Improved Game Focus weakness review by ranking groups by average points lost per mistake, opening saved reviews at the selected pre-mistake position, and keeping previews focused on the played move.
- Extended Game Focus with a Last-10/All-time overall and phase-accuracy graph in Weaknesses, cached Performance Reports, shared KataGo settings, optional point-loss filtering, SGF drill export, compact in-chart tooltips, and reliable Refresh after restoring `game_focus.db`.
- Added KataGo Contribution in Tools. Contribute through a compatible secure WebSocket endpoint or a local KataGo process, with live game/analysis viewing and Colab or Modal setup guides.
- Added HumanSL Rank(Avg.) estimates to Performance Report and Career Analysis, and refined Career's rank-guided human-model opponents and styles.
- Updated KataGo Auto Setup for KataGo v1.17.1 and v1.17 transformer models: it resolves backend-specific official releases, matches CUDA with cuDNN, prefers compatible transformer models, and falls back safely; TensorRT remains unavailable until capability detection is supported. New Zealand even games now default to 7.0 komi.
- Hardened Pattern Search for large or interrupted imports with recoverable checkpoints, safer lifecycle handling, restored-index rebuilding, accurate continuation search, and staged portable `.db` database bundle import/export, including direct streaming from Android's system picker.
- Further hardened Pattern Search by rejecting incomplete or illegal SGFs, rebuilding auxiliary indexes atomically with rollback, restoring exact SGF branches and setup actions, preserving stable snapshot identities, and displaying every indexed hit with its correct outline, orientation, and continuation filtering.
- Replaced the legacy Joseki assets with an offline generated OGS explorer containing about 20k positions, full-board Fuseki support, official move categories and marks, source/tag filters, descriptions, and bundled or external related-position links.
- Preserved SGF setup stones, cleared points, player-to-move markers, and compressed setup rectangles across board, record, teaching, task-conversion, and Pattern Search imports.
- Added five stone-sound options with Random playback and selectable English or Chinese voice prompts.
- Improved score estimation across study and game boards with correct prisoner accounting, authoritative side-to-move playouts, urgent capture and atari-save handling, rules-appropriate territory/area/stone totals, safer unconditional-life detection, conservative automatic dead-stone decisions, and whole-group manual marking.
- Report P2P connection failures once instead of dropping or duplicating errors.
- Refined board-coordinate layout and clipping across board views, widened large-screen Performance Report and Pattern Search statistics dialogs, fixed tsumego solution navigation, kept SRS reviews independent when My Mistakes entries are cleared or ignored, and refreshed the app icon and About-page acknowledgements.
- Improved KataGo candidate-PV hover responsiveness and made shortcut focus checks safe during page disposal; completed and corrected German, Spanish, Italian, Romanian, Russian, Ukrainian, and Chinese localization coverage.

## 0.2.5+67
- Joseki page in Train, including about 5,000 bundled variations, pass/tenuki branches, a readable corner board, linked comments, cleaned labels/source data, and debug-only source-saving tools.
- Improved SRS review with neutral cancellation, speed-based scheduling, short failed-review retries, capped intervals, and 5-correct graduation.
- Improved Pattern Search and Pattern Management with better selected-area search, imports/indexing/rebuild progress, search history, position statistics, metadata repair/normalising summaries, duplicate handling, and safer maintenance.
- Rebuilt KataGo Page with a modular SWHub-style analysis/play UI, themed controls, persisted panels, local/alternate/remote engine setup, hardware-aware Auto Setup, modest b18/b28 model downloads, manual OpenCL choice, and a Colab notebook.
- Expanded KataGo study/play with human-rank heatmaps, aligned analysis overlays, full-game reanalysis, Tsumego Frame, timers, AI styles, and a sortable/filterable Performance Report mistakes tab.
- Added Game Tsumegos from KataGo analysis, with manual position saves, bulk mistake-position saves, tags/notes, a Home list view, board previews, filtering/sorting, multi-select delete, and playable PV review.
- Added Career Mode under Play, with ranked KataGo human-model games, Fox-style rank windows, rank history/peak tracking, post-game review, Career SGF saves, and stronger-rank teaching practice with auto-undo.
- Improved SGF workflows with SGF/GIB/NGF import from picker, drag/drop, clipboard, file association, save/save-as/copy, folder favorites, metadata/notes preservation, analysis feedback export, Linux/AppImage thumbnails, and single-instance desktop file opening.
- Standardized desktop-generated files under `Documents/SWHub`, refined board/task visuals and SGF/game-tree handling, refreshed FAQ/localization coverage, cleaned legacy code/assets, and added focused SRS, Pattern Search, KataGo, SGF, and game-record tests.

## 0.2.41
- Added Teaching Rooms from Play, with live shared boards, room chat/voice, teacher/student roles, and turn-based student move assignment.
- Expanded SGF tools with connected-group liberty counts, dynamic smiley status markers, group marker toggles, and theme-aware move icons.
- Added one-at-a-time student voice permission in Teaching Rooms, so a teacher can let one student speak alongside the teacher broadcast while everyone hears both.
- Added optional Teaching Room passwords for protected room entry.
- Improved pen drawing cursor tracking of sgf tools.
- Added Smiley and Liberties SGF Tool Markers.

## 0.2.4
- Added automatic stats and leaderboard sync, including sync-key credential handling and safer stats export.
- Improved leaderboard history, period/category reporting, and merge support for exams and leaderboard attempts.
- Reworked the desktop KataGo page with a stronger review UI, improved analysis controls, player setup, timers, and SGF save fixes.
- Kept desktop KataGo out of Android builds while preserving cloud katago on all platforms.
- Added SRS graduation counting and fixed SRS, tsumego variation, Ghost Mode, and server scoring issues.
- Made SGF Management available from Home on all supported platforms and restricted task management to debug/developer mode.
- Improved local board page to have more sgf editing options, and fixed the visual game tree looks.
- Updated FAQ content and refreshed/fixed task database content.

## 0.2.3
- Added SSGS multiplayer rooms with invitations, team games, Rengo-style play, One Color Go, Traitor Go, Blind Go, and Phantom Go variants.
- Improved SSGS scoring sync with host-only counting controls, synchronized manual dead-stone marking, full ownership-map transmission, and reset of scoring acceptance state.
- Added byo-yomi period management and timeout handling to the SWHub/SSGS server.
- Fixed SSGS and Traitor variant desync/reconnection issues, including state redaction and client-side reconciliation.
- Added "solve all correct variations" support for tsumego, with follow-up fixes for multi-variation solving.
- Fixed Ghost Mode so initial stones stay visible and unrelated/random stones do not appear.
- Fixed SRS-related issues and refreshed/fixed task data, including Diabolical warm-up answers.
- Made SGF Management available on all supported platforms while keeping task management developer-only/debug-only.
- Cleaned up OGS-related code and added a robust portable Windows build workflow.
- Improved sync-related behavior and updated the FAQ.

## 0.2.2
- Added the Me page with profile-style stats, sharing, unique solved tracking, and a GitHub-style training heatmap.
- Added global leaderboards for training modes, with period filters and duplicate-username handling.
- Added stats persistence/sync improvements and safeguards against stats loss on upgrade.
- Added more stone sound options.
- Added Diabolical tsumego placeholders and initial Diabolical task data.
- Improved local-board scoring mode and leaderboard reporting.
- Cleaned up localization files and fixed black-screen/startup issues.

## 0.2.1
- Added Pattern Search exploration improvements, Guess mode support, score estimation, and a fuller-height search layout.
- Added position statistics dialogs with histograms, dynamic date ranges, winrate charts, and improved continuation displays.
- Improved Pattern Search and Pattern Management pages, including duplicate detection robustness, metadata display, player names, and sidebar summaries.
- Modernized and optimized libkombilo with C++17 support, binary caching, faster startup/loading, and safety/UX fixes. Plus fixed a lot of libkombilo TODO & bugs.
- Fixed Pattern Search import crashes, handicap-game discovery, metadata filtering, continuation disappearance, and hidden-coordinate board padding.
- Improved leaderboard periods and histogram behavior.

## 0.2.0
- Optimized SGF Management and Pattern Management, including faster rank filtering and better metadata handling.
- Renamed the local server/client flow to SSGS and fixed duplicate users in the SSGS lobby.
- Added the FAQ page in Settings, Esc shortcut support, board mouse-scroll navigation, and broader keyboard shortcut coverage.
- Improved Pattern Search database import/export and added Ctrl+S shortcut support.
- Added new/updated collections, synced puzzle databases, and added placeholder Diabolical collection content.
- Added many status/count tasks, including 9x9, 13x13, and 19x19 count tasks.
- Fixed task reset interactivity, Ghost Mode behavior, and ghost stone shadows.
- Added auto-next for ranked mode and collections.
- Consolidated user data files into the SWHub folder on desktop.
- Updated FAQ/about text and Android workflow cleanup.

## 0.1.16
- 294 Status type tasks added
- 391 Count type tasks added
- Ghost Mode in Task Attempts
- Randomize Task Colors
- Block Stone Placements in Count & Status by default
- Count Hard Mode
- New Collection
- Added/updated count task rank ranges and task database content.
- Improved behavior around status/count task variations.

## 0.1.15
- Added Simple Go Server support, later renamed/refined as SSGS.
- Added custom board cursor assets and cursor settings.
- Added stone scaling support.
- Added fuzzy stone placement for more realistic stone positions.
- Added wiggle animation when placing stones.
- Added the new Status and Count task types.
- Improved Local Board behavior and fixed Local Board page issues.
- Fixed board preview updates in Appearance settings.
- Improved board line/stone rendering to support the new placement and scaling options.

## 0.1.14
- Added P2P Tsumego Battle support with lobby/rematch fixes, timer fixes, presence/resumption improvements, and updated worker configuration.
- Added the first Pattern Search workflow, including Guess Mode groundwork, crash fixes, and TODO cleanup.
- Added developer Task Management improvements, including recursive SGF folder import, collection filtering, bulk rank/type/tag assignment, default branch status fixes, bulk delete, and automatic SGF rank assignment.
- Added SRS review for mistakes, with dedicated SRS/mistakes tables, detailed SRS page, ETA/count-up timer, solution navigation, and robust database initialization.
- Added status and count task types, static-position conversion, sidebar answer highlights, custom rank ranges/topics, and related SRS/attempt tracking fixes.
- Improved Local Board and task editor with Japanese score estimation, dead-stone detection, variation persistence, tree-view visibility, and visual feedback.
- Added mouse-scroll board navigation, auto-next/auto-remove-mistakes behavior, and decoupled task sidebar work.
- Improved board/server performance and time synchronization.

## 0.1.13 : The SADGE update
- add timeout problems to exam review and stats (@Cidragon)
- add more Collections
- remove Topic feature
- removed about 134815 tsumegos
- Start of SWHub Public

## 0.1.12
- Ukrainian localization (@vabue)
- OGS: fix bug where correspondence games would be resumed (@benjaminpjones)
- OGS: fix byoyomi update bug (@benjaminpjones)
- improve login error descriptions (@benjaminpjones)
- set iOS app audio as background to avoid interruptions (@adudenamedruby)
- persist local board state on shared preferences
- add exam and task type charts to statistics
- fix: task title overflow
- add result page for exams and collections
- add Custom Exam presets
- improve selection granularity of task topics
- add setting for hiding players' rank (@adudenamedruby)
- add fullscreen setting for mobile platforms

## 0.1.11
- OGS support (@benjaminpjones)
- add setting to track Time Frenzy mistakes (@hemme)
- add option to copy task SGF (@hemme)
- accessibility: add setting to show wrong moves as crosses (@hemme)
- Italian localization (@hemme)
- Romanian localization (@adudenamedruby)
- German localization (@StHagel, @InfoKendoKing)
- next task can be triggered with a swipe gesture where applicable
- add setting for randomizing task orientation (@hemme)

## 0.1.10
- now available in Chinese (simplified), Russian and Spanish
- add task search by pattern
- add help dialogs for several pages
- show current rank for each topic
- fix topic progress display bug when returning to topic page
- fix timezone bug in statistics
- new theme: BadukTV
- remove experimental 9x9 human-like AI bot 
- remove a few broken tasks
- Start of SWHub Private

## 0.1.9
- add Next button for topic exams 
- fix: redo button bug on custom exams
- fix: disable start custom exam if there are no tasks available
- fix: custom exam reports more mistakes than available
- fix many broken tasks
- improve overall routing/navigation
- improve statistics page: daily/weekly/monthly stats
- new themes by Pumu
- experimental: 9x9 human-like AI bot 
- improved sound settings

## 0.1.8
- add file picker dialog to save games on desktop
- add task topics
- fix: starting a collection warns about ongoing sessions
- fix: collections page refreshes after exiting current session
- add mode to try custom moves in tasks
- add Custom Exam mode
- fix several broken tasks

## 0.1.7
- hotfix for Windows game downloads

## 0.1.6
- add My Mistakes page
- add Collections page
- download games to Downloads directory on all desktop platforms
- fix several broken tasks
- fix always-black-to-play setting
- fix broken game sharing on iPad
- fix missing last-move annotation when rejoining game
- fix receiving counting requests from opponents on foxwq
- improve disconnection handling on mobile platforms
- display player online status during games

## 0.1.5
- fix several broken tasks
- add Endgame Exam mode
- add setting to set all tasks as black-to-play
- add task share link and Find Task mode
- improved stone assets (thanks @Eraleis!)
- save SGF from local board
- improve download and parsing of Fox games

## 0.1.4
- fix several broken and duplicated tasks
- update Tygem automatch presets to match the official client
- add Windows VS Redistributable files to installer
- make downloading games more responsive
- use an older GitHub runner for Linux builds (based on Ubuntu 22.04)

## 0.1.3
- remove Register button for iOS and MacOS due to Apple guidelines
- logout support
- add button to show task continuations (correct and wrong variations)

## 0.1.2
- recent results and rank up/down requirements
- refresh game record automatically after games
- fix: refresh issue caused opponent's move to not show up on ranked mode
- add board navigation keyboard shortcuts
- fix: rank display issue in ranked mode
- clear ghost stone when tapping a occupied point
- add buttons to redo and go to next rank grading exam

## 0.1.1
- game list, download and AI Sensei sharing
- grading exam result now shows the average time per task as well
- add a task solving response delay setting
- fix: grading exam counts as failed when exiting in the middle of it
- fix: remove ghost stone from captured stones
- fix: do not spam result banner after solving a task
- relax disconnection threshold for foxwq

## 0.1.0+3

- fix: show hovering stone only when it's your turn during games
- fix: result banner doesn't get in the middle of the next button in wide layout
- settings page refactored into separate sections
- add setting to confirm moves on large boards to avoid misclicks on small screens
