## PHPTAL / Ztal Sublime Text Package

*Note*: This plugin has not been tested under all operating systems. It's really quite basic so at a guess I'd say it'll work. However if you discover a problem please [file an issue][1].


### Installation

Manually:

 - Clone or [download git repo][2] into your packages folder (If you are unsure where this is, in Sublime Text use the 'Browse Packages' menu item to open this folder).
 - Restart Sublime Text editor

With Package Control:

 - Coming soon!

---

### File types
This package's tmLanguage file is set to work with xhtml, tmpl and tpl files. If for some reason Sublime doesn't honor this you can force it by opening a file of type and choosing 'Open all with current extension as...' from the syntax selector at bottom right of window.

### Theme Highlighting
This package creates a new set of scopes for theming which, as of now, no theme supports. The easiest way to solve this is to open which ever theme you are using (.tmTheme) and add the following:

	<dict>
		<key>name</key>
		<string>PHPTAL Block</string>
		<key>scope</key>
		<string>block.phptal</string>
		<key>settings</key>
		<dict>
			<key>foreground</key>
			<string>#D6769B</string>
		</dict>
	</dict>
	<dict>
		<key>name</key>
		<string>PHPTAL Attribute</string>
		<key>scope</key>
		<string>attribute.phptal</string>
		<key>settings</key>
		<dict>
			<key>foreground</key>
			<string>#D6769B</string>
		</dict>
	</dict>
	<dict>
		<key>name</key>
		<string>PHPTAL String</string>
		<key>scope</key>
		<string>string.phptal</string>
		<key>settings</key>
		<dict>
			<key>foreground</key>
			<string>#E88156</string>
		</dict>
	</dict>
	<dict>
		<key>name</key>
		<string>PHPTAL Variable</string>
		<key>scope</key>
		<string>variable.phptal</string>
		<key>settings</key>
		<dict>
			<key>foreground</key>
			<string>#E88156</string>
		</dict>
	</dict>
	<dict>
		<key>name</key>
		<string>PHPTAL Variable Reference</string>
		<key>scope</key>
		<string>variable.reference.phptal</string>
		<key>settings</key>
		<dict>
			<key>foreground</key>
			<string>#FF9C4C</string>
		</dict>
	</dict>
	<dict>
		<key>name</key>
		<string>PHPTAL Warning</string>
		<key>scope</key>
		<string>warning.phptal</string>
		<key>settings</key>
		<dict>
			<key>foreground</key>
			<string>#E83736</string>
			<key>fontStyle</key>
			<string> italic underline</string>
		</dict>
	</dict>


Once saved you should see that tal blocks, attributes, strings etc are now coloured differently to standard HTML.
(Feel free to change the colours to suit your theme!)

### Snippets
This package is basically a vast collection of snippets to aid template coding with PHPTAL / zTal. I've separated them out based on the documentation. Typing either 'tal_' or 'ztal_' will open the auto complete where you can browse the various snippets available to you.

### Settings
By default the package will enable autocomplete whenever it encounters 'tal' or 'ztal'. It's set to a delay of 300ms to try and prevent it from unnecessarily opening.

If you find this annoying you can disable it by opening a template file in Sublime Text then going to Preferences -> Settings more -> Syntax Specific - User. A new file will open. Pasting the following then saving the file will override the defaults.

		{
			"auto_complete": false
		}

If you find anything that's broken or you think something is missing - [file an issue][1].


  [1]: https://github.com/jackw/phptal-sublime/issues
  [2]: https://github.com/jackw/phptal-sublime/archive/master.zip