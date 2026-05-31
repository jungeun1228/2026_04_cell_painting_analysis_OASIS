# 2026_04_cell_painting_analysis_OASIS

This repository is to build cell painting analysis workflow using the Axiom OASIS imaging data. The raw data file was retrieved from Ewald et al. (2026): https://github.com/jessica-ewald/2024_09_09_Axiom_OASIS

GitHub notebook preview may fail due to file size.
View rendered notebook on NBViewer:
https://nbviewer.org/github/jungeun1228/2026_04_cell_painting_analysis_OASIS/blob/main/Cell_painting_analysis_OASIS.ipynb


### [Workflow]  
### Preprocessing
1. Feature-level/well QC, feature scaling and PCA
2. Plate-level normalization (batch correction)
3. Feature selection
4. Replicate aggregation

### Downstream analysis
1. UMAP using the highest test concentration
2. Hit selection based on Mahalanobis distance
3. Cosine similarity/clustering for hit compounds
4. Dose-response modelling for hit compounds - Mahalanobis distance and cell count
5. Specificity analysis to differentiate specific phenotypic changes from cytotoxicity

### What can be improved?  
1. tcplfit2-style multi-model fitting (Hill, exponential, polynomial): apply diverse models for model fitting and choose the best model individually for each compound  help determine effect concentrations for more compounds 
2. feature-level BMC (based on individual morphological feature) c.f. global BMC (used for this project; higher information loss)
 
### References
Anthropic. 2026. Claude. Anthropic PBC, San Francisco, CA. Available at: https://claude.ai/?utm_source=chatgpt.com (accessed in May 2026).  
Cimini, B. et al. 2023. Cell Painting Wiki. Carpenter-Singh Lab. Available at: https://github.com/carpenter-singh-lab/2023_Cimini_NatureProtocols/wiki.  
Ewald, J., Titterton, K., Bäuerle, A. et al. 2026. Cell Painting for cytotoxicity and mode-of-action analysis in primary human hepatocytes. Cell Systems.  
Moshkov, N., Becker, T., Yang, K., Horvath, P., Dancik, V., Wagner, B., Clemons, P., Singh, S., Carpenter, A., and Caicedo, J. 2023. Predicting compound activity from phenotypic profiles and chemical structures. Nature Communications 14, 1967.  
OpenAI. 2026. GPT-5, ChatGPT model. OpenAI, San Francisco, CA. Available at: ChatGPT (accessed in April 2026).
