# Choropleth Movie Visualisation

Interactive **D3.js** choropleth map showing movie-related metrics (e.g. average rating, revenue) by country using a movie dataset. The project is a static web app: open `index.html` in a browser to explore the map. This was implmented as part of a group vizualisation project. 

## Features

- World choropleth map using TopoJSON country shapes. 
- Country colouring based on movie statistics per country.
- Tooltip / hover interactions for inspecting values.
- Legend and colour scale driven by D3.

## Project Structure

├─ .vscode/     
├─ data/  
│ ├─ countries-50m.json     # TopoJSON world map  
│ └─ movies_*.csv/json     # Movie dataset(s) used for the map  
├─ libs/  
│ └─ d3/     # D3.js library files  
├─ scripts/  
│ ├─ ChoroplethMap.js     # Main D3 choropleth implementation  
│ └─ utils.js      
├─ styles/  
│ ├─ main.css      
│ └─ choropleth-map.css     #  map-specific styles  
├─ index.html     # Entry point  
└─ template.png      
 
## Getting Started

### Prerequisites

- Any modern web browser (Chrome, Firefox, Edge, Safari).
- Optionally, a simple HTTP server (recommended to avoid CORS issues when loading data). 

### Run Locally

1. Clone the repository:

```
 git clone https://github.com/lostithi/Choropleth-Movie-Vizualisation.git
 cd Choropleth-Movie-Vizualisation 
```

2. Start a local web server (pick one):

```
Python 3
python -m http.server 8000

Node (http-server)
npx http-server . 
```


3. Open in the browser:

- Go to `http://localhost:8000/index.html`.

The choropleth should load the world map from `data/countries-50m.json` and the movie data from files in `data/`, then render the coloured map in the main container defined in `index.html`. 
 
 
## Development Notes

- All files are static; no build step is required.
- Keep relative paths consistent: `index.html` expects data in `data/`, script files in `scripts/`, styles in `styles/`, and D3 in `libs/d3/`. 

   


