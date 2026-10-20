# dewatra-vessel-data-challenge

Information about the DeWaTra Operational Vessel Data Challenge.

## General information

Welcome to the public repo of the DeWaTra Operational Vessel Data Challenge! You can find general description about the challenge and its objectives on the [DeWaTra page](https://dewatra.eu/operational-vessel-data-challenge/). You can also find contact information for questions and issues there.

This repo is intended to clarify recurring questions, rules and other practical topics about the challenge.

## Dataset and anonymization

The challenge dataset contains operational and environmental measurements from a single vessel. To protect the identity of the vessel and data owner, identifying information such as the IMO number has been removed and timestamps have been shifted.

The dataset will be shared privately with registered contestants. Some continuous periods have intentionally been withheld as a private validation dataset, so gaps in the provided time series should not automatically be interpreted as missing data. Other gaps and missing measurements may still occur naturally in the source data.

Please treat the supplied data as private and do not commit, upload, or otherwise publish the dataset in public repositories. Public repositories can still be used for code, documentation, data-cleaning contributions, and other challenge-related development, but the supplied vessel data itself should remain private.

## Data quality and collaborative cleaning

The dataset comes from real vessel operations and may contain missing, inconsistent, or otherwise questionable measurements. We will contribute some initial quality checks where possible, but we encourage contestants to explore the data and contribute useful checks and corrections to the public repository, so that broadly applicable improvements can benefit everyone.

This collaborative effort is focused on quality control and correction of the raw measurements. This includes, for example, identifying invalid or corrupted measurements and proposing generally applicable corrections. Choices such as aggregation, feature construction, normalization, and other model-specific preprocessing remain up to each team.

Our intention is to avoid duplicating the same data-quality work across teams and keep the competition focused on developing good models rather than on who happens to spot a particular data issue first. At the same time, we hope the shared cleaning work will leave a useful contribution from the challenge that participating teams and the wider industry can reuse when working with real vessel data. This reflects the collaborative data-quality philosophy of the challenge.

Some issues may require information that has intentionally not been disclosed as part of the vessel anonymization. Identifying information has deliberately been removed from the challenge data. If you identify a problem that could potentially be investigated using the vessel's actual position or other identifying information, please raise it privately with the organizers rather than attempting to identify the vessel. We will investigate and contribute a correction or additional information where possible.

At a later stage of the challenge, organizer-accepted raw-data quality checks and corrections will be frozen into a common cleaning convention. The same convention will then be applied by the organizers when preparing the withheld data used for model evaluation. This keeps the treatment of the raw data consistent while leaving each team free to develop its own preprocessing and modelling approach. The withheld dataset is designed to assess generalization to unseen periods of operation.

## Permitted information

Contestants are free to use the information provided with the challenge and general domain knowledge when developing their models. However, the vessel has been intentionally anonymized, and contestants should not attempt to identify the vessel or its operator, or use vessel-specific information obtained by doing so.

Models should not rely on future observations when making a prediction. Additional guidance on the use of external information may be provided as the challenge develops.

## Coming later

* Treatment of non-stationary/transient operating periods.
* Rules and mterics for model evaluation.
