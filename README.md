# Interactive Football Pitch Using Jupyter Voila

[Jupyter voila](https://blog.jupyter.org/and-voil%C3%A0-f6a2c08a4a93) allows to serve Jupyter notebooks, and especially ipywidgets, as standalone applications.
This repository contains an example notebook which uses `ipydatagrid` and `bqplot` to create a simple interactive football pitch.
You can test it live in Binder or run it locally.

The deployed notebook can be found here: [Notebook on Heroku](https://voila-football-pitch-example.herokuapp.com/)  
(Be patient, it might need some time to spin up the dyno on Heroku.)

## Voila in Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/seidlr/voila-interactive-football-pitch/master?urlpath=voila%2Frender%2FInteractive-Football-Pitch.ipynb)

## Notebook in Binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/seidlr/voila-interactive-football-pitch/master?filepath=Interactive-Football-Pitch.ipynb)

## Local installation

To run the example notebook, first create a `conda` environment.

```bash
conda env update
```

This creates an environment `voila-football-pitch` which can be used in a jupyter notebook.
Next, activate the environment and start the voila server.

```bash
conda activate voici-interactive-football-pitch
```

run the notebook by

```
voici Interactive-Football-Pitch.ipynb
```

## Old notebook

jupyter nbextension enable --py --sys-prefix bgplot
jupyter nbextension install --py --symlink --sys-prefix ipydatagrid
jupyter nbextension enable --py --sys-prefix ipydatagrid

## Voici

To use Voici, you'll need to install it first:

pip install voici
Then, you can generate static dashboards from a notebook or a directory of Notebooks like this:

```
# Build the dashboard

voici Interactive-Football-Pitch.ipynb

```

Once your dashboards are built, you can simply serve them with a simple static server, e.g.:

```
cd \_output
python -m http.server
```
