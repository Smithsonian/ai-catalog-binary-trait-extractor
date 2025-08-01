<p align="center">
  <img src="https://github.com/madaime2/ai-catalog-binary-trait-extractor/blob/main/assets/images/Example_Dichotomous_Key_Pedicularis.png?raw=true" alt="Example Dichotomous Key" width="700"/>
</p>

# Binary Trait Extractor for Pedicularis

This repository documents a pipeline for extracting structured morphological traits from botanical species descriptions using large language models. It follows the Smithsonian AI Model Catalog format. Although this pipeline is designed for Pedicularis, its prompt-based approach makes it easily adaptable to other plant clades or non-plant groups with comparabale documentation.

## How to Use This Repository

### Quick Start
1. Clone or fork this repository to access the AI-based trait extraction pipeline
2. Install required dependencies listed in requirements.txt or the user guide
3. Prepare the input data: species descriptions in plain text or CSV format
4. Run the extraction pipelne (scripts and notebooks in examples)
5. Load the structured outputs in CSV or JSON format for subsequent ecological and evolutionary analyses 

## Files Included

### README.md
 - Core documentation describing model scope, usage, and metadata (Smithsonian AI Model Catalog Standard)

### LICENSE
 - MIT License

### CHANGELOG.md
 - Verion history and update log

## Setup Guide

### Initial Setup
1. **Clone the repository** 
2. **Set up a Python environment and install dependencies**
3. **Format species descriptions (see examples in sample-data)**
4. **Follow instructions in user guide**

### Customization Checklist
- [ ] Update README.md and metadata fields
- [ ] Adjust prompt and schema for target clade and trait set
- [ ] Add or modify usage examples
- [ ] Log changes in CHANGELOG.md

### Tips
- **Use consistent, structured input for better extraction accuracy**
- **Document trait definitions and prompt formats**
- **Update regularly**
- **Share modified pipeline by linking to this repository or citing it**

## Repository Directory Structure

```
ai-catalog-binary-trait-extractor/
├── README.md                            # Main model documentation
├── LICENSE                              # Model licensing information (MIT)
├── CHANGELOG.md                         # Version history and update log
├── .gitignore
├── examples/                            # Usage examples
│   ├── Trait_extraction_pipeline.ipynb  # Trait extraction pipeline and visualizations
│   └── Trait_extraction_pipeline.py     # Python script version of pipeline                             
├── docs/                                # Additional documentation
│   ├── user-guide.md                    # How to use the model
│   └── technical-specs.md               # Technical specifications and reproducibility
└── assets/                              # Supporting files
    ├── images/                          # Example visualizations (e.g., Dichotomous key, UMAP)
    └── Data/                            # Datasets
```
## README.md Template

*Copy this template and fill in the information to the best of your ability. Keep in mind, certain sections may not be appropriate to your use case.*


# Smithsonian AI Model Catalog Entry: Binary Trait Extractor for Pedicularis

## 1. Model Information

