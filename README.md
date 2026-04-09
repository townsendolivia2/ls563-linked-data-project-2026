# ls563-linked-data-project-2026
## Description
This project attempts to link costumes created by high fashion designers to the dance works they were created for and the choreographers who created the dance works in which the costumes were featured. 

## Ontologies and Controlled Vocabularies Used
For this project, I used schema.org and Wikidata.

## Linking Strategy
All designers and choreographers were linked to Wikidata to disambiguate the identity of each entity. Names of costumes were kept as literals because those entities did not have Wikidata identifiers. Dance works were kept as literals because most did not have Wikidata identifiers. Additionally, many of the dance works in this dataset are reiterations or reimaginings of dance works with the same name but created by a different choreographer, or in some cases, dance works by the same choreographer were restaged using different costumes or produced by different companies. All properites which had Wikidata identifiers were linked to Wikidata to disambiguate its identity. Attempts were made to link costume materials and design techniques to the Getty AAT, but inconsistent server connection made these linkages impossible, so those properties were removed. 

Not all costumes were linked to the dance works they were featured in because not all dance works were included in the dataset. Similarly, not all designers were linked to the costumes they created because some costumes were not included in the dataset. These omissions were not intentional, but a result of the lack of information available about the costumes and dance works I was attempting to link. All costumes, dance works, choreographers, and designers which could be linked were linked through triples at the bottom of the file.

## Example Triples
cos:6      schema:producer  wd:Q2881198 ;
        schema:creator   wd:Q242868 ;
        schema:name      "Wicked Stepmother's Trenchcoat" ;
        rdf:type         schema:CreativeWork .
dw:9      schema:contributor  wd:Q242868 ;
        schema:producer     wd:Q2881198 ;
        schema:creator      wd:Q477891 ;
        schema:name         "Snow White" ;
        rdf:type            schema:CreativeWork .
des:7      schema:hasOccupation  wd:Q3501317 ;
        schema:mentor         wd:Q3158853 ;
        schema:mentor         wd:Q299211 ;
        schema:brand          wd:Q3173870 ;
        schema:birthPlace     wd:Q467132 ;
        rdf:type              schema:Person .
