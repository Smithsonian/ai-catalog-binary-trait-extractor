# Binary Trait Extractor for Pedicularis

This repository documents a pipeline for extracting structured morphological traits from botanical species descriptions using large language models. It follows the Smithsonian AI Model Catalog format. 

## How to Use This Repository

### Quick Start
1. **Click "Use this template"** on GitHub to create your own repository
2. **Rename your repository** to `ai-catalog-[your_model_name]`
   - Example: `ai-catalog-fern-classifier` or `ai-catalog-canopy-segmentation`
   - Avoid generic names like `ai-catalog-my-model`
   - Use specific names that reflect the model's purpose or domain
   - This helps with organization and searchability in the catalog
   - **Important**: Do not include spaces or special characters in the name
   - Use hyphens to separate words for readability
3. **Clone your repository** to your computer
4. **Fill out the README.md** with your model's information
5. **Complete the model card** in the docs folder
6. **Commit and push** your changes

### How to Rename Your Repository
After creating from template:
1. Go to your repository **Settings** tab on GitHub
2. Scroll to **"Repository name"** section
3. Change name to: `ai-catalog-[your_model_name]`
4. Click **"Rename"** button
5. Update the title in README.md to match

## Files Included

### README.md
 - Complete template for Smithsonian AI Model Catalog standards. This file serves as the main documentation for your AI model. Fill in the sections with relevant information about your model, including its purpose, performance metrics, intended uses, and technical specifications.

### LICENSE
 - Choose appropriate license for your model and documentation

### CHANGELOG.md
 - Template for tracking version changes

## Setup Guide

### Initial Setup
1. **Create from template** - Use GitHub's "Use this template" button
2. **Rename repository** to `ai-catalog-[your_model_name]`
3. **Clone to your computer**
4. **Complete documentation**

### Customization Checklist
- [ ] Rename repository to `ai-catalog-[model_name]`
- [ ] Update README.md title and all placeholders
- [ ] Complete documentation sections to the best of your ability
- [ ] Add usage examples if any
- [ ] Set appropriate license
- [ ] Add contact information
- [ ] Create initial CHANGELOG.md entry

### Tips
- **Use specific names**: `ai-catalog-bert-medical-ner` not `ai-catalog-my-model`
- **Keep it simple**: Focus on documentation, not complex infrastructure
- **Update regularly**: Keep performance metrics and version info current
- **Link to evaluation**: Reference your `ai-eval-[model_name]` repository if you have one

## Repository Directory Structure

```
ai-catalog-model-name/
├── README.md                    # Main model documentation (use template below)
├── LICENSE                      # Model licensing information
├── CHANGELOG.md                # Version history
├── docs/                       # Additional documentation
│   ├── user-guide.md          # How to use the model
│   └── technical-specs.md     # Additional technical details
├── examples/                   # Usage examples
│   └── notebooks/             # Jupyter notebooks (optional)
└── assets/                     # Supporting files
    ├── images/                # Screenshots, diagrams
    └── sample-data/           # Small sample datasets
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
- **Compute**: [CPU/GPU requirements]
- **Memory**: [RAM requirements]
- **Storage**: [Storage needs]

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
[Oversight mechanisms and responsible parties]

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
