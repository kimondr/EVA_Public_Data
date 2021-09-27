# EVA Public Dataset
Aggregated and deidentified COVID-19 RT-OCT testing results from different tourist profiles arriving in Greece in Summer 2020

## Data Aggregation
Due to the identification risk from releasing data with fine granularity (including age group, gender, date of entry), we use the [“Safe Harbor” method for deidentification](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html) and 
* we group every 2 consecutive days and define 2-day epochs (**epoch_dates**), 
* aggregate over **epoch**, country of origin (**country**), point of entry (**point_entry**),
* for all (epoch, country, point_entry) entries for which the total number of Arriving Travelers is less than 25, we replace the country name with "Other",
* delete all entries, with country name "Other" for which the total number of Arriving Travelers is less than 25.

We hereby release this (deidentified) dataset that contains for each period (defined as two consecutive days), country and point of entry the following aggregated data:
- number of scheduled arrivals (**numSchedArrivals**),
- number of performed tests (**numTestsPerformed**),
- number of travelers found positive (**numPositivesFound**),
- number of tests allocated by Eva (**numTestsAlloc**),
  
## Granular Data Availability
The finer granularity dataset that includes the travelers' age group and region of origin has a high identifiability risk and is therefore protected by GDPR. This data is controlled by the Greek Ministry of Civil Protection (Controller) and the Greek Minisry of Digital Governance (Processor). Access to this dataset can only be granted by the Controller and the Processor for research that is conducted in the public interest in the area of public health (GDPR Recital 159) for scientific purposes (GDPR Article 89).

## Potential Use Cases
Among other things, our data could be used to:
* better understand cross-country variation in asymptomatic traveler populations across the world,
* evaluate alternative reinforcement learning strategies for healthcare applications,
* better understand the impact of operational constraints on the effectiveness of COVID-19 testing.

## Citing our work
If you use this data, we request that you cite the associated research paper (citation given below), which documents the mathematical details of the Eva algorithm as well as empirical evidence that supports the effectiveness of Eva in the summer of 2020. Note that this data does not exactly replicate the results in our paper since some rows and features have been excluded in the deidentification process described above.

```
@article{bastani2021Efficient,
  title={Efficient and Targeted COVID-19 Border Testing via Reinforcement Learning},
  author={Bastani, Hamsa and Drakopoulos, Kimon and Gupta, Vishal and Vlachogiannis, Jon and Hadjicristodoulou, Christos and Lagiou, Pagona and Magiorkinis, Gkikas and Paraskevis, Dimitrios and Tsiodras, Sotirios}, 
  year={2021},
  month={Sept.},
  url={https://doi.org/10.1038/s41586-021-04014-z}, 
  journal={Nature}
}
```

