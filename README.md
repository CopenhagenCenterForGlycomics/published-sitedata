# Build template recipes for site data

## BUILD

Build the recipes (expanding out variables etc) for the various data sources.

## TEST

For each of the built recipes, do a test run, extracting 100 lines of each source and 
then checking that it matches a given manifest

## DEPLOY RECIPES and DEPLOY CODE

Deploy the recipes and the code to generate the data. The code gets a version on deploy, the manifests get MD5s, and the original data gets an MD5. If the code / manifest / data
combined checksum is different, we need to re-run the generation of the data. Code updates
should be infrequent.