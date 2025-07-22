# AI Model Catalog Repository Template

This is a template for documenting and cataloging AI model metadata according to the recommendations in Smithsonian's AI Handbook.

## How to Use This Template

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


# Smithsonian AI Model Catalog Entry: [Model Name]

## 1. Model Information

- **Model Name**: [Unique identifier or name of the AI model]
- **Version**: [Version number to track updates and changes]
- **Description**: [Brief overview of the model's purpose and functionality]
- **Type**: [Classification: LLM, vision model, multimodal, etc.]
- **Release Date**: [When this version was released]
- **Developer/Owner**: [Individual or team responsible for the model]

### Quick Stats
- **Total Parameters**: [Number]
- **Training Dataset Size**: [Size]
- **Primary Metric**: [Metric]: [Value]
- **Last Updated**: [Date]

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
[How the model will be maintained]

### Responsible Parties
[Who maintains the model]

### Update Frequency
[Expected cadence of updates]

### Retraining Criteria
[Conditions that would trigger retraining]

### Version History
See [CHANGELOG.md](CHANGELOG.md) for detailed version history.

## 12. Reproducibility Information

### Code Repository
- **Main Repository**: [This repository URL]
- **Training Code**: [Link to training code if separate]

### Reproduction Steps
See [Reproducibility Guide](docs/technical-specs.md) for detailed instructions.

### Seeds and Constants
[Random seeds and fixed parameters used]

### Validation Approach
[How results were validated]

### Institutional Review
[Details of any internal review process completed]

