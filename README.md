## Fluoro-forest: A semi-supervised machine learning worfklow for cell type prediction in high plex immunofluorescence data.


<div align="center">
  <img src="method_workflow.png" alt = "fluoroforest workflow" width="800">
</div>

Method overview can be found here:  , recommended to start with core_c7.ipynb for full worfklow

To run the provided examples, image data and epxression summaries can found at Dryad: 
specifically, '_expression.tsv' and '.ome.tif files', to create the final project structure:

```
fluoroforest
├── environments
│   ├── cellpose.yaml # environment for cell segmentation (independent workflow)
│   └── cell_annotations.yml # environment for running training and prediction framework
├── example_data
│   ├── anal_cancer
│   │   ├── processed
│   │   │   ├── C-7.ome.tif # core biopsy 1 (DRYAD)
│   │   │   └── N-12.ome.tif # core biopsy 2 (DRYAD)
│   │   ├── raw
│   │   │   └── channelnames.txt # marker names in order of image slice
│   │   ├── segmentations
│   │   │   ├── C-7.geojson
│   │   │   ├── c7_subset_expanded_seg.npy # derived from cellpose example
│   │   │   ├── c7_susbet_seg.npy # derived from cellpose example
│   │   │   └── N-12.geojson
│   │   ├── summaries
│   │   │   ├── C-7_coords.csv
│   │   │   ├── C-7_expression.csv # expression summary of core 1 (DRYAD)
│   │   │   ├── N-12_coords.csv
│   │   │   └── N-12_expression.csv # expression summary of core 2 (DRYAD)
│   │   └── temp_annotations
│   │       ├── C7_annotations.csv # training data
│   │       └── N12_annotations.csv # training data
│   └── others
│       └── placeholder.txt
├── src
│   ├── functions
│   │   ├── __init__.py
│   │   ├── anno_class.py
│   │   ├── annotation_utils.py
│   │   ├── classifier_class.py
│   │   ├── core_class_test.py
│   │   ├── plot_utils.py
│   │   └── segmentation_utils.py
│   └── notebooks
│       ├── __init__.py
│       ├── combined_c7_n12.ipynb # compares exclusive vs composite models
│       ├── core_c7.ipynb # EXAMPLE 1, requires annotation environment
│       ├── core_n12.ipynb # EXAMPLE 2, require annotation environment
│       └── segmentation_example.ipynb # segmentation worfklow, requires cellpose environment
└── workflow.png
```

