openitg-assets
--------------

This repo stores static assets for OpenITG builds, such as game and patch data.
If you need to change theme data, please do it in either 'patch-data' (for all
releases) or 'game-data-home' (for PC releases specifically).

In general, this should be used as a supplement to 'openitg-utils'; let those
scripts work with it instead of working with the data yourself.

Directory layout
----------------

arcade-patch-template: contains supporting data for arcade patches (X config,
	startup scripts, kernel modules, patch.xml template). Do not use this
	directly; it's used by some utils to generate full patches.

game-data-base: contains engine data from the ITG game drive (theme, noteskins,
	supporting data). Do *not* modify this data: we need it to produce
	consistent patches across all platforms. If something here needs
	modified, override it within 'patch-data'.

game-data-home: contains supporting data for OpenITG home releases (the 'home'
	theme, supporting data). This is used exclusively for home releases.
	Modify it as you like.

patch-data: contains OpenITG-specific overrides for 'game-data-base', which are
	common to all releases. Modify it as you like, but if you're building
	a patch, use the scripts in openitg-utils; don't build directly here.
