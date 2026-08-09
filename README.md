# Analytics Workflow

This folder contains the analysis notebooks and supporting files used to collect
YouTube videos and comments, classify the resulting corpus, validate annotations,
and generate the network and process-mining outputs for the manuscript revision.

## Root Files

- `01_search_videos.ipynb`: Searches YouTube for the scientific and
  pseudoscientific terms, stores video IDs and metadata, and prepares the first
  video-level classification outputs.
- `02_extract_comments.ipynb`: Downloads video-level information, transcripts,
  and comment threads for the selected YouTube videos.
- `03_comments_classification.ipynb`: Detects comment language and classifies
  comments by emotion and thematic category using transformer-based models.
- `04_network_analysis.ipynb`: Builds directed transition networks from
  classified comments, applies category mappings and thresholds, runs
  sensitivity analyses, and exports network tables and figures.
- `05_Process_Mining.ipynb`: Prepares event logs from classified conversations
  and runs process-mining analyses to study temporal patterns in comment
  sequences.
- `06_Get_video_metadata.ipynb`: Retrieves and enriches video metadata,
  including language detection for the video-level records.
- `07_load_annotation_responses.ipynb`: Loads human annotation files and
  compares them with the automated labels, including agreement metrics and
  disagreement checks.
- `08_RandomSampler.ipynb`: Creates proportional video samples and stratified
  comment samples for manual annotation, including annotation-ready exports.
- `09_desires_insult_empty_inspection.ipynb`: Reviews non-informative comments
  and comments classified as `Insult` or `Desires`, then exports quality-check
  tables.
- `10_Count_videos.ipynb`: Counts scientific and pseudoscientific videos by
  content-classification status.
- `workflow_data_collection.md`: Mermaid diagram describing the video search,
  video screening, and validated corpus creation workflow.
- `workflow_data_processing.md`: Mermaid diagram describing comment extraction,
  NLP enrichment, filtering, and final analytical outputs.

## Data Folders

- `Data/Videos/`: Search outputs, term-level video CSV files, and sampled video
  workbooks.
- `Data/Comments/`: Evaluated comment datasets used by the classification,
  network, and process-mining notebooks.
- `Data/Anotation files/`: Manual annotation instructions, annotation samples,
  annotator responses, and root exports.
- `Data/Results/`: Generated analysis outputs, including network files,
  process-mining outputs, quality checks, archived files, and submission figures.

Run the notebooks from the project root so that the relative `Data/...` paths
resolve correctly.
