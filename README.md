# ads-bib-tools
Tools for generating human-readable bibtex output from ADS libraries.

## Scripts

#### disambiguate-ads-bib

The ADS web interface allows users to specify a custom export key format (e.g. Author1Author2Year), but does not automatically produce unique keys or even check that the fields used to populate the key consist of bibtex-compatible characters. This tool finds and disambiguates repeated keys by appending the first two words from the entry's title. It also removes forbidden characters from the key.

Usage: bash disambiguate-ads-bib /path/to/bibfile.bib

Instructions: In the ADS web interface, under Account > Customize Settings set "BibTeX Default Export Key Format" to %2H%Y and set "BibTeX Default Export Max Authors" and/or "BibTeX Default Author Cutoff" as desired. Then, export and save the ADS library in bibtex format; run disambiguate-ads-bib on the bibtex file.
