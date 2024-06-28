# jump-start-template

A shortcut to your favorite code.

`jump-start` is a lightweight system to organize that code that
you keep coming back to. It’s a structured GitHub repository
and a web frontend.

A **starter** is a directory of code that you like -- whether
it’s a single script or an entire app. Each starter lives in a
**group** directory. Organize similar code for easier
navigation.

When you want to use your favorite code, locate that starter
either in this README.md or in your gallery website. Copy the
command, and run it in your terminal. Your starter code is now
in your project.

## Starters

*This section of the readme will be rewritten automatically
with documentation for your specific starters.*

See
[kevinschaul/jump-start/](https://github.com/kevinschaul/jump-start/##Starters)
for an example.

## Adding a starter

Why not use jump-start to add a starter? Run the following command, replacing
STARTER_GROUP with a group name (e.g. `react`), and STARTER_NAME with a
starter name (e.g. `BarChart`).

```
npx tiged kevinschaul/jump-start-template/example/starter STARTER_GROUP/STARTER_NAME
```

Then, add your code, and edit the generated `jump-start.yaml` file to your liking.

### `jump-start.yaml`

Each starter must contain this file, which defines a few items used by the
gallery.

Some examples:

- [kevinschaul react-d3/LineChart](https://github.com/kevinschaul/jump-start/blob/main/react-d3/LineChart/jump-start.yaml)
- [kevinschaul r/data-analysis](https://github.com/kevinschaul/jump-start/blob/main/r/data-analysis/jump-start.yaml)

**`description`**: Anything you want to write about this starter. It could be
the code’s features, any additional installation instructions, whatever. This
appears in the `## Starters` section of the README.md, and in the web gallery.

**`defaultDir`**: Where the files generated by this starter will be placed by
default. For example, if you know that your React components live in
`components/elements/`, set the `defaultDir` to that. The jump-start command
shown in the README.md and gallery will place the files into this directory.

**`mainFile`** (optional): The file shown initially in the gallery's "Starter files
section.

**`preview`** (optional): Configuration that gets passed down to the gallery's
"Preview" section. The previews render via
[Sandpack](https://sandpack.codesandbox.io/docs/getting-started/usage), so this
configuration mimics Sandpack's. Currently only supports React. Your starter
must include the file `Preview.js`, which default exports a React component.

**`preview.template`** (optional, e.g. "react"): The template used by Sandpack.
I've only used "react" but others may work too.

**`preview.dependencies`** (optional, e.g. `d3: "5"`): An object containing
dependencies for Sandpack to use for the preview. Think of it as the
`package.json` file for the preview. Anything your starter needs should be
listed here.

## Running the gallery locally

The jump-start gallery code lives in [a separate
repo](https://github.com/kevinschaul/jump-start-gallery),
included here as an npm package. To run the gallery
locally, using the starters in this repo as its data:

```
npm install
npm run dev
```

Open [localhost:6006](localhost:6006) in a browser.

## Deploying the gallery to Github Pages

This repo includes a [deploy workflow](.github/workflows/deploy.yml) that
deploys your jump start gallery to Github pages.
 
