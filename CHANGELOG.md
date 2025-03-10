# [2.13.0](https://github.com/atom-community/autocomplete-paths/compare/v2.12.19...v2.13.0) (2021-03-04)

- Build the path cache asynchronously without blocking the main thread -> Big projects no longer freeze Atom
- Build the cache in parallel (fast-glob uses threads underneath)
- Unified method for building the cache on all platforms
- Allows using glob for pattern ignoring which is the most common way of writing path patterns

### Bug Fixes

* _getGitIgnoreGlob ([84460f4](https://github.com/atom-community/autocomplete-paths/commit/84460f4750d2cb8bb16d4a88abee0eb11a2acb11))
* _getIgnoredPatternsGlob ([5ef1d7d](https://github.com/atom-community/autocomplete-paths/commit/5ef1d7d955444e5399bdd1082e3f32f3cfc03e47))
* get directoryPath as the input of _populateCacheFor ([38a9120](https://github.com/atom-community/autocomplete-paths/commit/38a9120e130177246b962f55d36ba0a09af22747))
* globifyDirectory ([896ecfc](https://github.com/atom-community/autocomplete-paths/commit/896ecfc8ef8f0bd1934cfb4f1ca61b42762be679))
* globifyGitIgnore ([170bf68](https://github.com/atom-community/autocomplete-paths/commit/170bf681f0435e408711cc69b346105ff478a792))
* globifyGitIgnoreFile ([2d76bf3](https://github.com/atom-community/autocomplete-paths/commit/2d76bf33a456cf23944b272b9aa2f9418351181a))
* globifyPath ([120eb16](https://github.com/atom-community/autocomplete-paths/commit/120eb16a155293adf643c3d7c16ffb123d3101de))
* install fast-glob ([c551bb8](https://github.com/atom-community/autocomplete-paths/commit/c551bb8cd87ed9f26cdd7996c813aeb36b5b2628))
* isGitIgnoreComment ([9717e0d](https://github.com/atom-community/autocomplete-paths/commit/9717e0db12d518f9ae0aa5f8969aeb40fbb7e7e5))
* isWhitespace ([a5a9dba](https://github.com/atom-community/autocomplete-paths/commit/a5a9dba9274bb04c73ef4dc84d7c71ac05a22d68))
* posixifyPath ([76c81f4](https://github.com/atom-community/autocomplete-paths/commit/76c81f4ea387be8d77cb3ccaeeba750ebe29d4a5))
* posixifyPathNormalized ([03f22b9](https://github.com/atom-community/autocomplete-paths/commit/03f22b92c5a9ccae671b102f531e8f48f885df33))
* prepend gitIgnoreDirectory before getting path type ([21cbdaf](https://github.com/atom-community/autocomplete-paths/commit/21cbdafedde3b3574d21b1e6138d662dc24e05ce))
* trimLeadingWhiteSpace ([5b48778](https://github.com/atom-community/autocomplete-paths/commit/5b487787f858ca50221abc951ffb0d565b9f2f9f))
* trimTrailingWhitespace ([fca9c11](https://github.com/atom-community/autocomplete-paths/commit/fca9c11e1a6d2b9ef0c23d209aab3311bd2f1644))
* trimWhiteSpace ([770a4e5](https://github.com/atom-community/autocomplete-paths/commit/770a4e5518142527a704a05ab21aee67a09528ff))
* use enum for PATH_TYPE ([9b35b4f](https://github.com/atom-community/autocomplete-paths/commit/9b35b4fa8ec555ec49dc77c7b481929fff4e44dd))


### Features

* git ignore to glob converter ([9873705](https://github.com/atom-community/autocomplete-paths/commit/987370531cd9356a9eb1ba54332c283564664db2))
* handle the patterns that are definitely a directory ([5779928](https://github.com/atom-community/autocomplete-paths/commit/5779928308eeea383f35facb025a081ba2f5573e))
* handle the patterns that are definitely a file ([6ed0a77](https://github.com/atom-community/autocomplete-paths/commit/6ed0a776c52460085efd983ee3b2b8d096cec3e6))
* use glob inside _onDirectoryChanged ([d89e176](https://github.com/atom-community/autocomplete-paths/commit/d89e1763a4aca5e3a32cd717e71813eae7b9fbb3))
* use glob to build the path cache ([307a695](https://github.com/atom-community/autocomplete-paths/commit/307a6959b6d6baff5278132fc675919ce933ecf9))

## [2.12.19](https://github.com/atom-community/autocomplete-paths/compare/v2.12.18...v2.12.19) (2021-03-03)


### Bug Fixes

* export entry functions named ([24f272a](https://github.com/atom-community/autocomplete-paths/commit/24f272a38bf82607014abb0712a798ef07b59e42))
* fix no case declaration ([0ccf198](https://github.com/atom-community/autocomplete-paths/commit/0ccf198b32a9fb45ad1328fd5105dd8e40a10a7f))
* use exec instead of spawn ([f7921ed](https://github.com/atom-community/autocomplete-paths/commit/f7921eda3ee9107e897b758f3ad4440f93c29017))
* use Object.keys for adding OptionScopes ([f386a00](https://github.com/atom-community/autocomplete-paths/commit/f386a003599aa978758e06605672123717f6338d))

## [2.12.18](https://github.com/atom-community/autocomplete-paths/compare/v2.12.17...v2.12.18) (2021-02-07)


### Bug Fixes

* bump zadeh to include the dist files ([1f1e9b5](https://github.com/atom-community/autocomplete-paths/commit/1f1e9b51b31320ea1b0148c6c288af2dd18578df))
* use zadeh library ([3ba7742](https://github.com/atom-community/autocomplete-paths/commit/3ba7742ee24b26e04a4421aca79ee48a77db62d5))

2.12.17 (Jan 24 2021)
===================
- Replace `await-spawn` with the native `exec` function
- Faster load time (the bundle size is half now.)

2.12.16 (Jan 23 2021)
===================
- Faster load time (tree shaking underscore)
* Bump dependencies


2.12.12 (November 24 2020)
===================

* Bump dependencies

2.12.12 (November 24 2020)
===================

* Include dist files

2.12.10 (November 24 2020)
===================

* Handle when a project is not git repository ([#239](https://github.com/atom-community/autocomplete-paths/pull/239))

2.12.9 (November 11 2020)
===================

* Entries filtering performance optimization ([#238](https://github.com/atom-community/autocomplete-paths/pull/238))

2.12.8 (November 11 2020)
===================

* Call the correct updateConfig

2.12.7 (November 11 2020)
===================

* General improvements (asyncify, Parcel, refactor, dead-code remove) ([#237](https://github.com/atom-community/autocomplete-paths/pull/237))

2.12.6 (November 10 2020)
===================

* Refactoring in default scopes ([#234](https://github.com/atom-community/autocomplete-paths/pull/234))
* Bump dependencies ([#236](https://github.com/atom-community/autocomplete-paths/pull/236))

2.12.5 (November 4 2020)
===================

* Add more extensions to HTML ([#197](https://github.com/atom-community/autocomplete-paths/pull/197))

2.12.4 (November 4 2020)
===================

* Update fuzzaldrin-plus-fast to 1.1.1 ([#232](https://github.com/atom-community/autocomplete-paths/pull/232))

2.12.3 (November 4 2020)
===================

* Add javascript to default scopes to support tree-sitter syntax ([#203](https://github.com/atom-community/autocomplete-paths/pull/203))
* Use native fuzzaldrin plus fast ([#230](https://github.com/atom-community/autocomplete-paths/pull/230))
* Add normalized slashes for projectRelativePath ([#226](https://github.com/atom-community/autocomplete-paths/pull/226))
* Add default woff2 extension support ([#180](https://github.com/atom-community/autocomplete-paths/pull/180))
* Do not display StatusBarTile if no provider ([#233](https://github.com/atom-community/autocomplete-paths/pull/233))
* Fix leftover interval timer ([#185](https://github.com/atom-community/autocomplete-paths/pull/185))

2.12.2 (January 9 2018)
===================

* Fixes less scope ([#198](https://github.com/atom-community/autocomplete-paths/pull/198)) - thanks [@guoshencheng](https://github.com/guoshencheng)

2.12.1 (October 13 2017)
===================

* Fixes uninitialized files - thanks [@avaly](https://github.com/avaly)

2.12.0 (October 9 2017)
===================

Thanks a lot to [@avaly](https://github.com/avaly) for the following contributions:

* Fixes support for switching projects
* Adds support for project-relative paths autocompletion
* Shows cache file count in status bar
* Adds a `ignoredPatterns` option that specifies ignored files
* Uses `find` system command if possible which improves performance
* Uses new file watcher API introduced in Atom 1.21.0

2.11.0 (September 3 2017)
===================

* Adds option for HTML autocompletion
* Fixes `replaceOnInsert` logic for requests that match multiple regexes
* Regards `core.excludeVcsIgnoredPaths` option
* Better support for `.vue` files. Splits CSS and JS handling into separate scopes.

2.10.1 (September 2 2017)
===================

* Adds option to ignore submodules

2.8.2 (September 1 2017)
===================

* Fixes memory leak in PathsCache which caused the `maximum file count` message after a couple
  of cache rebuilds

2.8.1 (August 24 2017)
===================

* Fixes memory leak in PathsCache, which now uses strings as keys instead of `Directory` instances
* Includes prefix config for unnamed ES6 imports
* Includes support for .vue files

2.8.0 (August 15 2017)
===================

* User scopes override default scopes now


2.7.0 (August 15 2017)
===================

* Actually stop indexing when cancelling due to maximum file count
* Hide status bar item when indexing has been cancelled

2.6.0 (August 14 2017)
===================

* Disabled directory watching / incremental builds for Windows, fixing freezes
* Fix `normalizeSlashes` option for Windows

2.5.0 (August 13 2017)
===================

* Support for `core.ignoreNames` option
* Fix `currentDirectory` handling

2.4.0 (August 12 2017)
===================

* Support for relative paths - now only suggests paths in the given directory (e.g. `./lib/`)
* Strip directory paths from suggestions, if possible

2.3.0 (August 12 2017)
===================

* Exposing provider's `suggestionPriority`

2.2.0 (August 12 2017)
===================

* Added a file limit that should fix application freezing

2.1.0 (August 11 2017)
===================

* Backwards slashes are now replaced with forward slashes in windows, if possible.
* Got rid of `readdirp` and `pathwatcher` dependencies. Instead, we are now using atom's
  integrated `pathwatcher` by using the exposed `Directory` and `File` classes. This also
  fixes installation issues on machines that don't have the necessary compilation tools
  installed
* Added support for coffeescript's `require ""` syntax

2.0.2 (August 11 2017)
===================

* Upgraded `fuzzaldrin-plus`, `readdirp` and `pathwatchers`, resulting in better
  cross-platform support and stability

2.0.1 (August 11 2017)
===================

* Avoid synchronous I/O with GitRepository
* Fix non-git projects

2.0.0 (August 11 2017)
===================

* Paths are now cached on startup or using the 'Rebuild Cache' command
* Cache is rebuilt incrementally when files are renamed / deleted / added
* autocomplete-paths now shows all relevant files, depending on the scope descriptor and prefix
* See [the default scopes](lib/config/default-scopes) for examples on how to define scopes

0.5.0 (May 10 2014)
===================

* Fixed path regex. ([#8](https://github.com/atom-community/autocomplete-paths/pull/8))

0.4.0 (May 8 2014)
==================

* Fixed path normalization

0.3.0 (May 8 2014)
==================

* Rewrote the whole plugin, fixed a lot of bugs

0.2.0 (Apr 11 2014)
===================

* Minor bugfix

0.1.0 (Apr 11 2014)
===================

* Initial release
