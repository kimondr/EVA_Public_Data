# EVA Public Dataset
Aggregated, Publicly Available Dataset for Project EVA

## Data Aggregation
Due to the identification risk from releasing data with fine granularity (including age group, gender, date of entry), we use the [“Safe Harbor” method for deidentification](https://www.hhs.gov/hipaa/for-professionals/privacy/special-topics/de-identification/index.html) and 
* we group every 2 consecutive days and define 2-day epochs (**epoch_dates**), 
* aggregate over **epoch**, country of origin (**country**), point of entry (**point_entry**),
* for all (epoch, country, point_entry) entries for which the total number of Arriving Travelers is less than 25 we replace the country name with "Other". 
* delete all entries, with country name "Other" for which  total number of Arriving Travelers is less than 25.
  
  
We hereby release this (deidentified) dataset that contains for each period (defined as two consecutive days), country and point of entry the following aggregated data:
- number of scheduled arrivals (**numSchedArrivals**),
- number of performed tests (**numTestsPerformed**),
- number of travelers found positive (**numPositivesFound**),
- number of tests allocated by Eva (**numTestsAlloc**),
  
## Granular Data Availability
The finer granularity dataset that includes the traelers point of entry and region of entry has a high identifiability risk and is therefore protected by GDPR.
This data is controlled by the Greek Ministry of Civil Protection (Controller) and the Greek Minisry of Digital Governance (Processor). Access to this dataset can only be granted
by the Controller and the Processor for research that is conducted in the public interest in the area of public health (GDPR Recital 159) for scientific purposes (GDPR Article 89).


## Citing our work
Team Eva has a research paper with the mathematical details of the algorithm in addition to empirical evidence from the summer of 2020 on the effectiveness of Eva. Should you use this data or need to cite that work, we politely ask you use the following citation:

```
@article{bastani2021deploying,
  title={Deploying an Artificial Intelligence System for Covid-19 Testing at the Greek Border},
  author={Bastani, Hamsa and Drakopoulos, Kimon and Gupta, Vishal and Vlachogiannis, Jon 
    and Hadjicristodoulou, Christos and Lagiou, Pagona 
    and Magiorkinis, Gkikas and Paraskevis, Dimitrios and Tsiodras, Sotirios}, 
  year={2021},
  month={Feb.},
  url={http://dx.doi.org/10.2139/ssrn.3789038}, 
  journal={SSRN}
}
```

