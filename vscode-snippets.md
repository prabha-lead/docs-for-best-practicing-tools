# VS Code Snippets [Link to Video](https://github.com/prabha-lead/docs_for_best_practicing_tools/raw/main/vscode-snippets.mp4)

Visual Studio Code (VSCode) allows users to use snippets in any type of file. Snippets are small blocks of reusable code that can be inserted in a file quickly. Snippets in VSCode can save you keystrokes and increase your productivity by reducing repeated typing tasks.

Here is a basic guide for creating custom JavaScript snippets in VSCode.

1. **Open the Code Snippets file**

First, open VSCode and navigate to "File" -> "Preferences" -> "User Snippets". A dropdown will appear, select "JavaScript". This will open a new file called `javascript.json`. This file is where you will define your custom JavaScript snippets.

2. **Defining a Snippet**

A snippet is defined in JSON format. The overall structure of a snippet is as follows:

```json
"SnippetName": {
    "prefix": "trigger",
    "body": [
        "code line 1",
        "code line 2"
    ],
    "description": "Description of the snippet"
}
```

- `"SnippetName"`: This is just a name for your snippet. It is not used in the editor.

- `"prefix"`: This is the trigger keyword for your snippet. When you type this keyword in the editor and press `Tab` or `Enter`, the snippet will be inserted.

- `"body"`: This is an array containing the code lines of your snippet. Each line is a separate string in the array.

- `"description"`: This is a brief description of your snippet. It will be displayed in the snippet suggestions dropdown in the editor.

3. **Example JavaScript Snippet**

Here's an example of a simple JavaScript snippet for a `console.log` statement:

```json
"Console Log": {
    "prefix": "log",
    "body": [
        "console.log($1);"
    ],
    "description": "Inserts a console.log statement"
}
```

After defining this snippet, when you type "log" and press `Tab` or `Enter` in the editor, it will insert `console.log();` with the cursor positioned between the parentheses.

4. **Using Variables and Placeholders**

VSCode snippets support the use of variables and placeholders to increase their flexibility. For example, you can use `$1`, `$2`, etc., in the `"body"` field to indicate cursor positions after the snippet is inserted. `$0` indicates the final cursor position.

Here's an example of a snippet using placeholders:

```json
"Function": {
    "prefix": "func",
    "body": [
        "function $1($2) {",
        "\t$0",
        "}"
    ],
    "description": "Inserts a function declaration"
}
```

When you trigger this snippet, it will insert a function declaration. The cursor will first be positioned at `$1` (where the function name should be), then move to `$2` (where the function parameters should be), and finally move to `$0` (inside the function body).

After defining your snippets, save the `javascript.json` file. Your snippets are now ready to use. Remember that snippet suggestions are only shown if Quick Suggestions are enabled for your language.

For more information, you can refer to the official VSCode documentation on Snippets [here](https://code.visualstudio.com/docs/editor/userdefinedsnippets).


