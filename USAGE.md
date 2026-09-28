# Usage notes

## Recommended workflow for a publication
1. Curate the final genome annotation used in the study.
2. Download the corresponding nucleotide record from NCBI in GenBank format (`.gb`, `.gbk`, or `.genbank`).
3. Load the GenBank file into `phage_genome_visualizer.html`.
4. Review the imported CDS features and functional categories. Non-CDS features such as `misc_feature` are reported but excluded from the CDS count and map.
5. Edit functional categories where necessary to match the annotation/classification scheme used in the study.
6. Verify the genome length, accession, and CDS annotations.
7. Download the edited CSV to preserve the exact visualization input.
8. Render the genome map and export it as SVG.
9. Keep the GenBank file, edited CSV, and software release used for the publication.

## Functional categories

The software does not claim that functional module assignments are inherent GenBank fields. Categories are supplied or reviewed by the user. This is intentional so that the visualization reflects the annotation strategy described in the associated study.

## GenBank import

GenBank import is provided as a convenience for extracting CDS-level coordinates and product annotations. Because phage records differ in annotation depth, users should verify imported features before producing a final scientific figure.

Only features annotated as `CDS` are included in the CDS count and genome map; non-CDS features such as `misc_feature` are reported separately.
