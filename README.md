# AgrarGIS

## Installation

After cloning the repository, run

    npm install

to install the project's dependencies.

## Prepare data

This project requires vector tiles and styles for its maps. Vector tiles are created with [Tippecanoe](https://github.com/mapbox/tippecanoe/), which needs to be installed on the system that creates the tiles. Styles need sprites, which are built from the icons provided in `public/map/icons/`.

1. Download the layers as zip from the URL provided by Manuel Illmeyer
2. Unzip the content of the zip to the `data/` Folder
3. Run

       npm run tiles:vector
    
   If you want to download a cache of the raster tiles used by this application, also run

       npm run tiles:raster

   The application requires both to run.

## Run the development server

    npm run dev

## Build the application for deployment

    npm run build

Note that this will take a while, because not only the application, but also the data (vector tiles!) will be copied to the `dist/` folder.

To deploy the application, copy the contents of the `dist/` folder of your S3 or http server.

To rebuild only the app, assuming that the vector tiles were already deployed, run

    npm run build-app

## Creating sprites for the Mapbox Style file

The sprites in `public/map/` are created from the svg images in `pulic/map/icons/`. When adding new svg images to that folder, run

    npm run sprites

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)