- **Model Name**: Binary Trait Extractor for Pedicularis
- **Version**: v1.0.0
- **Description**: This tool uses a large language model (e.g., OpenAI GPT-3.5) to extract standardized morphological traits from botanical species descriptions (i.e. taxonomic treatments). It encodes binary, numeric, and categorical traits into structured matrices that subsequently enable trait-based diversity analysis, detection of unique character combinations, and generation of dichotomous keys. 
- **Type**: LLM-based text-to-structure pipeline
- **Release Date**: 2025-07-24
- **Developer/Owner**: (Marc-Elie Adaime (Smithsonian Data Science Lab)

### Quick Stats
- **Total Parameters**: Not Applicable (uses OpenAI GPT-3.5 via API)
- **Training Dataset Size**: Not Applicable (model is pre-trained)
- **Primary Metric**: Manual trait extraction accuracy: XX% (estimated based on validation of output against expert-annotated traits)
- **Last Updated**: 2025-07-25

### Related Resources
- **Evaluation Repository**: [Link to ai-eval-model_name if exists]
- **Model Files**: [Link to model weights/files]
- **Additional Links**: [Link to additional documentation if applicable]

## 2. Intended Uses and Limitations

### Primary Intended Uses
- Extracting binary, numeric, and categorical morphological, life history, and physiological traits from botanical species descriptions using large language models
- Generating structured trait matrices for downstream analyses such as trait uniqueness evaluation, trait-based clustering (using ordination methods), and dichotomous key construction

### Out-of-Scope Uses
- Extraction of traits from poorly formatted textual sources
- Use as a substitute for expert taxonomic validation without post-processing

### Known Limitations
- Reliance on the consistency and certainty of species descriptions; results may vary with ambiguous or uncertain descriptions, as well as with highly unstructured texts
- Trait extraction depends on prompt sensitivity and the behavior of the selected LLM (e.g., OpenAI)
- The pipeline lacks confidence or uncertainty quantification in its current form

### Institutional Context
This model supports biodiversity and conservation research aligned with the Smithsonian's mission to advance understanding of natural history and evolution. It helps researchers standardize phenotypic data for a broad range of ecological and evolutionary studies.

## 3. Technical Specifications

### Algorithm and Architecture
- **Algorithm**: Prompt-based extraction using large language models (LLMs)
- **Architecture**: API calls to GPT-3.5 using structured JSON prompts and validation logic
- **Model Size**: Not applicable (model is externally hosted by OpenAI)

### Input/Output Requirements
- **Input Requirements**: Cleaned species descriptions in plain text or CSV format, consisting of English-language morphological descriptions
- **Output Format**: Structured JSON or CSV files representing trait matrices, encoding binary/numeric/categorical traits by species
- **Hardware Requirements**: Minimal for local usage (CPU); requires internet access and OpenAI API key

## 4. Training Information

### Training Data
- **Sources**: None used locally; the LLM is pre-trained on a wide corpus including scientific literature relevant to botanical descriptions
- **Dataset Size**: 352 species from the Flora of China; 45 traits 
- **Data Preprocessing**: Standardize parsing and formatting of botanical species descriptions before sending to API

### Training Procedure
- **Methodology**: No local training; inference-only pipeline via prompt engineering
- **Training Infrastructure**: Not applicable
  
## 5. Performance Metrics
 
| Metric | Value | Test Dataset | Notes |
|--------|--------|--------------|-------|
| Accuracy | [%] | [Dataset name] | [Context or conditions] |
| Precision | [%] | [Dataset name] | [For classification tasks] |
| Recall | [%] | [Dataset name] | [For classification tasks] |
| [Custom Metric] | [Value] | [Dataset name] | [Domain-specific metrics] |

### Benchmark Comparisons
No formal benchmark comparison yet; accuracy evaluated through manual revision 

## 6. Bias and Fairness Assessment

### Bias Impact Analysis
Bias may result from inconsistencies in species descriptions or biases associated with the language model itself 

### Bias Mitigations
- Use highly structured prompts and validation schemes
- Manual review of extracted traits and expert consultation when needed
  
### Remaining Concerns
Potential inconsistent performance across clades with highly variable taxonomic descriptions

### Protected Attributes
Not applicable (no personal attributes involved)

## 7. Operational Details

### Deployment Environment
- Local Python environment (Jupyter notebook / script)
- Requires access to OpenAI API (e.g., GPT-3.5)

### Dependencies
- Python 3.8+
- OpenAI
- Pandas
- Numpy
- Tqdm

### Resource Requirements
- **Compute**: CPU sufficient; No GPU required
- **Memory**: ≥4 GB RAM recommended for processing large datasets
- **Storage**: < 500 MB for output files (JSON/CSV); more if processing additional species

### Integration Points
- Can be integrated with downstream ecological and evolutionary analysis pipelines

### Monitoring Framework
- Manual run and review; no continuous monitoring currently

## 8. Governance and Compliance

### Ethical Considerations
- Pipeline does not involve sensitive data

### Risk Assessment
- Minimal risks associated with incorrect trait extraction; downstream analyses should involved expert review

### User Access Controls
- Users must supply their own OpenAI API key (if using an OpenAI model)

### Governance Framework
Oversight is provided by the pipeline developer, Marc-Elie Adaime, who is responsible for updating the code and documentation. 

## 9. Licenses and Attribution

### Model License
This model is released under [LICENSE NAME]. See [LICENSE](LICENSE) for details.

### Dataset License(s)
[Licenses covering training data]

### Required Citations
```bibtex
@misc{[binary_trait_extractor],
  title={[Binary Trait Extractor for Pedicularis]},
  author={[Marc-Elie Adaime]},
  year={[2025]},
  url={[https://github.com/madaime2/ai-catalog-binary-trait-extractor]}
}
```

### Intellectual Property Status
The code and prompt are original and developed by the author; no proprietary components included

### Third-Party Components
- OpenAI GPT-3.5
- Python open-source libraries

## 10. User Resources

### User Guide
See [User Guide](docs/user-guide.md) for detailed instructions.

### Example Implementations
- [Basic usage examples](examples/)
- [Jupyter notebooks](examples/notebooks/)

### Known Issues
- Occasional LLM hallucinations and inconsistencies in trait extraction
- Some rare traits may be missed without proper prompt engineering

### Support Contacts
- **Technical Support**: adaimem@si.edu
- **Model Maintainer**: Marc-Elie Adaime

## 11. Maintenance and Updates

### Maintenance Plan
This pipeline will be maintained through periodic updates to the codebase, prompt templates, and trait selection. Future improvements may include adopting different LLMs, expanding the trait list, and designing and running further analyses.  

### Responsible Parties
Marc-Elie Adaime

### Update Frequency
When necessary, particularly when user feedback is incoporated. 

### Retraining Criteria
Not applicable - the system relies on pre-trained LLMs (e.g., OpenAI GPT-3.5) and prompt engineering. Retraining is not currently part of the architecture/pipeline. 

### Version History
See [CHANGELOG.md](CHANGELOG.md) for detailed version history.

## 12. Reproducibility Information

### Code Repository
- **Main Repository**: https://github.com/madaime2/ai-catalog-binary-trait-extractor
- **Training Code**: Not applicable - uses OpenAI LLMs via API without fine-tuning

### Reproduction Steps
See [Reproducibility Guide](docs/technical-specs.md) for detailed instructions, including:
- How to extract and load species descriptions
- How to format trait extraction prompts
- How to run the extraction pipeline and store outputs
- How to perform various analyses, including diversity quantification 

### Seeds and Constants
N/A - No random seed control available via OpenAI's API. However, deterministic mode (temperature = 0) is used to ensure repeatability. 

### Validation Approach
Manual comparison of extract traits against-expert annotated descriptions for a subset of species.

### Institutional Review
No formal review yet. This tool is under independent development. 
