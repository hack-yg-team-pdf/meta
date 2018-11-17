# #HackYG team-pdf planning workspace

## Components

Individual components of the build

* form review - how many are form-fillable, how have a destination? digital or otherwise? how many are _not_ intended to be handed to the government? (e.g. notice of termination of tenancy)

* scraper for [all of YG's forms](http://www.gov.yk.ca/forms/all.html)
  * 

* devise a JSON schema that can capture all form data
* PDF -> JSON automated data parsing piece (for form-fillable PDFs, can we go the whole way with [pdfminer](https://github.com/euske/pdfminer)?)
* Human PDF -> JSON conversion pipeline involves having humans tag PDF structure
  * we need to render PDFs in the brower; is [PDF.js](https://mozilla.github.io/pdf.js/) the tool for us?
* JSON -> Web Former renderer (can we reuse [DOBT's formrenderer](https://github.com/dobtco/formrenderer-base))? Another [DOBT component](https://github.com/dobtco/formbuilder) has details on JSON structure 
* catalogueing piece for the eventual web-form


## Canonical forms

The list of all of YG's forms are [here](http://www.gov.yk.ca/forms/all.html). Here are some forms that are illustrative and we'll focus on in our first pass

* [YG's Request for Access to Records](http://www.gov.yk.ca/forms/forms/4500/yg4552_b.pdf)
* [YG's Spring Litter Removal](http://www.gov.yk.ca/forms/forms/6500/yg6560_e.pdf)
* [YG's Licensed Pratical Nurses Full License Application](http://www.gov.yk.ca/forms/forms/6500/yg6644_e.pdf)


## S3

Most data transfer is done over S3; in the bucket `yg-pdf`; ask Ian for an access key

* `s3://yg-pdf/form_jsons` - the formatted jsons in the form format ready for display
* `s3://yg-pdf/raw_pdfs` - Scraped pdfs to be turned into jsons
