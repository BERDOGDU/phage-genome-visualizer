# Phage Genome Visualizer

A reusable, standalone **HTML5/JavaScript** tool for proportional visualization of bacteriophage genome architecture and functional modules.

The tool runs locally in a modern web browser and does **not** require installation of Python, R, JavaScript packages, or external libraries.

## Features

- Import annotated CDS information from **CSV**.
- Import a local **GenBank (`.gb`, `.gbk`, `.genbank`)** file downloaded from NCBI.
- Plot CDS features proportionally according to genomic coordinates.
- Display forward and reverse strand orientation as directional arrows.
- Edit functional categories before figure generation.
- Optionally generate keyword-based category suggestions from product names; these are heuristic and must be reviewed by the user.
- Customize functional-category colors.
- Export the final genome map as **SVG**.
- Download the edited annotation table as CSV.
- No external JavaScript libraries are required.

## Quick start

1. Download `src/phage_genome_visualizer.html`.
2. Open the file in a modern web browser (Chrome, Edge, Firefox, or Safari).
3. Load either:
   - a CSV file with the required columns, or
   - a GenBank file downloaded from NCBI.
4. Review the CDS table and functional categories.
5. Enter or verify the genome length.
6. Click **Render genome map**.
7. Click **Export SVG** to save the publication-ready vector map.

## CSV input format

Required columns:

```text
start,end,strand,locus_tag,product,function
```

Optional column:

```text
protein_id
```

`strand` can be written as `1`, `-1`, `+`, `-`, `Forward`, or `Reverse`.

Example:

```csv
start,end,strand,locus_tag,protein_id,product,function
595,1062,-1,ESKpn_CDS0002,YCJ05049.1,single strand DNA binding protein,"DNA, RNA and nucleotide metabolism"
11650,11865,1,ESKpn_CDS0017,YCJ05064.1,holin,lysis
```

A complete example dataset is available in `example_data/ES-Kpn13_example.csv`.

## Using a GenBank file from NCBI

Download the desired nucleotide record from NCBI in **GenBank format** and load the resulting `.gb` or `.gbk` file into the tool. The parser reads CDS coordinates, strand orientation, locus tags, protein IDs, and product annotations when available.

GenBank does not provide a universal standardized field corresponding to the functional module categories used in every phage study. Therefore, functional categories are **editable by the user**. The optional category-suggestion function is based only on simple product-name keywords and should not be treated as an automated functional annotation method.

## Example output

`example_output/ES-Kpn13_genome_map.svg` contains an example genome map for *Klebsiella* phage ES-Kpn13.

## Reproducibility

For a publication, preserve the exact input annotation file or CSV used to generate the figure together with the version/release of this repository. A GitHub release can be archived in Zenodo to obtain a DOI for a specific software version.

## Development note

This tool was developed by Berna Erdoğdu with assistance from OpenAI ChatGPT for code generation and refinement. The author reviewed and adapted the code for bacteriophage genome visualization and is responsible for its validation and scientific use.


## License

MIT License. See the repository `LICENSE` file.

## Citation

Citation information is provided in `CITATION.cff`. After a software release is archived in Zenodo, the DOI can be added to both `CITATION.cff` and this README.
