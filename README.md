# dewatra-vessel-data-challenge

Information about the DeWaTra Operational Vessel Data Challenge.

## General Information

Welcome to the public repo of the DeWaTra Operational Vessel Data Challenge! You can find general description about the challenge and its objectives on the [DeWaTra page](https://dewatra.eu/operational-vessel-data-challenge/). You can also find contact information for questions and issues there.

This repo is intended to clarify recurring questions, rules, and other practical topics about the challenge.

## Dataset and Anonymization

The challenge dataset contains operational and environmental measurements from a single vessel. To protect the identity of the vessel and data owner, identifying information such as the IMO number has been removed and timestamps have been shifted.

The dataset will be shared privately with registered contestants. Some continuous periods have intentionally been withheld as a private validation dataset, so gaps in the provided time series should not automatically be interpreted as missing data. Other gaps and missing measurements may still occur naturally in the source data.

Please treat the supplied data as private and do not commit, upload, or otherwise publish the dataset in public repositories. Public repositories can still be used for code, documentation, data-cleaning contributions, and other challenge-related development, but the supplied vessel data itself should remain private.

## Data Features and Conventions

The notebook [data_conventions.ipynb](data_conventions.ipynb) is intended to clarify common questions about the features and data conventions. We are continuously updating it based on questions received from contestants. If anything about how to interpret the features is unclear, you are encouraged to open an issue, and we will update the notebook with an answer to your question. If you prefer to keep your identity anonymous, you can email the organizers directly. That said, if the answer is relevant for the other contestants, they will be made public within the reference notebook.

## Collaborative Data Quality Assurance

The dataset comes from real vessel operations and may contain missing, inconsistent, or otherwise questionable measurements. We encourage contestants to explore the data and report useful checks and corrections to the public repository, so that broadly applicable improvements can benefit the industry and remain available for reuse when working with real vessel data. This will avoid duplicating the same data-quality work across teams and keep the competition focused on developing good models rather than on different teams spotting the same data issues.

### Missing Data and Gaps

Teams are free to decide what kind of treatment they want to apply to missing data, if any. If you think any gaps could be addressed by using vessel identifying information, such as AIS or weather hind cast data, please raise it privately with the organizers rather than attempting to identify the vessel. We will investigate and contribute a correction or additional information where possible. Choices such as aggregation, feature construction, normalization, and other model-specific preprocessing remain up to each team.

### Inaccurate and Erroneous Measurements

The distinction between inaccurate versus erroneous measurements is not always clear when the dataset measurements is our only source of information. In principle, we will leave teams to decide how to handle measurements that are seemingly inaccurate. On the other hand, if you find measurements that are physically erroneous, please do the following:

1. Raise an issue in this repository explaining the finding.
2. The organizers will apply a filter condition to remove the erroneous data, then publish the condition on the [data_quality.ipynb](data_quality.ipynb) notebook.
3. Accepted filters will later be frozen into a common data cleaning convention. The same convention will be applied by the organizers when preparing the private dataset for model evaluation.
4. Teams will decide separately how to address any gaps left by removing the erroneous data, e.g., replace it with a median, leave it empty, etc.

Again, if you think the erroneous measurements can be replaced with better ones by using vessel identifying information, please raise it privately with the organizers.

## Permitted Information

Contestants are free to use the information provided with the challenge and general domain knowledge when developing their models. However, the vessel has been intentionally anonymized, and contestants should not attempt to identify the vessel or its operator, or use vessel-specific information obtained by doing so.

Models should not rely on future observations when making a prediction. Additional guidance on the use of external information may be provided as the challenge develops.

## Coming Later

* Treatment of non-stationary/transient operating periods.
* Model submission.
* Rules and metrics for model evaluation.
