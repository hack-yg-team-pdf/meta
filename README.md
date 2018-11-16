# meta
project planning

Components:

* form review - how many are form-fillable, how have a destination? digital or otherwise? how many are _not_ intended to be handed to the government? (e.g. notice of termination of tenancy)
* scraper for [all of YG's forms](http://www.gov.yk.ca/forms/all.html)

* devise a JSON schema that can capture all form data
* PDF -> JSON automated data parsing piece (for form-fillable PDFs, can we go the whole way with [pdfminer](https://github.com/euske/pdfminer)?)
* Human PDF -> JSON conversion pipeline involves having humans tag PDF structure
  * we need to render PDFs in the brower; is [PDF.js](https://mozilla.github.io/pdf.js/) the tool for us?
* JSON -> Web Former renderer (can we reuse [DOBT's formrenderer](https://github.com/dobtco/formrenderer-base))? Another [DOBT component](https://github.com/dobtco/formbuilder) has details on JSON structure 
* catalogueing piece for the eventual web-form
