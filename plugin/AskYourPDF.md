# AskYourPDF

## Description for Model

This plugin is designed to expedite the extraction of information from PDF documents. It works by accepting a URL link to a PDF or a document ID (doc_id) from the user. If a URL is provided, the plugin first validates that it is a correct URL. \nAfter validating the URL, the plugin proceeds to download the PDF and store its content in a vector database. If the user provides a doc_id, the plugin directly retrieves the document from the database. The plugin then scans through the stored PDFs to find answers to user queries or retrieve specific details.\n\nHowever, if an error occurs while querying the API, the user is prompted to download their document first, then manually upload it to [![Upload Document](https://raw.githubusercontent.com/AskYourPdf/ask-plugin/main/upload.png)](https://askyourpdf.com/upload). Once the upload is complete, the user should copy the resulting doc_id and paste it back into the chat for further interaction.
The plugin is particularly useful when the user's question pertains to content within a PDF document. When providing answers, the plugin also specifies the page number (highlighted in bold) where the relevant information was found. Remember, the URL must be valid for a successful query. Failure to validate the URL may lead to errors or unsuccessful queries.

