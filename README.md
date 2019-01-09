# Cerebro

## Description

Visualize and explore complex data sets from single-cell RNA-sequencing experiments.

Currently available only for Windows and macOS.
Linux users have the option to launch the application through a Docker container or hosting the application using the `app.R` file and a local R installation.

## Installation

Download release for your OS, unpack and run.

## Usage

* Analyze data set with Cerebro-prepare pipeline.
* Launch the browser and load the data set.

## How to build from source

### macOS

To clone and run this repository you'll need [Git](https://git-scm.com) and [Node.js](https://nodejs.org/en/download/) (which comes with [npm](http://npmjs.com)) installed on your computer. From your command line:

```bash
# Clone this repository
git clone https://gitlab.com/romanhaa/cerebro.git
# Install Electron Packager (if first time)
npm install electron-packager -g 
# Go into the repository
cd source
# Install dependencies
npm install
# Install electron-log (probably not necessary)
npm install electron-log
# Run the app
npm start
# Build the Executable/App
npm run package-win
OR
npm run package-mac 
```

### Windows

If you're using Linux Bash for Windows, [see this guide](https://www.howtogeek.com/261575/how-to-run-graphical-linux-desktop-applications-from-windows-10s-bash-shell/) or use `node` from the command prompt.

## Release History

* version X.X
  * ...

## Contributions

* <https://github.com/ColumbusCollaboratory/electron-quick-start>

## To Do

* [ ] Upload current state.
* [ ] Prepare Docker container and instructions on how to use it.
* [ ] Add contributions that are currently mentioned inside the browser.

## Changelog

* Use `formattable`.
* Make only RDS files selectable.
* Change text in some panels.
* Make input in gene expression panel case-independent.
* Make refresh shortcut local (instead of global).
* Make sample names be displayed instead of the long names (top expressed genes and marker genes).
* Border around plots.
* Show names in sample-by-cluster and cluster-by-sample plots and cell cycle in respective plots.
* Allow user to choose plotting order.
* Reorder some user inputs to save space.
* Show cluster tree if available.
* Hide some columns from tables in enriched pathways to have a cleaner view. They can still be shown manually.
* Use a box layout across the app.
* Use more attractive colors (from <flatuicolors.com>).
* Add info popup boxes with additional explanation for each/most panel(s).
* Reduce empty space (padding around boxes) across the app.
* Remove Z-score from marker gene tables since combined score should be more informative.
* Add color bar representation through formattable in marker gene tables.
* Remove legend in gene expression and gene set expression scatter plots because scale will still be visible in box plots.
* Add checks for presence of tables of top expressed genes and marker genes.
* Hide gene column in enriched pathway tab by default to save space.
* Update R version for Windows to 3.5.1.
* Add export buttons for dimensional reductions using ggplot instead of the scatterD3 function which crashes with too many cells.
* Manually modify code for scatterD3 legend to prevent sorting. A more consistent solution should be found however.
* If marker genes haven't already been checked in the pipeline, this will be done in the browser for murine and human samples.