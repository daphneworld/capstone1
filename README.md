# Can a parent predict the safety level of a childcare center?

## Predictive Analysis of New York City Childcare centers

![picture](https://www.texaschildcaretraining.com/wp-content/uploads/2016/02/Blocks-how-safe-e1455198065617-420x315.jpg)

A 3-month-old baby died in SoHo Daycare in July 2015. SoHo Daycare is operated for 14 years without a license. Another incident was a 3-year-old girl who died in a daycare in Long Island on December 2018. Recently, in January 2019, a 4-month-old baby died in a daycare in Brooklyn. Al these incidents are the worst nightmares for all parents. One of the biggest concerns of working parents is to provide high-quality childcare for their children. A daycare can cost them as much as a college tuition. However, they would like to trust and be sure that childcare centers provide a safe and healty environment for their precious child.    

Health departments conduct inspections and surveillances across America to monitor safety level of childcare centers. However, the checks are insufficient in preventing the rising number of violations. This project addresses the need for improved surveillance and additional precautions. The analysis of New York City childcare inspection data tries to answer that can a parent predict the safety level of a childcare center.
 
Two data sets used for the analysis. First one is the DOHMH(Department of Health and Mental Hygiene) Child Care Inspection Data. The second one is social media data imported from Yelp. This data set used to analyze the parent reviews for each childcare centers. For more information about the data and the cleaning process, please see the links below:

  1. [Proposal](https://github.com/daphneworld/capstone1/blob/master/%20Proposal.pdf)
  
  2. [Data Wrangling Process](https://github.com/daphneworld/capstone1/blob/master/Data%20Wrangling%20Process%20of%20Capstone%20Project%201.pdf)
  
  3. [Data Wrangling Code](https://github.com/daphneworld/capstone1/blob/master/Data%20Wrangling%20of%20Capstone%20Project.ipynb)
  
Childcare centers are annually inspected by New York City childcare inspection office. The data is formed as summary of inspection visits for past three years. Each row represents an inspection visit to a specific facility. However majority of them inspected more than three based on an observed violation or complaints. The exploratory data analysis process contain the analysis of different features and their relations.  For more information about the exploratory data analysis process, please see the links below:

  1. [Data Story](https://github.com/daphneworld/capstone1/blob/master/CHILDCARE%20CENTERS%20SAFETY%20LEVEL%20PREDICTION.pdf)
 
  2. [Exploratory Data Analysis](https://github.com/daphneworld/capstone1/blob/master/Exploratory%20Data%20Analysis.pdf)
 
  3. [Exploratory Data Analysis Code](https://github.com/daphneworld/capstone1/blob/master/Exploratory%20Data%20Analysis%20New%20York%20City%20Childcare%20Centers.ipynb)
 
## Key Findings

 - The maximum number of inspection visit to a facility is 74. It means approximately 24 visit in a year and 2 visit in a month.
 
 - Only 3698 inspection visits turn out without any violation observation.
 
 - The number of inspections visit that violation observed is 38081.
 
 - The number of schools are correlated with the number of violations. Brooklyn is the region, which has the highest number of schools in the New York City area, and Staten Island has the least number of schools. The highest number of violation has been observed in the Brooklyn region and the number of observed violations in Staten Island is the smallest.
 
 - There isn’t any educated staff in camps.

 - The highest number of violations observed between 2-5 year-old age ranges.

 - There isn't a correlation between the number of violation and the ratings at Yelp. It means parents are not a good detector for violations.

 - The most occurred violations are respectively;
   - Staff failed to obtain proof of immunization; Except for exempt staff, required staff immunizations were not submitted to child care service; records not confidential. 
   
   - At time of inspection it was determined that child care service allows staff to perform their duties that are not healthy or are incapable of carrying out their duties. Staff medical clearances are not maintained by child care service.
   
   - At time of inspection floors/walls ceilings were observed not maintained; in disrepair or covered in a toxic finish.
   
   - At time of inspection it was determined that child care service failed to ensure staff received required training within time frames and/or failed to maintain training records.
   
   - All teachers have not received training in infectious disease control and reporting.
   
   - At time of inspection child care service facility observed not maintained or in disrepair. Dry sweeping observed in areas occupied by children.
   
   - Child care service failed to arrange/conduct criminal/SCR background clearance checks for required individuals; failed to re-clear required individuals with the SCR every two years.
   
   - All staff do not have required immunizations certified by a health care provider; record not available for inspection
   
   - Child care service staff identified/acting as group teachers do not meet the required qualifications of the position.
   
   - At time of inspection hand wash sinks are not supplied with an adequate amount of running water. At time of inspection water temperature exceeded 115 deg Fahrenheit. 

  - The number of violation based on regions are respectively;
  
   - In Brooklyn, 11662 violations observed in 1219 schools.
   
   - In Queens, 8493 violations observed in 681 schools.
   
   - In Manhattan, 8319 violations observed in 735 schools.
   
   - In Bronx, 7926 violations observed in 438 schools.
   
   - In Staten Island, 1676 violation observed in 139 schools.
   
  - The top three childcare centers with the highest number of violation are;
  
  Center Name | Number of Violation
  ------------|---------------------
  THE LEARNING TREE|74 violations
  TENDER TOTS/137 ST LLC|73 violations
  SEABURY DAY CARE CENTER|73 violations
  
  ## Machine Learning
  
  

