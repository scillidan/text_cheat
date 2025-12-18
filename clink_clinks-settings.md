## [Clink Settings](https://chrisant996.github.io/clink/clink.html#clinksettings)

- `argmatcher.show_hints` True  
	When both the [`comment_row.show_hints`](https://chrisant996.github.io/clink/clink.html#saved-command-history#comment_row_show_hints) and `argmatcher.show_hints` settings are enabled, [argmatchers](https://chrisant996.github.io/clink/clink.html#saved-command-history#argumentcompletion) can show usage hints in the comment row (below the input line).
- `autosuggest.async` True  
	When this is `true` matches are generated asynchronously for suggestions. This helps to keep typing responsive.
- `autosuggest.enable` True  
	When this is `true` a suggested command may appear in [`color.suggestion`](https://chrisant996.github.io/clink/clink.html#saved-command-history#color_suggestion) color after the cursor. If the suggestion isn't what you want, just ignore it. Or insert the whole suggestion with the Right arrow or End key, insert the next word of the suggestion with Ctrl\-Right, or insert the next full word of the suggestion up to a space with Shift\-Right. The [`autosuggest.strategy`](https://chrisant996.github.io/clink/clink.html#saved-command-history#autosuggest_strategy) setting determines how a suggestion is chosen.
- `autosuggest.hint` True  
	The default is `true`. When this and [`autosuggest.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#autosuggest_enable) are both `true` and a suggestion is available, show a right-aligned usage hint to help make the feature more discoverable and easy to use (`Right=Insert Suggestion` or `Right=Insert F2=List` etc). Set this to `false` to hide the usage hint.
- `autosuggest.original_case` True  
	When this is enabled (the default), inserting a suggestion uses the original capitalization from the suggestion.
- `autosuggest.strategy` `match_prev_cmd history completion`  
	This determines how suggestions are chosen. The suggestion generators are tried in the order listed, until one provides a suggestion. There are three built-in suggestion generators, and scripts can provide new ones. `history` chooses the most recent matching command from the history. `completion` chooses the first of the matching completions. `match_prev_cmd` chooses the most recent matching command whose preceding history entry matches the most recently invoked command, but only when the [`history.dupe_mode`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_dupe_mode) setting is `add`.
- `clink.autostart` `\`  
	This command is automatically run when the first CMD prompt is shown after Clink is injected. If this is blank (the default), then Clink instead looks for `clink_start.cmd` in the binaries directory and profile directory and runs them. Set it to "nul" to not run any autostart command.
- `clink.autoupdate` `check`  
	Clink can periodically check for updates for the Clink program files (see [Automatic Updates](https://chrisant996.github.io/clink/clink.html#saved-command-history#automatic-updates)).
- `clink.colorize_input`  
	True Enables context sensitive coloring for the input text (see [Coloring the Input Text](https://chrisant996.github.io/clink/clink.html#saved-command-history#classifywords)).
- `clink.customprompt` `\`  
	\*.clinkprompt files contain customizations for the prompt. Setting this to the name of a .clinkprompt file causes it to be loaded and used for displaying the prompt (see [Customizing the Prompt](https://chrisant996.github.io/clink/clink.html#saved-command-history#customisingtheprompt)).
- `clink.default_bindings` `bash` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	When this is `bash` (the default), Clink uses bash key bindings and does not match leading dots unless typed (completion does not match `.foo` when `f` is typed).  
	When this is `windows`, Clink overrides some of the bash defaults with familiar Windows key bindings for Tab, Ctrl\-A, Ctrl\-F, Ctrl\-M, and Right, and also Clink mimics the CMD completion behavior where completion matches `.foo` when just `f` is typed (that can also be controlled with the [match-hidden-files](https://chrisant996.github.io/clink/clink.html#saved-command-history#configmatchhiddenfiles) configuration variable in the [.inputrc](https://chrisant996.github.io/clink/clink.html#saved-command-history#init-file) file).
- `clink.logo` `full`  
	Controls what startup logo to show when Clink is injected. `full` = show full copyright logo, `short` = show abbreviated version info, `none` = omit the logo.
- `clink.max_input_rows` `0`  
	Limits how many rows the input line can use, up to the terminal height. When this is `0` (the default), the terminal height is the limit.
- `clink.paste_crlf` `crlf`  
	What to do with CR and LF characters on paste. Setting this to `delete` deletes them, `space` replaces them with spaces, `ampersand` replaces them with ampersands, and `crlf` pastes them as-is (executing commands that end with a newline).
- `clink.path` `\`  
	A list of paths from which to load Lua scripts. Multiple paths can be delimited semicolons.
- `clink.popup_delete_direction` `down`  
	When this is `down` (the default), deleting an entry in a popup list moves the selection down (repeated deletions delete downwards). When this is `up`, deleting an entry in a popup list moves the selection up (repeated deletions delete upwards).
- `clink.popup_search_mode` `find`  
	When this is `find`, typing in popup lists moves to the next matching item. When this is `filter`, typing in popup lists filters the list.
- `clink.promptfilter` True  
	Enable [prompt filtering](https://chrisant996.github.io/clink/clink.html#saved-command-history#customising-the-prompt) by Lua scripts.
- `clink.scroll_offset` `3`  
	Number of screen lines to show above or below a selected item in popup lists or the [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) command. The list scrolls up or down as needed to maintain the scroll offset (except after a mouse click).
- `clink.update_interval` `5`  
	The Clink autoupdater will wait this many days between update checks (see [Automatic Updates](https://chrisant996.github.io/clink/clink.html#saved-command-history#automatic-updates)).
- `cmd.admin_title_prefix` `\`  
	When set, this replaces the "Administrator: " console title prefix.
- `cmd.altf4_exits` True  
	When set, pressing Alt\-F4 exits the cmd.exe process.
- `cmd.auto_answer` `off`  
	Automatically answers cmd.exe's "Terminate batch job (Y/N)?" prompts. `off` = disabled, `answer_yes` = answer Y, `answer_no` = answer N.
- `cmd.ctrld_exits` True [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Ctrl\-D exits the cmd.exe process when it is pressed on an empty line.
- `cmd.get_errorlevel` True  
	When this is enabled, Clink runs a hidden `echo %errorlevel%` command before each interactive input prompt to retrieve the last exit code for use by Lua scripts. If you experience problems, try turning this off. This is on by default.
- `color.arg` `\`  
	The color for arguments in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.arginfo` `yellow` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Argument info color. Some argmatchers may show that some flags or arguments accept additional arguments, when listing possible completions. This color is used for those additional arguments. (E.g. the "dir" in a "-x dir" listed completion.)
- `color.argmatcher` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for the command name in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled, if the command name has an argmatcher available.
- `color.cmd` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Used when displaying shell (CMD.EXE) command completions, and in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.cmdredir` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for redirection symbols (`<`, `>`, `>&`) in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.cmdsep` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for command separators (`&`, `|`) in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.comment_row` `bright white on cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for the comment row. During [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) the comment row shows the "and _N_ more matches" or "rows _X_ to _Y_ of _Z_" messages. It can also show how history expansion will be applied at the cursor.
- `color.common_match_prefix` `\`  
	Used when displaying a prefix that all match completions have in common. This can be superseded by [Completion Colors](https://chrisant996.github.io/clink/clink.html#saved-command-history#completioncolors).
- `color.description` `bright cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Used when displaying descriptions for match completions.
- `color.doskey` `bright cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Used when displaying doskey alias completions, and in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.executable` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	When set, this is the color in the input line for a command word that is recognized as an executable file when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.filtered` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The default color for filtered completions (see [Filtering the Match Display](https://chrisant996.github.io/clink/clink.html#saved-command-history#filteringthematchdisplay)).
- `color.flag` `default` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for flags in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.hidden` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Used when displaying file completions with the "hidden" attribute.
- `color.histexpand` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for history expansions in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled. If this color is not set or [`history.auto_expand`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_auto_expand) is disabled or [`history.expand_mode`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_expand_mode) is off, then history expansions are not colored.
- `color.horizscroll` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for the `<` or `>` horizontal scroll indicators when Readline's [`horizontal-scroll-mode`](https://chrisant996.github.io/clink/clink.html#saved-command-history#confighorizontalscrollmode) variable is set.
- `color.input` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for input line text. Note that when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is disabled, the entire input line is displayed using `color.input`.
- `color.interact` `bold`  
	The color for prompts such as a pager's `--More?--` prompt.
- `color.message` `default`  
	The color for the message area (e.g. the search prompt message, digit argument prompt message, etc).
- `color.modmark` `\`  
	The color for the modified history line mark character.
- `color.popup` `\`  
	When set, this is used as the color for popup lists and messages. If no color is set, then the console's popup colors are used (see the Properties dialog box for the console window).
- `color.popup_border` `\`  
	When set, this is used as the color popup list borders. If no color is set, then the color from `color.popup` is used.
- `color.popup_desc` `\`  
	When set, this is used as the color for description column(s) in popup lists. If no color is set, then a color is chosen to complement the console's popup colors (see the Properties dialog box for the console window).
- `color.popup_footer` `\`  
	When set, this is used as the color for popup list footer message text. If no color is set, then the color from `color.popup_border` is used.
- `color.popup_header` `\`  
	When set, this is used as the color for popup list title text. If no color is set, then the color from `color.popup_border` is used.
- `color.popup_select` `\`  
	When set, this is used as the color for the selected popup list item. If no color is set, a color is chosen by swapping the foreground and background colors from `color.popup`.
- `color.popup_selectdesc` `\`  
	When set, this is used as the color for the selected popup list item's description text. If no color is set, a color is chosen by swapping the foreground and background colors from `color.popup`.
- `color.prompt` `\`  
	When set, this is used as the default color for the prompt. But it's overridden by any colors set by [Customizing The Prompt](https://chrisant996.github.io/clink/clink.html#saved-command-history#customisingtheprompt).
- `color.readonly` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Used when displaying file completions with the "readonly" attribute.
- `color.selected_completion` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for the selected completion with the [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) command. If no color is set, then reverse video is used.
- `color.selection` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for selected text in the input line (for example, when using Shift\-Arrow keys). If no color is set, then reverse video is used.
- `color.suggestion` `bright black` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for automatic suggestions when [`autosuggest.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#autosuggest_enable) is enabled.
- `color.suggestionlist` `\`  
	The color for suggestions in the [suggestion list](https://chrisant996.github.io/clink/clink.html#saved-command-history#suggestion-list).
- `color.suggestionlist_dim` `bright black` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for dim text in the suggestion list's header.
- `color.suggestionlist_highlight` `bright cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for highlighting the matching part of the suggestions. For the selected suggestion, this is combined with `color.suggestionlist_selected`.
- `color.suggestionlist_markup` `yellow` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for markup in the suggestion list, in the header and at the beginning and end of each suggestion item. For the selected suggestion, this is combined with `color.suggestionlist_selected`.
- `color.suggestionlist_selected` `default on bright black` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The color for the selected suggestion. This is combined with other suggestion list colors, so typically this should specify at least a background color.
- `color.unexpected` `default`  
	The color for unexpected arguments in the input line when [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) is enabled.
- `color.unrecognized` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	When set, this is the color in the input line for a command word that is not recognized as a command, doskey macro, directory, argmatcher, or executable file.
- `comment_row.hint_delay` `500`  
	Specifies a delay in milliseconds before showing input hints (see [Showing Input Hints](https://chrisant996.github.io/clink/clink.html#saved-command-history#showinginputhints)). The delay can be up to 3000 milliseconds, or 0 for no delay.
- `comment_row.show_hints` False  
	Allow showing input hints in the comment row (see [Showing Input Hints](https://chrisant996.github.io/clink/clink.html#saved-command-history#showinginputhints)).
- `debug.log_output_callstacks` False  
	Include callstack when logging output. This has no effect unless `debug.log_terminal` is enabled. This is intended for diagnostic purposes only, and can make the log file grow significantly.
- `debug.log_prompt` False  
	Logs the raw prompt string generated by prompt filters to the clink.log file. This is intended for diagnostic purposes only, and can make the log file grow significantly.
- `debug.log_terminal` False  
	Logs all terminal input and output to the clink.log file. This is intended for diagnostic purposes only, and can make the log file grow significantly.
- `directories.dupe_mode` `add`  
	Controls how the current directory history is updated. A value of `add` (the default) always adds the current directory to the directory history. A value of `erase_prev` will erase any previous entries for the current directory and then add it to the directory history. Note that directory history is not saved between sessions.
- `doskey.enhanced` True  
	Enhanced Doskey adds the expansion of macros that follow `|` and `&` command separators and respects quotes around words when parsing `$1`...`$9` tags. To suppress macro expansion for an individual command, prefix the command with a space or semicolon ( `foo` or `;foo`). Or following `|` or `&`, prefix with two spaces or a semicolon (`foo|  bar` or `foo|;bar`).
- `exec.aliases` True  
	When matching executables as the first word ([`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)), include doskey aliases.
- `exec.associations` False  
	When matching executables as the first word ([`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)), include files with a registered file association (e.g. launchable documents such as ".pdf" files).
- `exec.commands` True  
	When matching executables as the first word ([`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)), include CMD commands (such as `cd`, `copy`, `exit`, `for`, `if`, etc).
- `exec.cwd` True  
	When matching executables as the first word ([`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)), include executables in the current directory. (This is implicit if the word being completed is a relative path, or if [`exec.files`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_files) is true.)
- `exec.dirs` True  
	When matching executables as the first word ([`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)), also include directories relative to the current working directory as matches.
- `exec.enable` True Match executables when completing the first word of a line. Executables are determined by the extensions listed in the `%PATHEXT%` environment variable.
- `exec.files` False  
	When matching executables as the first word ([`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)), include files in the current directory.
- `exec.path` True  
	When matching executables as the first word ([`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)), include executables found in the directories specified in the `%PATH%` environment variable.
- `exec.space_prefix` True  
	If the line begins with whitespace then Clink bypasses executable matching ([`exec.path`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_path)) and will do normal files matching instead.
- `files.hidden` True  
	Includes or excludes files with the "hidden" attribute set when generating file lists.
- `files.system` False Includes or excludes files with the "system" attribute set when generating file lists.
- `history.auto_expand` True  
	When enabled, history expansion is automatically performed when a command line is accepted (by pressing Enter). When disabled, history expansion is performed only when a corresponding expansion command is used (such as [`clink-expand-history`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-expand-history) Alt\-^, or [`clink-expand-line`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-expand-line) Alt\-Ctrl\-E).
- `history.dont_add_to_history_cmds` `exit history`  
	List of commands that aren't automatically added to the history. Commands are separated by spaces, commas, or semicolons. Default is `exit history`, to exclude both of those commands.
- `history.dupe_mode` `erase_prev`  
	If a line is a duplicate of an existing history entry Clink will erase the duplicate when this is set to `erase_prev`. Setting it to `ignore` will not add duplicates to the history, and setting it to `add` will always add lines (except when overridden by [`history.sticky_search`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_sticky_search)).
- `history.expand_mode` `not_quoted`  
	The `!` character in an entered line can be interpreted to introduce words from the history. This can be enabled and disable by setting this value to `on` or `off`. Values of `not_squoted`, `not_dquoted`, or `not_quoted` will skip any `!` character quoted in single, double, or both quotes respectively.
- `history.ignore_space` True  
	Ignore lines that begin with whitespace when adding lines in to the history.
- `history.max_lines` 10000 [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	The number of history lines to save if [`history.save`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_save) is enabled (or 0 for unlimited).
- `history.save` True  
	Saves history between sessions. When disabled, history is neither read from nor written to a master history list; history for each session is written to a temporary file during the session, but is not added to the master history list.
- `history.shared` False  
	When history is shared, all instances of Clink update the master history list after each command and reload the master history list on each prompt. When history is not shared, each instance updates the master history list on exit.
- `history.show_preview` True  
	When enabled, if the text at the cursor is subject to history expansion, then this shows a preview of the expanded result below the input line using the [`color.comment_row`](https://chrisant996.github.io/clink/clink.html#saved-command-history#color_comment_row) setting.
- `history.sticky_search` False  
	When enabled, reusing a history line does not add the reused line to the end of the history, and it leaves the history search position on the reused line so next/prev history can continue from there (e.g. replaying commands via Up several times then Enter, Down, Enter, etc).
- `history.time_format` `%F %T`  
	This specifies a time format string for showing timestamps for history items. For a list of format specifiers see `clink set history.time_format` or [History Timestamps](https://chrisant996.github.io/clink/clink.html#saved-command-history#history-timestamps).
- `history.time_stamp` `off`  
	The default is `off`. When this is `save`, timestamps are saved for each history item but are only shown when the `--show-time` flag is used with the `history` command. When this is `show`, timestamps are saved for each history item, and timestamps are shown in the `history` command unless the `--bare` or `--no-show-time` flag is used.
- `lua.break_on_error` False  
	Breaks into Lua debugger on Lua errors.
- `lua.break_on_traceback` `\`  
	Breaks into Lua debugger on `traceback()`.
- `lua.debug` False  
	Loads a simple embedded command line debugger when enabled. Breakpoints can be added by calling [pause()](https://chrisant996.github.io/clink/clink.html#saved-command-history#pause).
- `lua.path` `\`  
	Value to append to the [`package.path`](https://www.lua.org/manual/5.2/manual.html#pdf-package.path) Lua variable. Used to search for Lua scripts specified in `require()` statements.
- `lua.strict` True  
	When enabled, argument errors cause Lua scripts to fail. This may expose bugs in some older scripts, causing them to fail where they used to succeed. In that case you can try turning this off, but please alert the script owner about the issue so they can fix the script.
- `lua.throttle_interval` `0`  
	Restricts coroutine execution. This is off (0) by default, which allows coroutines to freely control their own execution times and rates. If coroutines interfere with responsiveness, you can set this to a number that restricts how often (in seconds) a long-running coroutine can actually run. Until v1.7.17, the throttling interval was hard-coded 5 seconds, but now it's configurable and 0 by default (no throttling).
- `lua.traceback_on_error` False  
	Prints stack trace on Lua errors.
- `match.coloring_rules` `\`  
	Provides a series of color definitions used when displaying match completions. See [Completion Colors](https://chrisant996.github.io/clink/clink.html#saved-command-history#completioncolors) for details.
- `match.expand_abbrev` True  
	Expands an abbreviated path before performing completion. In an abbreviated path, directory names may be shortened to the minimum number of characters to unambiguously refer to a directory. For example, "c:\\Users\\chris\\Documents" could be abbreviated as "c:\\U\\c\\Do", depending on what directories exist in the file system.
- `match.expand_envvars` False [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	Expands environment variables in a word before performing completion.
- `match.fit_columns` True  
	When displaying match completions, this calculates column widths to fit as many as possible on the screen.
- `match.ignore_accent` True  
	Controls accent sensitivity when completing matches. For example, `ä` and `a` are considered equivalent with this enabled.
- `match.ignore_case` `relaxed`  
	Controls case sensitivity when completing matches. `off` = case sensitive, `on` = case insensitive, `relaxed` = case insensitive plus `-` and `_` are considered equal.
- `match.max_fitted_matches` `0`  
	When the [`match.fit_columns`](https://chrisant996.github.io/clink/clink.html#saved-command-history#match_fit_columns) setting is enabled, this disables calculating column widths when the number of matches exceeds this value. The default is 0 (unlimited). Depending on the screen width and CPU speed, setting a limit may avoid delays.
- `match.max_rows` `0`  
	The maximum number of rows of items [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) can show. When this is 0, the limit is the terminal height.
- `match.preview_rows` `0`  
	The number of rows to show as a preview when using the [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) command (bound by default to Ctrl\-Space). When this is 0, all rows are shown and if there are too many matches it instead prompts first like the [`complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-complete) command does. Otherwise it shows the specified number of rows as a preview without prompting, and it expands to show the full set of matches when the selection is moved past the preview rows.
- `match.sort_dirs` `with`  
	How to sort matching directory names. `before` = before files, `with` = with files, `after` = after files.
- `match.substring` False [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	When set, if no completions are found with a prefix search, then a substring search is used.
- `match.translate_slashes` `auto`  
	File and directory completions can be translated to use consistent slashes. The default is `auto` which translates all slashes in the completed word to match the first kind of slash in the word (or the system path separator if the word didn't have any slashes before being completed). Use `slash` for forward slashes, `backslash` for backslashes, or `system` for the appropriate path separator for the OS host (backslashes on Windows). Use `off` to turn off translating slashes.
- `match.wild` True  
	Matches `?` and `*` wildcards when using any of the completion commands. Turn this off to behave how bash does, and not match wildcards (but [`glob-complete-word`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-glob-complete-word) always matches wildcards).
- `prompt.async` True  
	Enables [asynchronous prompt refresh](https://chrisant996.github.io/clink/clink.html#saved-command-history#asyncpromptfiltering). Turn this off if prompt filter refreshes are annoying or cause problems.
- `prompt.spacing` `normal`  
	The default is `normal` which never removes or adds blank lines. Set to `compact` to remove blank lines before the prompt, or set to `sparse` to remove blank lines and then add one blank line.
- `prompt.transient` `off`  
	Controls when past prompts are collapsed ([transient prompts](https://chrisant996.github.io/clink/clink.html#saved-command-history#transientprompts)). `off` = never collapse past prompts, `always` = always collapse past prompts, `same_dir` = only collapse past prompts when the current working directory hasn't changed since the last prompt.
- `readline.hide_stderr` False  
	Suppresses stderr from the Readline library. Enable this if Readline error messages are getting in the way.
- `suggestionlist.default` False  
	When this is true, a Clink session starts with the suggestion list enabled. The suggestion list can be toggled on/off with F2 or whatever key is bound to the [`clink-toggle-suggestion-list`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-toggle-suggestion-list) command.
- `terminal.adjust_cursor_style` True  
	When enabled, Clink adjusts the cursor shape and visibility to show Insert Mode, produce the visible bell effect, avoid disorienting cursor flicker, and to support ANSI escape codes that adjust the cursor shape and visibility. But it interferes with the Windows 10 Cursor Shape console setting. You can make the Cursor Shape setting work by disabling this Clink setting (and the features this provides).
- `terminal.color_emoji` `auto`  
	Set this to indicate whether the terminal program draws emojis using colored double width characters. This needs to be set accurately in order for Clink to display the input line properly when it contains emoji characters. When set to `off` Clink assumes emojis are rendered using 1 character cell. When set to `on` Clink assumes emojis are rendered using 2 character cells. When set to `auto` (the default) Clink tries to predict how emojis will be rendered based on OS version and terminal program.
- `terminal.differentiate_keys` False  
	When enabled, pressing Ctrl\-H or I or M or \[ generate special key sequences to enable binding them separately from Backspace or Tab or Enter or Esc.
- `terminal.east_asian_ambiguous` `auto`  
	There is a group of East Asian characters whose widths are ambiguous in the Unicode standard. This setting controls how to resolve the ambiguous widths. By default this is set to `auto`, but some terminal hosts may require setting this to a different value to work around limitations in the terminal hosts. Setting this to `font` measures the East Asian Ambiguous character widths using the current font. Setting it to `one` uses 1 as the width, or `two` uses 2 as the width. When this is 'auto' (the default) and the current code page is 932, 936, 949, or 950 then it tries to automatically measure the width based on which terminal host and font are used, or for any other code pages (including UTF8) it uses 1 as the width. The `%CLINK_EAST_ASIAN_AMBIGUOUS%` environment variable overrides this setting.
- `terminal.emulation` `auto`  
	Clink can either emulate a virtual terminal and handle ANSI escape codes itself, or let the console host natively handle ANSI escape codes. `native` = pass output directly to the console host process, `emulate` = clink handles ANSI escape codes itself, `auto` = emulate except when running in ConEmu, Windows Terminal, WezTerm, or Windows 10 new console.  
	This is superseded by [`%CLINK_ANSI_HOST%`](https://chrisant996.github.io/clink/clink.html#saved-command-history#override-terminal-detection) if set.
- `terminal.mouse_input` `auto`  
	Clink can optionally respond to mouse input, instead of letting the terminal respond to mouse input (e.g. to select text on the screen). When mouse input is enabled in Clink, clicking in the input line sets the cursor position, and clicking in popup lists selects an item, etc. Setting this to `off` lets the terminal host handle mouse input, `on` lets Clink handle mouse input, and `auto` lets Clink handle mouse input in ConEmu and in the default Conhost terminal when Quick Edit mode is unchecked in the console Properties dialog. For more information see [Mouse Input](https://chrisant996.github.io/clink/clink.html#saved-command-history#gettingstarted_mouseinput).
- `terminal.mouse_modifier` `\`  
	This selects which modifier keys (Alt, Ctrl, Shift) must be held in order for Clink to respond to mouse input when mouse input is enabled by the [`terminal.mouse_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#terminal_mouse_input) setting. This is a text string that can list one or more modifier keys: 'alt', 'ctrl', and 'shift'. For example, setting it to "alt shift" causes Clink to only respond to mouse input when both Alt and Shift are held (and not Ctrl). If the `%CLINK_MOUSE_MODIFIER%` environment variable is set then its value supersedes this setting. For more information see [Mouse Input](https://chrisant996.github.io/clink/clink.html#saved-command-history#gettingstarted_mouseinput).
- `terminal.raw_esc` False  
	When enabled, pressing Esc sends a literal escape character like in Unix or Linux terminals. This setting is disabled by default to provide a more predictable, reliable, and configurable input experience on Windows. Changing this only affects future Clink sessions, not the current session.
- `terminal.scrollbars` True  
	When enabled, lists show scrollbars using extended Unicode box drawing characters. Some terminals or fonts may be incompatible with this.
- `terminal.shell_integration` `auto`  
	Clink can send [shell integration codes](https://learn.microsoft.com/en-us/windows/terminal/tutorials/shell-integration) to the terminal, if the terminal supports them. When set to `off` Clink never sends shell integration codes. When set to `on` Clink always sends shell integration codes. When set to `auto` Clink only sends shell integration codes if it detects a terminal that is expected to support them.
- `terminal.use_altgr_substitute` False  
	Support Windows' Ctrl\-Alt substitute for AltGr. Turning this off may resolve collisions with Readline's key bindings.