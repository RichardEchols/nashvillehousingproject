**Nashville Housing**

![f271fc60-cb41-11e9-9a56-cf16cd66e478-how_much_are_homes_selling_for_in_my_neighborhood-ogid-122127](https://github.com/RichardEchols/nashvillehousingproject/assets/125469793/4333334f-4d1e-450b-9656-c14a9f4dbfdf)



**Background:**


In the fast-paced world of real estate, data is as valuable as the property itself. The Nashville Housing project was initiated to cleanse and refine a comprehensive housing dataset, shedding light on the market's nuances and trends. As a data analyst, I recognized the potential locked within the raw figures — the stories they could tell about growth, demand, and the shifting landscape of Nashville's community. This project was as much an exploration of data as it was of the city's heart and soul through the lens of its housing market.



**Questions:**


Several questions were at the core of this analysis, driving the data cleaning process with purpose:

* How can we ensure data accuracy and consistency across different fields such as sale dates and addresses?
* What are the patterns of vacant property sales in Nashville, and how are they recorded?
* Can we identify and eliminate redundancies to distill the dataset to its most informative and actionable elements?
* How does the segmentation of complex data fields into more granular components enhance our understanding and usability of the data?




**Main Findings:**


The meticulous cleaning process revealed:

* The dataset contained a mix of date formats that required standardization to ensure consistency for time-series analysis.
* Property addresses were sometimes incomplete or spread across multiple fields, obscuring valuable insights into geographical trends.
* The dataset included shorthand notations that, while concise, were not immediately clear without context; transforming these improved readability and interpretation.
* Duplicate records were present, which could have skewed any subsequent analysis had they not been identified and removed.




**Conclusions:**


The project concluded with several actionable outcomes:

* A standardized and consistent dataset was established, with dates formatted uniformly for accurate chronological analysis.
* By segmenting address fields and standardizing values, the data now allows for more precise geographic mapping and trend spotting.
* The cleanup process eliminated ambiguities and redundancies, providing a streamlined dataset ready for deep analytical dives and visualization.
* The refined data paves the way for a truthful exploration of the Nashville housing market, enabling data-driven decision-making for stakeholders.



**Original Dataset**


<img width="1775" alt="Screenshot 2023-11-14 at 4 23 55 PM" src="https://github.com/RichardEchols/nashvillehousingproject/assets/125469793/36a114b2-7911-460b-8979-16567bae71bc">




**Process:**

The Nashville Housing project entailed a series of SQL queries aimed at data cleaning and preparation for a housing market analysis. The process followed these steps:

**Data Assessment:**

Started with a review of the raw data from the NashvilleHousing table to understand the structure and quality of the data.


**Date Standardization:**

Modified the SaleDate field to ensure a consistent date format across the dataset using the CONVERT function.


**Address Data Validation:**

Checked for and filled in missing PropertyAddress fields by joining records on ParcelID and ensuring all properties had a valid address.


**Address Segmentation:**

Broke down the PropertyAddress into separate columns to capture street addresses and city names individually, enhancing data granularity.


**Owner Address Parsing:**

Used the PARSENAME and REPLACE functions to extract owner address components, segmenting them into individual columns for address, city, and state.


**Field Value Transformation:**

Converted shorthand notations in the SoldAsVacant field from 'Y' and 'N' to 'Yes' and 'No' for clarity and consistency.


**Duplicate Removal:**

Employed a Common Table Expression (CTE) with the ROW_NUMBER function to identify and remove duplicate records based on a set of key attributes.


**Column Pruning:**

Removed unused columns such as OwnerAddress, TaxDistrict, and PropertyAddress post-segmentation, to streamline the dataset.
Throughout each step, careful attention was given to data integrity and accuracy. The goal was to prepare a clean, well-structured dataset that could be used for in-depth analysis of the Nashville housing market, focusing on sales trends, valuation, and property turnover rates.



**The culmination of this project is a clear, concise, and accessible dataset that serves as a reliable foundation for further analysis and insights into the Nashville housing market.**
