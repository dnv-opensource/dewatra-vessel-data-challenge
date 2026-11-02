# dewatra-vessel-data-challenge

Information about the DeWaTra Operational Vessel Data Challenge.

## General information

Welcome to the public repo of the DeWaTra Operational Vessel Data Challenge! You can find general description about the challenge and its objectives on the [DeWaTra page](https://dewatra.eu/operational-vessel-data-challenge/). You can also find contact information for questions and issues there.

This repo is intended to clarify recurring questions, rules and other practical topics about the challenge.

## Dataset and anonymization

The challenge dataset contains operational and environmental measurements from a single vessel. To protect the identity of the vessel and data owner, identifying information such as the IMO number has been removed and timestamps have been shifted.

The dataset will be shared privately with registered contestants. Some continuous periods have intentionally been withheld as a private validation dataset, so gaps in the provided time series should not automatically be interpreted as missing data. Other gaps and missing measurements may still occur naturally in the source data.

Please treat the supplied data as private and do not commit, upload, or otherwise publish the dataset in public repositories. Public repositories can still be used for code, documentation, data-cleaning contributions, and other challenge-related development, but the supplied vessel data itself should remain private.

## Data features and conventions

The notebook [data_conventions.ipynb](data_conventions.ipynb) is intended to clarify common questions about the features and data conventions. We are continuously updating it based on questions received from contestants. If anything about how to interpret the fetures is unclear, you are encouraged to open an issue, and we will update the notebook with an answer to your question. If you prefer to keep your identity anonymous, you can send an email to the organizers directly. That said, if the answer is relevant for the other contestants, they will be made public within the reference netebook.

## Collaborative data quality assurance

The dataset comes from real vessel operations and may contain missing, inconsistent, or otherwise questionable measurements. We encourage contestants to explore the data and report useful checks and corrections to the public repository, so that broadly applicable improvements can benefit the industry and remain available for reuse when working with real vessel data. This will avoid duplicating the same data-quality work across teams and keep the competition focused on developing good models rather than on different teams spotting the same data issues.

The steps are the following:
1. If you identify erroneous measurements, raise an issue explaining the finding. Feel free to propose a correction or filter.
2. The organization will consider the proposal and add relevant ones to the [data_quality.ipynb](data_quality.ipynb) notebook.
3. Accepted corrections will later be frozen into a common data cleaning convention. The same convention will be applied by the organizers when preparing the withheld data for model evaluation.
4. Choices such as aggregation, feature construction, normalization, and other model-specific preprocessing remain up to each team.

If you identify a problem that could potentially be corrected using the vessel's position or other identifying information, please raise it privately with the organizers rather than attempting to identify the vessel. We will investigate and contribute a correction or additional information where possible.

## Permitted information

Contestants are free to use the information provided with the challenge and general domain knowledge when developing their models. However, the vessel has been intentionally anonymized, and contestants should not attempt to identify the vessel or its operator, or use vessel-specific information obtained by doing so.

Models should not rely on future observations when making a prediction. Additional guidance on the use of external information may be provided as the challenge develops.

## Coming later

* Treatment of non-stationary/transient operating periods.
* Model submission.
* Rules and metrics for model evaluation.
