# Covid19-Vaccines-and-Treatments

Latest source-of-truth (input data) is found here: https://docs.google.com/spreadsheets/d/1M09AJucy7pQzqrXOvku7nYwWL6Ks0edR2fCfTYifnus/edit#gid=1988095192

Each row in `input_data/source_of_truth_drugs_format.csv` represents a single potential vaccine. To create the timeline visualizations, each cell of every row that represents a drug development phase in input data needs to become its own unique row in the output data, `output_data/viz_timeline_format.csv`.

The map data conversion is much simpler. Each row in `input_data/source_of_truth_maps_format.csv` represents a single clinical trial location. This matches with the format of `output_data/viz_map_format.csv`.

In order to update the visualization, a new row must be added to the bottom with whatever fields have changed along with an increase in the version number for that row (see the last 2 rows in `output_data/viz_map_format.csv` for an example). The visualizations will always pull the highest version number of each unique row.