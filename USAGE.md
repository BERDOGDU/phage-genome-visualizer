# Usage notes

## Recommended workflow for a publication

1. Curate the final genome annotation used in the study.
2. Export or prepare a CSV containing CDS coordinates, strand orientation, locus tags, product annotations, and the functional category scheme reported in the manuscript.
3. Load the CSV into `phage_genome_visualizer.html`.
4. Verify the genome length and functional categories.
5. Render the map and export it as SVG.
6. Keep the exact input CSV together with the software release used for the publication.

## Functional categories

The software does not claim that functional module assignments are inherent GenBank fields. Categories are supplied or reviewed by the user. This is intentional so that the visualization reflects the annotation strategy described in the associated study.

## GenBank import

GenBank import is provided as a convenience for extracting CDS-level coordinates and product annotations. Because phage records differ in annotation depth, users should verify imported features before producing a final scientific figure.
