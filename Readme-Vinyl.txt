Added a new mvSQL mode:

1. clone locally
2. go to tools/
3. run `npm install`
4. run `node add_mode.js mvsql "sql|^MvSQL"`

To change it edit the following files

* lib/ace/mode/mvsql.js (set the fold mode, highlights, .. to be used)
* lib/ace/mode/mvsql_highlight_rules.js (defines the highlight rules)
* lib/ace/snippets/mvsql.js (loads the static snippets)
* lib/ace/snippets/mvsql.snippets (defines the static snippets)

Additional files
* demo/kitchen-sink/docs/mvsql.sql (just a simple example to be used by the demo page)
* lib/ace/ext/modelist.js (lists all modes, used if the user can pick them at will)

Once the changes have been done, to publish:

1. back at the root folder
2. run `npm install`
3. run `node Makefile.dryice.js -nc -m` (-nc for no-conflict mode, -m for minified)

The generated files will be under build/src-noconfict, of interest
* mode-mvsql.js (the actual mode)
* snippets/mvsql.js (the static snippets)

these will also be updated (to add mvSQL as an option), if they are needed:
* ext-settings_menu.js
* ext-promt.js
* ext-options.js
* ext-modelist.js