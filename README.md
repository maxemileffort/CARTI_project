# Cancer Patient Network Fidelity

## Background

Hospital administration was tasked with deciding if it made sense to replace their linear accelerator (LA), a tool that is used to fight cancerous tumors using radiation therapy. The assumption was that the market they were in was going out of network because the out of network equipment was newer, more up-to-date. In an effort to keep patients in network, did it make sense for this hospital to buy a newer LA? Depending on the model, the cost of such a device can range anywhere from $500k to several millions. Naturally, before making such a big decision, it helps to look at some data.

## Method

In partnership with a data aggregator, we examined claims data for patients residing in the zip codes surrounding the target market. We looked for the diagnosis code 'Z51.0' (Encounter for antineoplastic radiation therapy) to appear anywhere in the 26 diagnosis codes possible on a claim, as well as any of the dozens of possible procedure codes linked to LA usage. The claims data was ingested into RedShift and made accessible to us to query. The actual query can be found in this repo.

## Results

What we found was that patients were leaving the market at a much lower rate than what was assumed (a good thing). Very few patients across any of the contracts that we care manage were leaving. Because of that, it made sense for the hospital administration to hold off on purchasing a new LA. 

## Other analysis

Still, there were some interesting findings. Of the patients that were leaving, when they left for radiation therapy, the almost always ended up on chemo instead. And while on chemo, they would stay with that out of network provider for the majority of their claims related to their cancer treatments. This sparked a conversation about what could be done to retain those patients, but was beyond the scope of this analysis.

## Notes

In this repo, the .txt file houses the query I used on RedShift to generate the underlying data for this analysis.

For the 2 PDFs, the Final version is the version I presented to my more technical manager, so that she could see my methods and be sure of the results.

The Final - Abridged is the version that the stakeholders saw, as a more high level summary of the information that they were after.
