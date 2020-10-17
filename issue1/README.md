Issue with VSCode Elm plugin v1.4.1 showing a wrong info message:

```
{
	"resource": "/d:/Dev/vscode-elm-tooling-issues/issue1/src/Main.elm",
	"owner": "Elm",
	"severity": 2,
	"message": "Missing type annotation: `number`",
	"source": "Type Inference",
	"startLineNumber": 12,
	"startColumn": 1,
	"endLineNumber": 12,
	"endColumn": 5
}
```

To reproduce:

- open this project in vscode
- then open the `Main` module
- wait for the Elm indexing to finish, afterwards the info message will show

The info message doesn't always show. I'm not sure why.

The problem is related to the `Broken` module. This module is in the project but it's not imported anywhere. So the project builds correctly.
