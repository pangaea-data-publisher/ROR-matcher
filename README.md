# Tools to enrich PANGAEA's institution table with ROR identifiers

Uses ROR APIs provided by ROR

## IPYNB FILES

- Query_match.ipynb - code used for query matching
- Aff_match.ipynb - code used for affiliation matching
- Aff_match_num_params.ipynb - calculation of number of parameters used in affiliation matching


## (Output files - not yet included)
CSV FILES
- institutions_Affil_m.csv - result of affiliation matching 
- institutions_Affil_m_aff_list.csv result of affiliation matching + a column with a list of affiliation terms "aff_list"

## Input CSV file contains initial columns: 
- id_institution
- abbreviation
- name
- city
- contact
- country
- fax
- phone
- state
- street
- uri
- uri_semantic
- id_institution_type
- id_user_created

## After matching the following columns are added:

- aROR_id:                    ROR_id received by affiliation matching
- Nparams:                  Number of parameters used for creation of affiliation string
- Aff_list:                     List of affiliation parameters
- chosen:                      API binary indicator (based on score)
- score:                        API matching confidence score, with values between 0 and 1 (inclusive)
- matching_type:       type of matching algorithm applied
- substring:                 substring of the affiliation field, to which organization was matched
- ROR_name:             Name from the ROR database
