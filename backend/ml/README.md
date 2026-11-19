# ML modules

This folder contains the machine-learning and NLP components used by SocietySelect AI.

## Workstreams

**NLP and recommendation**
- Resume text extraction
- Skill extraction
- Skill-to-requirement matching
- Candidate recommendation and ranking

**Performance and risk modelling**
- Student performance prediction
- Probation risk monitoring

Keep each component independently testable. Agree on shared input/output schemas before connecting modules to the API.

## Development order for NLP and recommendation

1. Extract text from PDF resumes with PyMuPDF.
2. Extract skills using a small, version-controlled skill vocabulary.
3. Match skills against society requirements with transparent rules.
4. Add Sentence Transformers and cosine similarity for semantic matching.
5. Combine skill match with assessment data using documented weighted scoring.
6. Evaluate results and expose stable functions through FastAPI.

## Data policy

Do not commit real resumes or personal student data. Use synthetic examples or data with suitable licenses and consent. Record the source and limitations of every dataset.
