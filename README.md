# Linear Theme for VS Code

The official [Linear](https://linear.app) color themes for Visual Studio Code. Bring Linear's colors to your editor,
sidebar, menus, diffs, and integrated terminal.

## Themes

| Theme               | Appearance                                        |
| ------------------- | ------------------------------------------------- |
| **Linear Dark**     | Linear's dark UI and default syntax colors        |
| **Linear Light**    | Linear's light UI and default syntax colors       |
| **Linear Midnight** | Linear's dark UI with its Midnight syntax palette |

Midnight changes the code colors while keeping the same UI colors as Linear Dark.

Requires **VS Code 1.80.0 or later**. The extension provides color themes; your fonts, layout, and file icons stay under
your control. No Linear account or additional extension is needed.

## Install

Find [Linear.app Theme in the Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=linear-app.linear-app-theme),
or open **Extensions** in VS Code and search for `@id:linear-app.linear-app-theme`. Check that the publisher is
**Linear**, then select **Install**.

You can also install it from a terminal if the `code` command is on your PATH:

```sh
code --install-extension linear-app.linear-app-theme
```

### Choose a theme

Open the Command Palette with `Cmd+Shift+P` on macOS or `Ctrl+Shift+P` on Windows/Linux. Run **Preferences: Color Theme**
and select **Linear Dark**, **Linear Light**, or **Linear Midnight**.

The theme picker shortcut is `Cmd+K`, then `Cmd+T` on macOS, or `Ctrl+K`, then `Ctrl+T` on Windows/Linux.

### Install a VSIX package

If you have a `.vsix` package, run **Extensions: Install from VSIX...** from the Command Palette and select the file.
Then choose a Linear theme as described above. You can also install a local package from a terminal:

```sh
code --install-extension /path/to/linear-app-theme-<version>.vsix
```

Replace the path and `<version>` with your package's filename. VS Code disables automatic updates by default for
extensions installed from VSIX; manage updates from the extension's entry in the Extensions view.

## Follow your system appearance

To switch between Light and Dark with your system appearance, merge these entries into your VS Code user
`settings.json`:

```json
{
  "window.autoDetectColorScheme": true,
  "workbench.preferredDarkColorTheme": "Linear Dark",
  "workbench.preferredLightColorTheme": "Linear Light"
}
```

Use `"Linear Midnight"` as the preferred dark theme if you want its code colors.

## Troubleshooting

**The theme is missing from the picker.** Check that `linear-app.linear-app-theme` is installed and enabled in the
current VS Code profile. Run **Developer: Reload Window**, then open **Preferences: Color Theme** again.

**Colors differ from the theme.** Check both user and workspace settings for `workbench.colorCustomizations`,
`editor.tokenColorCustomizations`, and `editor.semanticTokenColorCustomizations`. These settings can override theme
colors, including entries scoped to a specific Linear theme. Back up your settings before removing overrides you
want to compare.

**Code colors differ between languages.** Syntax colors depend on the language mode and installed language
extensions. Semantic highlighting can also affect them. Check the file's language mode and include a small code
sample when reporting a syntax issue.

**VS Code changes the theme automatically.** Check `window.autoDetectColorScheme`, your preferred light/dark themes,
and any workspace-specific `workbench.colorTheme` setting. See the [VS Code theme guide](https://code.visualstudio.com/docs/configure/themes)
for details.

## Feedback and source

Report color or readability issues in the [theme repository](https://github.com/linear/linear-vscode-theme/issues).
Include the theme name, extension version, VS Code version, operating system, and a screenshot or small code sample
that shows the problem. For syntax issues, include the language and relevant language extensions.

To preview a checkout of the [source repository](https://github.com/linear/linear-vscode-theme), run this command from
its root:

```sh
code --extensionDevelopmentPath=.
```

Select a Linear theme in the Extension Development Host window. The repository includes the theme JSON files, so
previewing them does not require a build.

## License

[MIT](https://github.com/linear/linear-vscode-theme/blob/main/LICENSE.txt)
