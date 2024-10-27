# wasserstoff-AiIntern-Task

## Project: PDF Processing Pipeline
## Goal:
* Develop a dynamic pipeline to ingest PDF files from a given folder, summarize documents, and extract domain-specific keywords. Store results in a MongoDB database.
* Custom implementations over pre-built pipelines should be favored to increase concurrency, speed, and innovation.
## Main Features:
### PDF Ingestion:
* It ingests multiple PDFs from a given folder path.
* Handles short, medium, and long-length documents.
* Parallel processing for document handling.
### MongoDB Storage:
* Stores initial metadata about every PDF document document name, path, size etc.
* It updates the records in MongoDB with the self-generated summary and keywords, when processed

### Text Summarization:
* This algorithm outputs abstracts based on size of PDF document. On smaller PDF documents, this algorithm outputs a very short abstrac of the text where as, on the opposite side, for larger PDF it tries to output a pretty long abstract
* The abstract style of summarization is designed and left open with scope for future improvements in the future

### Keyword Extraction:
* This algorithm generates specific, domain-specific keywords in the document using TF-IDF. This captures essential ideas or themes

### JSON Formatting:
* JSON returned summaries and keywords are stored in MongoDB. Handling errors when the PDF is not supported or corrupted in order not to corrupt the data.

### Concurrency & Performance:
* The concurrent process for handling multiple PDFs by multiplexing large files and documents in high volume. It will be measured in both processing time and scalability performance.
