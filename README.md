# Snippets for VSCode: Jaspr Components

 These snippets allow you to scaffold Jaspr components with minimal typing, speeding up your development process.


## Installation

Adding Jaspr snippets to VSCode is straightforward:

1. Open your command palette with `Cmd+Shift+P`.
2. Type "user snippets" and select `Configure User Snippets`.
3. Choose `dart.json` from the list of available snippet files.
4. Paste the provided JSON code or add them along with other configurations into your `dart.json` file, and save it.

## Usage

- **jstless**: Creates a basic structure for a Jaspr Stateless Component.
- **jstful**: Creates a basic structure for a Jaspr Stateful Component.

Below is the JSON code for the Jaspr snippets. Copy and paste this into your `dart.json` file under the VSCode user snippets directory.

```json
{
    "Jaspr Stateless Component": {
        "prefix": "jstless",
        "body": [
            "class $1 extends StatelessComponent {",
            "  @override",
            "  Iterable<Component> build(BuildContext context) sync* {",
            "    yield $2;",
            "  }",
            "}",
            ""
        ],
        "description": "Creates a Jaspr stateless component"
    },
    "Jaspr Stateful Component": {
        "prefix": "jstful",
        "body": [
            "class $1 extends StatefulComponent {",
            "  $1State createState() => $1State();",
            "}",
            "",
            "class $1State extends State<$1> {",
            "  @override",
            "  Iterable<Component> build(BuildContext context) sync* {",
            "    yield $2;",
            "  }",
            "}",
            ""
        ],
        "description": "Creates a Jaspr stateful component"
    }
}
```

These snippets are designed to streamline your Jaspr development workflow, making it easier and faster to create components for your web applications.
