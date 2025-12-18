## [Clink设置](https://chrisant996.github.io/clink/clink.html#clinksettings)

- `argmatcher.show_hints` True  
	当 [`comment_row.show_hints`](https://chrisant996.github.io/clink/clink.html#saved-command-history#comment_row_show_hints) 和 `argmatcher.show_hints` 设置都启用时， [argmatchers](https://chrisant996.github.io/clink/clink.html#saved-command-history#argumentcompletion) 可以在注释行（输入行下方）显示使用提示。 
- `autosuggest.async` True  
	当此选项为`true`时，匹配项会异步生成以供建议。这有助于保持输入的响应性。 
- `autosuggest.enable` True  
	当此选项为`true`时，建议的命令可能会在光标后以 [`color.suggestion`](https://chrisant996.github.io/clink/clink.html#saved-command-history#color_suggestion) 颜色显示。如果建议不符合你的需求，可以忽略它。或者可以用右箭头或结束键插入整个建议，使用 Ctrl-右箭头插入建议的下一个单词，或使用 Shift-右箭头插入建议中到空格的下一个完整单词。 [`autosuggest.strategy`](https://chrisant996.github.io/clink/clink.html#saved-command-history#autosuggest_strategy) 设置确定如何选择建议。 
- `autosuggest.hint` True  
	默认为 `true`。当此选项和 [`autosuggest.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#autosuggest_enable) 都为 `true` 且有建议可用时，右对齐的使用提示将显示，以帮助用户更容易发现并使用此功能（`Right=Insert Suggestion` 或 `Right=Insert F2=List` 等）。将其设置为 `false` 以隐藏使用提示。 
- `autosuggest.original_case` True  
	当此选项启用（默认为启用）时，插入建议时使用建议的原始大小写。 
- `autosuggest.strategy` `match_prev_cmd history completion`  
	此选项确定如何选择建议。建议生成器将按列出的顺序尝试，直到其中之一提供建议。共有三个内置的建议生成器，脚本可以提供新的生成器。`history` 选择来自历史记录的最新匹配命令。`completion` 选择第一个匹配的完成项。`match_prev_cmd` 选择最近的匹配命令，其前一个历史条目与最新调用的命令匹配，但仅在 [`history.dupe_mode`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_dupe_mode) 设置为 `add` 时。 
- `clink.autostart` `\`  
	此命令会在 Clink 注入后首次显示 CMD 提示时自动运行。如果此选项为空（默认为空），则 Clink 会在二进制目录和配置文件目录查找 `clink_start.cmd` 并运行它们。设置为 "nul" 可禁止运行任何自启动命令。 
- `clink.autoupdate` `check`  
	Clink 可以定期检查 Clink 程序文件的更新（请参见 [自动更新](https://chrisant996.github.io/clink/clink.html#saved-command-history#automatic-updates)）。 
- `clink.colorize_input`  
	True 启用上下文敏感的输入文本着色（请参见 [着色输入文本](https://chrisant996.github.io/clink/clink.html#saved-command-history#classifywords)）。 
- `clink.customprompt` `\`  
	\*.clinkprompt 文件包含提示的自定义设置。将其设置为 .clinkprompt 文件的名称会导致加载并使用该文件来显示提示（请参见 [自定义提示](https://chrisant996.github.io/clink/clink.html#saved-command-history#customisingtheprompt)）。 
- `clink.default_bindings` `bash` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	当此选项为 `bash`（默认值）时，Clink 使用 bash 键绑定，并且不会匹配前导点，除非输入时输入。 （完成不会在键入 `f` 时匹配 `.foo`）。  
	当此选项为 `windows` 时，Clink 用熟悉的 Windows 键绑定覆盖一些 bash 默认设置，这包括 Tab、Ctrl-A、Ctrl-F、Ctrl-M 和右键，并且还模拟 CMD 完成行为，其中完成在仅输入 `f` 时匹配 `.foo`（这也可以通过 [`match-hidden-files`](https://chrisant996.github.io/clink/clink.html#saved-command-history#configmatchhiddenfiles) 配置变量在 [.inputrc](https://chrisant996.github.io/clink/clink.html#saved-command-history#init-file) 文件中进行控制）。 
- `clink.logo` `full`  
	控制在 Clink 被注入时显示什么启动标志。`full` = 显示完整版权标志，`short` = 显示简略版本信息，`none` = 忽略标志。 
- `clink.max_input_rows` `0`  
	限制输入行可以使用的行数，最大不超过终端高度。当此选项为 `0`（默认值）时，终端高度就是限制。 
- `clink.paste_crlf` `crlf`  
	粘贴时如何处理 CR 和 LF 字符。将此选项设置为 `delete` 会删除它们，将其设置为 `space` 会将它们替换为空格，将其设置为 `ampersand` 会将其替换为 &，设置为 `crlf` 会按原样粘贴（执行以换行符结束的命令）。 
- `clink.path` `\`  
	从中加载 Lua 脚本的路径列表。多个路径可以用分号分隔。 
- `clink.popup_delete_direction` `down`  
	当此选项为 `down`（默认值）时，删除弹出列表中的条目会将选择向下移动（重复删除会向下删除）。当此选项为 `up` 时，删除弹出列表中的条目会将选择向上移动（重复删除会向上删除）。 
- `clink.popup_search_mode` `find`  
	当此选项为 `find` 时，在弹出列表中输入会移动到下一个匹配项。 当此选项为 `filter` 时，在弹出列表中输入会过滤列表。 
- `clink.promptfilter` True  
	启用通过 Lua 脚本的 [提示过滤](https://chrisant996.github.io/clink/clink.html#saved-command-history#customising-the-prompt)。 
- `clink.scroll_offset` `3`  
	在弹出列表或 [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) 命令中，选择的项目上下方的屏幕行数。列表会根据需要向上或向下滚动以保持滚动偏移（鼠标单击后除外）。 
- `clink.update_interval` `5`  
	Clink 自动更新程序将在此选项指定的天数之后检查更新（请参见 [自动更新](https://chrisant996.github.io/clink/clink.html#saved-command-history#automatic-updates)）。 
- `cmd.admin_title_prefix` `\`  
	设置时，此选项会替换 "Administrator: " 控制台标题前缀。 
- `cmd.altf4_exits` True  
	设置此选项时，按 Alt-F4 将退出 cmd.exe 进程。 
- `cmd.auto_answer` `off`  
	自动回答 cmd.exe 的 "Terminate batch job (Y/N)?" 提示。`off` = 禁用，`answer_yes` = 回答 Y，`answer_no` = 回答 N。 
- `cmd.ctrld_exits` True [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在空行上按 Ctrl-D 时退出 cmd.exe 进程。 
- `cmd.get_errorlevel` True  
	当此选项启用时，Clink 会在每个交互输入提示前运行隐藏的 `echo %errorlevel%` 命令，以检索最后的退出代码，以供 Lua 脚本使用。如果遇到问题，可以尝试将此选项关闭。默认情况下开启此选项。 
- `color.arg` `\`  
	在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，输入行中参数的颜色。 
- `color.arginfo` `yellow` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	参数信息颜色。某些 argmatchers 可能会显示某些标志或参数接受其他参数，当列出可能的完成项时。此颜色用于这些额外参数。（例如，列出完成项时的 "-x dir" 中的 "dir"）。 
- `color.argmatcher` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，输入行中命令名称的颜色，仅当命令名称有可用的 argmatcher 时。 
- `color.cmd` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	用于显示 shell (CMD.EXE) 命令完成时的颜色，以及在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时的输入行颜色。 
- `color.cmdredir` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，输入行中重定向符号 (`<`, `>`, `>&`) 的颜色。 
- `color.cmdsep` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，输入行中命令分隔符 (`&`, `|`) 的颜色。 
- `color.comment_row` `bright white on cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	注释行的颜色。在 [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) 期间，注释行显示 "and _N_ more matches" 或 "rows _X_ to _Y_ of _Z_" 的消息。它还可以显示历史扩展将在光标处应用的方式。 
- `color.common_match_prefix` `\`  
	在显示所有匹配完成项时用于展示共享前缀的颜色。可以被 [完成颜色](https://chrisant996.github.io/clink/clink.html#saved-command-history#completioncolors) 覆盖。 
- `color.description` `bright cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在显示匹配完成项的描述时使用的颜色。 
- `color.doskey` `bright cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	用于显示 doskey 别名完成项的颜色，以及在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时的输入行颜色。 
- `color.executable` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	当设置时，此选项是识别为可执行文件的命令词的输入行颜色，当启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时。 
- `color.filtered` `bold` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#filteringthematchdisplay)  
	过滤完成项的默认颜色（请参见 [过滤匹配显示](https://chrisant996.github.io/clink/clink.html#saved-command-history#filteringthematchdisplay)）。 
- `color.flag` `default` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，输入行中标志的颜色。 
- `color.hidden` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在显示具有 "隐藏" 属性的文件完成项时使用的颜色。 
- `color.histexpand` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，输入行中的历史扩展颜色。如果此颜色未设置，或 [`history.auto_expand`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_auto_expand) 被禁用或 [`history.expand_mode`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_expand_mode) 关闭，则不会对历史扩展进行着色。 
- `color.horizscroll` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	当 Readline 的 [`horizontal-scroll-mode`](https://chrisant996.github.io/clink/clink.html#saved-command-history#confighorizontalscrollmode) 变量设置时，用于 `<` 或 `>` 水平滚动指示符的颜色。 
- `color.input` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	输入行文本的颜色。请注意，当禁用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，整个输入行将使用 `color.input` 显示。 
- `color.interact` `bold`  
	用于提示的信息的颜色，如分页器的 `--More?--` 提示。 
- `color.message` `default`  
	消息区域（例如搜索提示消息、数字参数提示消息等）的颜色。 
- `color.modmark` `\`  
	已修改历史行标记字符的颜色。 
- `color.popup` `\`  
	当设置时，此选项用于弹出列表和消息的颜色。如果没有设置颜色，则使用控制台的弹出颜色（请参见控制台窗口的属性对话框）。 
- `color.popup_border` `\`  
	当设置时，此选项用于弹出列表边框的颜色。如果没有设置颜色，则使用 `color.popup` 的颜色。 
- `color.popup_desc` `\`  
	当设置时，此选项用于弹出列表中描述列的颜色。如果没有设置颜色，则选择与控制台的弹出颜色互补的颜色（请参见控制台窗口的属性对话框）。 
- `color.popup_footer` `\`  
	当设置时，此选项用于弹出列表底部消息文本的颜色。如果没有设置颜色，则使用 `color.popup_border` 的颜色。 
- `color.popup_header` `\`  
	当设置时，此选项用于弹出列表标题文本的颜色。如果没有设置颜色，则使用 `color.popup_border` 的颜色。 
- `color.popup_select` `\`  
	当设置时，此选项用于所选弹出列表项的颜色。如果没有设置颜色，则通过交换 `color.popup` 的前景和背景颜色来选择颜色。 
- `color.popup_selectdesc` `\`  
	当设置时，此选项用于所选弹出列表项描述文本的颜色。如果没有设置颜色，则通过交换 `color.popup` 的前景和背景颜色来选择颜色。 
- `color.prompt` `\`  
	当设置时，此选项用于提示的默认颜色。但被 [自定义提示](https://chrisant996.github.io/clink/clink.html#saved-command-history#customisingtheprompt) 中设置的任何颜色覆盖。 
- `color.readonly` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	用于显示具有 "只读" 属性的文件完成的颜色。 
- `color.selected_completion` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	与 [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) 命令结合使用，所选完成的颜色。如果没有设置颜色，则使用反转视频。 
- `color.selection` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	输入行中选中文本的颜色（例如，当使用 Shift-箭头键时）。如果没有设置颜色，则使用反转视频。 
- `color.suggestion` `bright black` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	当启用 [`autosuggest.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#autosuggest_enable) 时，自动建议的颜色。 
- `color.suggestionlist` `\`  
	建议列表中建议的颜色（请参见 [建议列表](https://chrisant996.github.io/clink/clink.html#saved-command-history#suggestion-list)）。 
- `color.suggestionlist_dim` `bright black` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	建议列表标题中暗文本的颜色。 
- `color.suggestionlist_highlight` `bright cyan` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	用于高亮显示建议匹配部分的颜色。对于所选建议，结合了 `color.suggestionlist_selected`。 
- `color.suggestionlist_markup` `yellow` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	用于建议列表中标题以及每个建议项的开始和结束的标记的颜色。对于所选建议，结合了 `color.suggestionlist_selected`。 
- `color.suggestionlist_selected` `default on bright black` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	所选建议的颜色。此颜色与其他建议列表颜色结合使用，因此通常应至少指定背景颜色。 
- `color.unexpected` `default`  
	在启用 [`clink.colorize_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#clink_colorize_input) 时，输入行中意外参数的颜色。 
- `color.unrecognized` [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	当设置时，此选项是输入行中未识别为命令、doskey 宏、目录、argmatcher 或可执行文件的命令词的颜色。 
- `comment_row.hint_delay` `500`  
	指定显示输入提示的延迟（以毫秒计）（请参见 [显示输入提示](https://chrisant996.github.io/clink/clink.html#saved-command-history#showinginputhints)）。延迟最多可达 3000 毫秒，或设置为 0 不延迟。 
- `comment_row.show_hints` False  
	允许在注释行中显示输入提示（请参见 [显示输入提示](https://chrisant996.github.io/clink/clink.html#saved-command-history#showinginputhints)）。 
- `debug.log_output_callstacks` False  
	在日志输出时包含调用栈。当启用 `debug.log_terminal` 时，此选项才有效。此选项仅用于诊断目的，并且可能会显著增加日志文件的大小。 
- `debug.log_prompt` False  
	将由提示过滤器生成的原始提示字符串记录到 clink.log 文件。这仅用于诊断目的，并可能会显著增加日志文件的大小。 
- `debug.log_terminal` False  
	将所有终端输入和输出记录到 clink.log 文件。这仅用于诊断目的，并可能会显著增加日志文件的大小。 
- `directories.dupe_mode` `add`  
	控制当前目录历史记录的更新。值为 `add`（默认值）时，总是将当前目录添加到目录历史记录。值为 `erase_prev` 将删除当前目录的任何先前条目，然后将其添加到目录历史记录。请注意，目录历史记录在会话之间不会保存。 
- `doskey.enhanced` True  
	增强的 Doskey 添加了在 `|` 和 `&` 命令分隔符之后展开宏，并在解析 `$1`...`$9` 标签时尊重引号。要抑制单个命令的宏展开，请在命令前面加一个空格或分号（`foo` 或 `;foo`）。或在 `|` 或 `&` 之后，前缀两个空格或分号（ `foo| bar` 或 `foo|;bar`）。 
- `exec.aliases` True  
	当将可执行程序作为第一词匹配时（[`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)），包括 doskey 别名。 
- `exec.associations` False  
	当将可执行程序作为第一词匹配时（[`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)），包括具有注册文件关联的文件（例如可启动文档如 ".pdf" 文件）。 
- `exec.commands` True  
	当将可执行程序作为第一词匹配时（[`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)），包括 CMD 命令（例如 `cd`、`copy`、`exit`、`for`、`if` 等）。 
- `exec.cwd` True  
	当将可执行程序作为第一词匹配时（[`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)），包括当前目录中的可执行文件。（如果正在完成的单词是相对路径或者 [`exec.files`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_files) 为 true，则这是隐含的。） 
- `exec.dirs` True  
	当将可执行程序作为第一词匹配时（[`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)），还包括相对当前工作目录的目录作为匹配项。 
- `exec.enable` True  
	匹配可执行程序时完成行的第一词。可执行程序由 `%PATHEXT%` 环境变量中列出的扩展名确定。 
- `exec.files` False  
	当将可执行程序作为第一词匹配时（[`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)），包括当前目录中的文件。 
- `exec.path` True  
	当将可执行程序作为第一词匹配时（[`exec.enable`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_enable)），包括在 `%PATH%` 环境变量中指定的目录中找到的可执行文件。 
- `exec.space_prefix` True  
	如果行以空格开头，则 Clink 会绕过可执行身份匹配（[`exec.path`](https://chrisant996.github.io/clink/clink.html#saved-command-history#exec_path）），并将执行正常文件匹配。 
- `files.hidden` True  
	在生成文件列表时包括或排除设置为 "隐藏" 属性的文件。 
- `files.system` False  
	在生成文件列表时包括或排除设置为 "系统" 属性的文件。 
- `history.auto_expand` True  
	启用时，一旦接受命令行（通过按 Enter），将自动执行历史扩展。禁用时，历史扩展仅在使用相应的扩展命令时执行（例如 [`clink-expand-history`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-expand-history) Alt-^，或 [`clink-expand-line`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-expand-line) Alt-Ctrl-E）。 
- `history.dont_add_to_history_cmds` `exit history`  
	不自动添加到历史记录的命令列表。命令用空格、逗号或分号分隔。默认值为 `exit history`，以排除这两个命令。 
- `history.dupe_mode` `erase_prev`  
	如果一行是现有历史条目的重复项，Clink 在设置为 `erase_prev` 时将删除重复项。将其设置为 `ignore` 将不添加重复项到历史记录，而将其设置为 `add` 将总是添加行（除非由 [`history.sticky_search`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_sticky_search) 覆盖）。 
- `history.expand_mode` `not_quoted`  
	在输入行中的 `!` 字符可以被解释为从历史中引入单词。通过设置此值为 `on` 或 `off` 可以启用或禁用。设置为 `not_squoted`、`not_dquoted` 或 `not_quoted` 会跳过在单、双或两个引号中引用的任何 `!` 字符。 
- `history.ignore_space` True  
	在将行添加到历史记录时忽略以空格开头的行。 
- `history.max_lines` 10000 [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	如果 [`history.save`](https://chrisant996.github.io/clink/clink.html#saved-command-history#history_save) 被启用，保存的历史行数量（或 0 代表无限）。 
- `history.save` True  
	保存会话之间的历史记录。禁用时，历史记录既未读取也未写入到主历史记录列表中；每个会话的历史记录在会话期间写入临时文件，但不会添加到主历史记录列表中。 
- `history.shared` False  
	当共享历史记录时，Clink 的所有实例在每个命令后更新主历史记录列表，并在每个提示下重新加载主历史记录列表。当不共享历史记录时，每个实例在退出时更新主历史记录列表。 
- `history.show_preview` True  
	启用时， 如果光标处的文本需要进行历史扩展，则将在输入行下方显示扩展结果的预览，使用 [`color.comment_row`](https://chrisant996.github.io/clink/clink.html#saved-command-history#color_comment_row) 设置。 
- `history.sticky_search` False  
	启用时， 重新使用历史行不会将其添加到历史末尾，并且它会将历史搜索位置停留在重新使用的行上，以便可以继续下一/前历史（例如，通过向上播放多个命令，然后按 Enter、向下、Enter 等）。 
- `history.time_format` `%F %T`  
	此选项指定显示历史项时间戳的时间格式字符串。有关格式说明符的列表，请参阅 `clink set history.time_format` 或 [历史时间戳](https://chrisant996.github.io/clink/clink.html#saved-command-history#history-timestamps)。 
- `history.time_stamp` `off`  
	默认值为 `off`。当此选项为 `save` 时，为每个历史项保存时间戳，但仅在与 `history` 命令一起使用 `--show-time` 标志时显示。当此选项为 `show` 时，保存每个历史项的时间戳，并且在 `history` 命令中除非使用 `--bare` 或 `--no-show-time` 标志，否则显示时间戳。 
- `lua.break_on_error` False  
	在 Lua 错误上中断 Lua 调试器。 
- `lua.break_on_traceback` `\`  
	在 `traceback()` 上中断 Lua 调试器。 
- `lua.debug` False  
	启用时加载简单的嵌入式命令行调试器。可以通过调用 [pause()](https://chrisant996.github.io/clink/clink.html#saved-command-history#pause) 添加断点。 
- `lua.path` `\`  
	要追加到 `[package.path](https://www.lua.org/manual/5.2/manual.html#pdf-package.path)` Lua 变量的值。用于搜索在 `require()` 语句中指定的 Lua 脚本。 
- `lua.strict` True  
	启用时，参数错误会导致 Lua 脚本失败。这可能会暴露某些旧脚本中的错误，导致它们在以前成功时失败。在这种情况下，您可以尝试将其关闭，但请提醒脚本拥有者以便他们修复脚本。 
- `lua.throttle_interval` `0`  
	限制协程执行。默认为关闭（0），允许协程自由控制其执行时间和速率。如果协程干扰响应性，您可以将此设置为一个数字，以限制长期运行的协程实际上可以运行的频率（以秒为单位）。在 v1.7.17 之前，限制间隔被硬编码为 5 秒，但现在可以配置，且默认为 0（不限制）。 
- `lua.traceback_on_error` False  
	在 Lua 错误上打印堆栈跟踪。 
- `match.coloring_rules` `\`  
	提供在显示匹配完成项时使用的一系列颜色定义。有关详细信息，请参见 [完成颜色](https://chrisant996.github.io/clink/clink.html#saved-command-history#completioncolors)。 
- `match.expand_abbrev` True  
	在执行完成之前展开缩写路径。在缩写路径中，目录名称可以缩短到以不歧义地引用目录所需的最小字符数。例如，“c:\\Users\\chris\\Documents” 可以缩写为 “c:\\U\\c\\Do”，具体取决于文件系统中存在的目录。 
- `match.expand_envvars` False [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	在执行完成之前展开单词中的环境变量。 
- `match.fit_columns` True  
	在显示匹配完成项时，计算列宽以适应尽可能多的项。 
- `match.ignore_accent` True  
	控制完成匹配时的重音敏感性。例如，`ä` 和 `a` 在启用时被视为等效。 
- `match.ignore_case` `relaxed`  
	控制完成匹配时的大小写敏感性。 `off` = 区分大小写，`on` = 不区分大小写，`relaxed` = 不区分大小写并且 `-` 和 `_` 被视为相等。 
- `match.max_fitted_matches` `0`  
	当启用 [`match.fit_columns`](https://chrisant996.github.io/clink/clink.html#saved-command-history#match_fit_columns) 设置时，当匹配项数量超过此值时，禁用计算列宽。默认值为 0（无限制）。根据屏幕宽度和 CPU 速度，设置限制可能避免延迟。 
- `match.max_rows` `0`  
	[`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) 可以显示的最大项数。当此选项为 0 时，限制为终端高度。 
- `match.preview_rows` `0`  
	使用 [`clink-select-complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-select-complete) 命令（默认绑定为 Ctrl-Space）时，显示作为预览的行数。当此选项为 0 时，显示所有行，如果匹配项过多，则首先提示，如 [`complete`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-complete) 命令所做。否则，它显示指定数量的行作为预览，没有提示，并在选择移动到超出预览行时展开以显示完整的匹配项。 
- `match.sort_dirs` `with`  
	如何对匹配目录名称进行排序。`before` = 在文件之前，`with` = 与文件一起，`after` = 在文件之后。 
- `match.substring` False [\*](https://chrisant996.github.io/clink/clink.html#saved-command-history#alternatedefault)  
	当设置时，如果未找到前缀搜索的完成项，则执行子字符串搜索。 
- `match.translate_slashes` `auto`  
	文件和目录完成可以转换为一致使用的斜杠。 默认值为 `auto`，会根据完成单词中第一种斜杠的类型翻译所有斜杠（如果单词在完成之前没有斜杠，则使用系统路径分隔符）。使用 `slash` 表示要使用正斜杠，`backslash` 表示要使用反斜杠，或 `system` 表示适合主机的路径分隔符（在 Windows 上为反斜杠）。使用 `off` 来关闭斜杠翻译。 
- `match.wild` True  
	使用任意完成命令时匹配 `?` 和 `*` 通配符。关闭此选项以便于 bash 不匹配通配符（但 [`glob-complete-word`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-glob-complete-word） 总是匹配通配符）。 
- `prompt.async` True  
	启用 [异步提示刷新](https://chrisant996.github.io/clink/clink.html#saved-command-history#asyncpromptfiltering)。如果提示过滤刷新使人烦恼或导致问题，则关闭此选项。 
- `prompt.spacing` `normal`  
	默认值为 `normal`，这永远不会删除或添加空行。设置为 `compact` 以删除提示前的空行，或设置为 `sparse` 以删除空行并添加一个空行。 
- `prompt.transient` `off`  
	控制何时收起过去的提示（[瞬态提示](https://chrisant996.github.io/clink/clink.html#saved-command-history#transientprompts)）。 `off` = 从不收起过去的提示，`always` = 始终收起过去的提示，`same_dir` = 仅当当前工作目录自上次提示以来未更改时收起过去的提示。 
- `readline.hide_stderr` False  
	压制 Readline 库中的 stderr。如果 Readline 错误消息妨碍使用，请启用此选项。 
- `suggestionlist.default` False  
	当此选项为 true 时，Clink 会话以启用建议列表开始。可以使用 F2 或绑定到 [`clink-toggle-suggestion-list`](https://chrisant996.github.io/clink/clink.html#saved-command-history#rlcmd-clink-toggle-suggestion-list) 命令的其他键切换建议列表。 
- `terminal.adjust_cursor_style` True  
	当启用时，Clink 会调整光标形状和可见性以显示插入模式，产生可见铃声效果，避免使人困惑的光标闪烁，并支持调整光标形状和可见性的 ANSI 转义码。但这会干扰 Windows 10 光标形状控制台设置。通过禁用此 Clink 设置（以及它提供的功能）可以使光标形状设置生效。 
- `terminal.color_emoji` `auto`  
	设置此项以指示终端程序是否使用彩色双宽字符绘制表情符号。需要准确设置此项，以便 Clink 能够在输入行中正确显示包含表情符号的内容。当设置为 `off` 时，Clink 假设表情符号是以 1 个字符单元渲染的。当设置为 `on` 时，Clink 假设表情符号是以 2 个字符单元渲染的。默认设置为 `auto`，Clink 会根据操作系统版本和终端程序尝试预测表情符号的渲染方式。 
- `terminal.differentiate_keys` False  
	启用时，按 Ctrl-H 或 I 或 M 或 \[ 会生成特殊键序列，以使它们能够与 Backspace 或 Tab 或 Enter 或 Esc 单独绑定。 
- `terminal.east_asian_ambiguous` `auto`  
	存在一组东亚字符，其宽度在 Unicode 标准中是模糊的。此选项控制如何解决模糊宽度。 默认情况下，设置为 `auto`，但某些终端主机可能需要将其设置为不同的值，以解决终端主机中的限制。将其设置为 `font` 会使用当前字体测量东亚模糊字符的宽度。将其设置为 `one` 使用 1 作为宽度，或 `two` 使用 2 作为宽度。当此选项为 ‘auto’（默认值）且当前代码页为 932、936、949 或 950 时，它会尝试根据使用的终端主机和字体自动测量宽度，或对于任何其他代码页（包括 UTF8）使用 1 作为宽度。 `%CLINK_EAST_ASIAN_AMBIGUOUS%` 环境变量覆盖此设置。 
- `terminal.emulation` `auto`  
	Clink 可以模拟虚拟终端并自己处理 ANSI 转义码，或者让控制台主机处理 ANSI 转义码。 `native` = 直接将输出发送到控制台主机进程，`emulate` = clink 自身处理 ANSI 转义码， `auto` = 模拟，除非运行在 ConEmu、Windows Terminal、WezTerm 或 Windows 10 新控制台中。  
	在设置了 [`%CLINK_ANSI_HOST%`](https://chrisant996.github.io/clink/clink.html#saved-command-history#override-terminal-detection) 的情况下，此设置被覆盖。 
- `terminal.mouse_input` `auto`  
	Clink 可以选择响应鼠标输入，而不是让终端响应鼠标输入（例如，在屏幕上选择文本）。当 Clink 启用鼠标输入时，单击输入行会设置光标位置，单击弹出列表会选择项目等。将此设置为 `off` 让终端主机处理鼠标输入，将 `on` 让 Clink 处理鼠标输入，将 `auto` 让 Clink 在 ConEmu 和默认的 Conhost 终端中（当在控制台属性对话框中没有勾选快速编辑模式时）处理鼠标输入。有关详细信息，请参见 [鼠标输入](https://chrisant996.github.io/clink/clink.html#saved-command-history#gettingstarted_mouseinput)。 
- `terminal.mouse_modifier` `\`  
	此选项选择必须按住哪些修饰键（Alt、Ctrl、Shift），以便在启用 [`terminal.mouse_input`](https://chrisant996.github.io/clink/clink.html#saved-command-history#terminal_mouse_input) 设置时 Clink 响应鼠标输入。 这是一个文本字符串，可以列出一个或多个修饰键：‘alt’，‘ctrl’ 和 ‘shift’。例如，将其设置为 "alt shift" 会导致 Clink 仅在同时按住 Alt 和 Shift 时响应鼠标输入（而不是 Ctrl）。如果设置了 `%CLINK_MOUSE_MODIFIER%` 环境变量，则其值会覆盖此设置。有关详细信息，请参见 [鼠标输入](https://chrisant996.github.io/clink/clink.html#saved-command-history#gettingstarted_mouseinput)。 
- `terminal.raw_esc` False  
	启用时，按 Esc 会发送一个字面上的转义字符，如在 Unix 或 Linux 终端中一样。默认情况下，此选项被禁用，以提供在 Windows 上更可预测、可靠和可配置的输入体验。更改此设置只影响将来的 Clink 会话，而不影响当前会话。 
- `terminal.scrollbars` True  
	当启用时，列表使用扩展的 Unicode 方框绘制字符显示滚动条。某些终端或字体可能与此不兼容。 
- `terminal.shell_integration` `auto`  
	Clink 可以向终端发送 [shell 集成代码](https://learn.microsoft.com/en-us/windows/terminal/tutorials/shell-integration)，如果终端支持它们。当设置为 `off` 时，Clink 从不发送 shell 集成代码。当设置为 `on` 时，Clink 始终发送 shell 集成代码。当设置为 `auto` 时，Clink 仅在检测到可能支持这些代码的终端时发送 shell 集成代码。 
- `terminal.use_altgr_substitute` False  
	支持 Windows 的 Ctrl-Alt 替代 AltGr。禁用此选项可能会解决与 Readline 键绑定的冲突。