# ScholarAI

## Description for Model

Access open access scientific literature from peer-reviewed journals. The abstract endpoint finds relevant papers based on 2 to 6 keywords. After getting abstracts, ALWAYS prompt the user offering to go into more detail. Use the fulltext endpoint to retrieve the entire paper's text and access specific details using the provided pdf_url, if available. ALWAYS hyperlink the pdf_url from the responses if available. Offer to retrieve chunks of fulltext incrementally only upon request.

