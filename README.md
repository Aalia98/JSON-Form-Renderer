# JSON Form Renderer

A React app that renders a form from a JSON schema. Paste a schema into the text area, click **Render UI**, and the form appears in the preview panel. Submitting the form shows the entered values as JSON.

A sample schema is included in `pasta.json` (a "Create Pasta" form).

## Features

- Paste a JSON schema and render it as a form with one click
- Alert with the error message if the JSON is not valid
- Fields are ordered by the `sort` value in the schema
- Supported field types (`uiType`):
  - `Input` - text field, with `placeholder` and `required`
  - `Select` - dropdown with `options` and a default value
  - `Group` - a box with a label that holds nested fields (works recursively)
- Submit collects the form values by `jsonKey` and shows them as JSON below the form

## Tech

React 18, Vite and Tailwind CSS.

## Run locally

Requires Node.js and npm.

```
git clone https://github.com/Aalia98/JSON-Form-Renderer.git
cd JSON-Form-Renderer
npm install
npm run dev
```

Then copy the contents of `pasta.json` into the text area and click **Render UI**.

## Known limitations

- Only `Input`, `Select` and `Group` are supported; other field types are not rendered
- Validation is limited to the browser's `required` check
- The Cancel button does not do anything yet
