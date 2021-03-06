# jupyterlab-nengo

Use the Nengo GUI within JupyterLab.

![Screenshot of Nengo GUI running in JupyterLab](screen-small.png)

## Prerequisites

* JupyterLab
* [Node.js](https://nodejs.org/en/) with npm
* [Nengo GUI](https://github.com/nengo/nengo-gui) from GitHub with the
  fix-jupyter-integration branch being installed.

## Installation

### Activate the Nengo GUI Jupyter notebook server extension (backend)

Add the following to your `~/.jupyter/jupyter_notebook_config.json`:

```json
{
  "NotebookApp": {
    "nbserver_extensions": {
      "nengo_gui.jupyter": true
    }
  }
}
```

### Install the JupyterLab extension (frontend)

Run:

```bash
jupyter labextension install @jgosmann/jupyterlab-nengo
```

## Development

For a development install (requires npm version 4 or later), do the following
in the repository directory:

```bash
npm install
npm run build
jupyter labextension link .
```

To rebuild the package and the JupyterLab app:

```bash
npm run build
jupyter lab build
```

