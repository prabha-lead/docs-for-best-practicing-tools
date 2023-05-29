### Prettier in VSCode

[Prettier](https://prettier.io/) is an opinionated code formatter that supports multiple languages and integrates with most editors. It helps enforce a consistent style by parsing your code and re-printing it with its own rules that take the maximum line length into account, wrapping code when necessary.

Here's how you can set up and use Prettier in VSCode:

1. **Install Prettier**

First, install Prettier globally:

```bash
npm install -g prettier
```

Or you can add it as a dev dependency in your project:

```bash
npm install --save-dev --save-exact prettier
```

2. **Install the Prettier VSCode Extension**

Install the Prettier extension from the VSCode marketplace. This extension will allow VSCode to use Prettier for code formatting.

3. **Configure Prettier**

Create a `.prettierrc` file in the root of your project to configure Prettier. Here's an example configuration:

```json
{
  "semi": true,
  "trailingComma": "all",
  "singleQuote": true,
  "printWidth": 80,
  "tabWidth": 2
}
```

You can also configure Prettier through the VSCode settings. To do this, open the settings (File -> Preferences -> Settings or `Ctrl+,`) and search for "Prettier".

4. **Use Prettier**

To format your code with Prettier, you can right-click anywhere in the document and select "Format Document". Or you can use the `Shift+Alt+F` shortcut.

To make Prettier the default formatter for certain file types, you can add the following to your VSCode settings:

```json
"[javascript]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
"[css]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},
// and so on for other file types
```

### Emmet in VSCode

Emmet is a web-developer's toolkit that can greatly improve your HTML & CSS workflow. It allows you to use abbreviations that it will then expand into full-fledged HTML or CSS code. Emmet support is built right into VSCode, and no extension installation is necessary.

Here's how you can use Emmet in VSCode:

1. **Using Emmet Abbreviations**

To use Emmet, you simply type an Emmet abbreviation and then press `Tab` to expand it. For example, typing `div` and then pressing `Tab` will give you `<div></div>`.

2. **Configure Emmet**

To configure Emmet settings, open the VSCode settings (File -> Preferences -> Settings or `Ctrl+,`) and search for "Emmet". Here you can customize the behavior of Emmet in VSCode.

3. **Emmet Cheat Sheet**

You can check out the [Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/) for a list of Emmet abbreviations.

4. **Enable Emmet in JSX**

By default, Emmet doesn't work in JSX in VSCode. To enable Emmet support in JSX, add the following to your VSCode settings:

```json
"emmet.includeLanguages": {
  "javascript": "javascriptreact"
}
```

With these steps, you should be able to effectively use Prettier and Emmet in VSCode. Both of these tools can greatly enhance your productivity in web development.
