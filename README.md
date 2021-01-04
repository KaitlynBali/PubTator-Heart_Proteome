# PubTator_Heart_Proteome

## Project Goal
My goal in this fall quarter project was to discover if there were any shortcomings associated with PubTator Central and its method in identifying cardiac proteins present in scientific literature. 

## Who I am
I am a second year undergraduate student studying at the University of California, Los Angeles. I am a part of the UCLA Integrated Data Science Training in Cardiovascular Medicine Program under the mentorship of Dr. Peipei Ping and Dr. Harry Caufield.  

## Requirements
1. BioPython was installed in this project. Here is a like to their website: https://biopython.org/
   - (In this project, BioPython's Entrez and Medline packages were used. The xml.dom.minidom module, xml.etree.ElementTreem module, csv module, and Python's request package         were all also imported.)
    
2. One must also remember to include their own email address in the 10th line of code: this enables NCBI to contact the user if something does not occur correctly. 

3. List of gene IDs for elevated genes in the human heart (one can seen in the code that I have named mine "heart_tissue_gene_ids - Sheet1.csv").
   - (1) First access The Human Protein Atlas. Here is a link to the website: https://www.proteinatlas.org/ .
   - (2) Click on "Tissue Atlas" and then "Heart" and then "387" and then "Custom TSV/JSON" .
   - (3) Unselect the default options in "Evidence" and "Gene" and only select for "Uniprot accession" under "Gene" .
   - (4) Download as a TSV file and simply copy and paste information into "Provide your identifiers" section under "Retrieve/ID mapping" on UniProt website (here is a link to 
        the website: https://www.uniprot.org/ ) .
   - (5) Under "Select Options" convert from "UniProtKB AC/ID" to "Entrez Gene (Gene ID)".
   - (6) Copy and paste the gene IDs into Google Sheets or Microsoft Excel and download as a csv.
    
## Running the first time
There is just one file. It is a Python Notebook. 

## Summary of work
Dr. Caufield had already provided me with the code that essentially obtained PubTator annotations for a sample of abstracts from PubMed and full-texts from PubMed Central pertaining to the human heart. The name of the file that contains the PubMed abstracts is "cardiac_absts.txt", and its PubTator annotations file name is "cardiac_absts_pubtator_annotations.xml". The name of the file that cotains the PubMed full-texts is "cardiac_fulltexts.xml", and its PubTator annotations filename is "cardiac_fulltexts_pubtator_annotations.xml". Referencing small portions of the annotation files allowed me to quickly check to see if my methods for my next tasks were working correctly.

Dr. Caufield had also provided me with the code that reported the proteins found across all the abstract annotations and the number of times these protein names occured. The code also reported the same data per individual abstract annotation document. Furthermore, the code also reported the proteins found across all the full-text annotations and the number of times these protein names occured, in addition to reporting the same data per individual full-text annotation document.

One of my tasks included modifying this code so that all the proteins were reported by their gene IDs for a more condensed list and for easier comparison in the next task. I had simply changed the XML path associated with this code along with one line in the "for loop" in order to complete this succesfully. I had also stored the gene IDs from the abstract annotations and the gene IDs from the full-text annotations into two different arrays for my next task of finding the intersection of gene IDs obtained from the The Human Protein Atlas with each of these two gene IDs lists that I had just obtained. 

The last part of this project includes simple code that I wrote to find the intersection of The Human Protein Atlas gene ID list with the list of gene IDs from the abstract annotations, and the intersection of The Human Protein gene IDs list with the list of gene IDs from the full-text annotations. This is the information I needed to obtain to perform my analysis. 
