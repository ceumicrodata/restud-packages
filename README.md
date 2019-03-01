# Processing backlog or replication packages for the Review of Economic Studies
## Where we are now
Replication packages for each accepted manuscript are stored in a ZIP file on Dropbox, with mostly consistent naming conventions. These ZIP files are created manually and uploaded to the publisher's website.
## Where we want to be
All packages stored on https://zenodo.org/ with metadata and DOI so that they are citable. Those packages that are small enough should also be on https://github.com/restud-replication-packages
## User stories
- As a _reader_, I want to be able to _browse_ replication packages easily, so that I get _inspired_ for doing similar work.
- As a _data editor_, I want to _accept GitHub repos_ as submissions so that I can _encourage tech savvy authors_ to submit.
- As a _production manager_, I want _easy upload_ to our repos so that I _don't make any mistakes_ during manual work with ZIP files.
- As an _author_, I want the _submission process to be smooth_ so that I can _focus on my research_.
- As a _reader_, I want to have _precise citation_ (inlcuding DOI) easily availabe so that I can _give credit_ to researchers.

## Tasks
- Explore Github and Zenodo API.
- Explore folder and file structure in Restud backlog.
- Build a datastore of metadata of replication packages. (zenodo UI? submisssion form in .docx format? new, structured submission form?)
- Develop/test tool to upload ZIP files to GitHub as new repos.
- Develop/test tool to pull these repos over to Zenodo and publish them with a DOI.

## Workflow
### For existing packages
1. Scipt prepares packages and metadata and stores them in a staging area
2. User manually checks and edits all metadata and approves packages. UI: .csv file or Google Spreadsheet
  - request edits from authors?
3. Script requests DOI for each package and saves them in metadata in staging area
4. Script uploads small packages to github (creating a release) and zenodo 
5. Script uploads large packages to zenodo, entering a simple README.md with metadata, doi and link to zenodo on github

## For new packages
1. Author filles in sctructured submission form. UI: jotform or similar
2. Metadata and package enter staging area (what backend to use?)
3. Data Editor reviews package
4. Script uploads to github and zenodo
