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
- **Primary Metric**: Manual trait extraction accuracy: ~90% (estimated based on validation of output against expert-annotated traits)
- **Last Updated**: 2025-07-25

### Related Resources
- **Evaluation Repository**: [Link to ai-eval-model_name if exists]
- **Model Files**: [Link to model weights/files]
- **Additional Links**: [Link to additional documentation if applicable]

## 2. Intended Uses and Limitations

### Primary Intended Uses
- [Specific use case the model was designed for]
- [Additional intended use case]


### Out-of-Scope Uses
- [Use case explicitly NOT recommended]


### Known Limitations
- [Key limitation users should be aware of]

### Institutional Context
[How this model aligns with institutional needs and mission]

## 3. Technical Specifications

### Algorithm and Architecture
- **Algorithm**: [Type of algorithm used - neural network, decision tree, etc.]
- **Architecture**: [Details about the model's architecture]
- **Model Size**: [Number of parameters, model weights size]

### Input/Output Requirements
- **Input Requirements**: [Expected input formats and constraints]
- **Output Format**: [Description of model outputs and formats]
- **Hardware Requirements**: [Computing resources needed for operation]

## 4. Training Information

### Training Data
- **Sources**: [Training data sources and composition]
- **Dataset Size**: [Number of examples/records]
- **Data Preprocessing**: [Steps taken to prepare training data]

### Training Procedure
- **Methodology**: [Training approach and hyperparameters]
- **Training Infrastructure**: [Computing resources]

## 5. Performance Metrics
 
| Metric | Value | Test Dataset | Notes |
|--------|--------|--------------|-------|
| Accuracy | [%] | [Dataset name] | [Context or conditions] |
| Precision | [%] | [Dataset name] | [For classification tasks] |
| Recall | [%] | [Dataset name] | [For classification tasks] |
| [Custom Metric] | [Value] | [Dataset name] | [Domain-specific metrics] |

### Benchmark Comparisons
[Performance against standard benchmarks in the domain]

## 6. Bias and Fairness Assessment

### Bias Impact Analysis
[Performance variation across different groups or classes in the model]

### Bias Mitigations
[Steps taken to address identified biases]

### Remaining Concerns
[Acknowledged limitations in bias mitigation]

### Protected Attributes
[How the model handles sensitive characteristics]

## 7. Operational Details

### Deployment Environment
[Where the model is deployed - cloud, on-premises, etc.]

### Dependencies
[Software or hardware dependencies required]

### Resource Requirements
- **Compute**: [CPU/GPU requirements]
- **Memory**: [RAM requirements]
- **Storage**: [Storage needs]

### Integration Points
[How the model connects to other systems]

### Monitoring Framework
[How the model is monitored in production]

## 8. Governance and Compliance

### Ethical Considerations
[Documentation of ethical implications and mitigations]

### Risk Assessment
[Evaluation of potential risks with the model's use]

### User Access Controls
[Authorization framework for model access]

### Governance Framework
[Oversight mechanisms and responsible parties]

## 9. Licenses and Attribution

### Model License
This model is released under [LICENSE NAME]. See [LICENSE](LICENSE) for details.

### Dataset License(s)
[Licenses covering training data]

### Required Citations
```bibtex
@misc{[citation_key],
  title={[Model Title]},
  author={[Author Names]},
  year={[Year]},
  url={[Repository URL]}
}
```

### Intellectual Property Status
[IP ownership and restrictions]

### Third-Party Components
[Any licensed components incorporated]

## 10. User Resources

### User Guide
See [User Guide](docs/user-guide.md) for detailed instructions.

### Example Implementations
- [Basic usage examples](examples/)
- [Jupyter notebooks](examples/notebooks/)

### Known Issues
[Currently identified issues or bugs]

### Support Contacts
- **Technical Support**: [Contact information]
- **Model Maintainer**: [Responsible party contact]

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
