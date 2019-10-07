# Can a parent predict the safety level of a childcare center?

## Predictive Analysis of New York City Childcare centers

![picture](https://www.texaschildcaretraining.com/wp-content/uploads/2016/02/Blocks-how-safe-e1455198065617-420x315.jpg)

A 3-month-old baby died in SoHo Daycare in July 2015. SoHo Daycare is operated for 14 years without a license. Another incident was a 3-year-old girl who died in a daycare in Long Island on December 2018. Recently, in January 2019, a 4-month-old baby died in a daycare in Brooklyn. Al these incidents are the worst nightmares for all parents. One of the biggest concerns of working parents is to provide high-quality childcare for their children. A daycare can cost them as much as a college tuition. However, they would like to trust and be sure that childcare centers provide a safe and healthy environment for their precious child.    

Health departments conduct inspections and surveillances across America to monitor safety level of childcare centers. However, the checks are insufficient in preventing the rising number of violations. This project addresses the need for improved surveillance and additional precautions. The analysis of New York City childcare inspection data tries to answer that can a parent predict the safety level of a childcare center.
 
Two data sets used for the analysis. First one is the DOHMH(Department of Health and Mental Hygiene) Child Care Inspection Data. The second one is social media data imported from Yelp. This data set used to analyze the parent reviews for each childcare centers. For more information about the data and the cleaning process, please see the links below:

  1. [Proposal](https://github.com/daphneworld/capstone1/blob/master/%20Proposal.pdf)
  
  2. [Data Wrangling Process](https://github.com/daphneworld/capstone1/blob/master/Data%20Wrangling%20Process%20of%20Capstone%20Project%201.pdf)
  
  3. [Data Wrangling Code](https://github.com/daphneworld/capstone1/blob/master/Data%20Wrangling%20of%20Capstone%20Project.ipynb)
  
Childcare centers are annually inspected by New York City childcare inspection office. The data is formed as summary of inspection visits for past three years. Each row represents an inspection visit to a specific facility. However majority of them inspected more than three based on an observed violation or complaints. The exploratory data analysis process contain the analysis of different features and their relations.  For more information about the exploratory data analysis process, please see the links below:

  1. [Data Story](https://github.com/daphneworld/capstone1/blob/master/CHILDCARE%20CENTERS%20SAFETY%20LEVEL%20PREDICTION.pdf)
 
  2. [Exploratory Data Analysis](https://github.com/daphneworld/capstone1/blob/master/Exploratory%20Data%20Analysis.pdf)
 
  3. [Exploratory Data Analysis Code](https://github.com/daphneworld/capstone1/blob/master/Exploratory%20Data%20Analysis%20New%20York%20City%20Childcare%20Centers.ipynb)
 
## Machine Learning
  
  A new column is added to the data set, which shows the three safety levels of childcare centers. The thresholds specify the safety levels, as shown below:
  
```Python
Safety = [] 
for value in df.iloc[:,1]: 
    if value >=5 and value<=12 : 
        Safety.append("Warning") 
    elif value <= 4: 
        Safety.append("Safe") 
    else: 
        Safety.append("Not Safe") 
       
df["Safety"] = Safety    
```

New York City Health center provide childcare performance summary card for parents to see recent inspection results.

![cpsc](https://www.nysenate.gov/sites/default/files/childcare_performance_card_-_6.2.jpg)

However it is hard to interpret and understand violation rates without a comparison with other facilities. This model aim to give a basic prediction for safety level of a childcare center. If a facility have less than or equal to 4 inspection visit, it is in `Safe` category. If the inspection visit number is more than 4 and less than or equal to 12, it is in `Warning` category. More than 12 visit correspond to the `Not Safe`category.

Among the multiclass prediction models, extra trees classifier achieved the best results. The model evaluated with different metrics. The average acuracy score is 0.97 and hamming loss is 0.02. For more information about the exploratory data analysis process, please see the link below:

   - [Machine Learning Analysis](https://github.com/daphneworld/capstone1/blob/master/ML%20analysis.ipynb)
   - [Presentation slides](https://github.com/daphneworld/capstone1/blob/master/Childcare_center_Presentation.pdf)
   

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
  

   
 ## Conclusion
 
 There is not a correlation between Yelp ratings and safety levels of the childcare centers. There are 20 childcare centers with '1' rating.  Two of them are in 'Safe' category. There are also many '5' rating childcare centers with a high number of violations. One of the most common ways to find the right daycare is the recommendation of other parents. However, these results show that the parents are not accurate detectors for the safety level of a childcare center. A limitation of this approach is that it relies upon high participation of parents to rate the facilities. There are many daycares with only one or two ratings. Yelp can be a powerful screening tool if there is support from a user base within the community. It may improve the quality of the results.
 
This model focused on the number of health code rating. It could also use for a more specific group of health code violations such as public health hazard or critical violations. For this study, the prediction of violations practiced by childcare centers owners and employees does not forecast the behaviors of these facilities in the future.  The follow-up studies were ideal for defining the ensuing situations.

This study offers proof that inspection data is useful to predict potential child health risks. We are aware that it is not something that will be easily replicated by the general public.  However, public health departments can build upon our methods and offer information to the public about the risks that have been identified by inspectors. This method will assist in prioritizing which facilities may require more intensive inspections and follow up visits. It is important to note that the system of assigning health code violations by inspectors may not be enough. 

## Recommendations

All families have a right to receive high-quality care for their child.  It is health departments job to ensure that childcare centers have safe and healthy environments for children. Another dimension of their job is to share their findings with the authorities and the public. However, it is crucial to articulate this output understandably. Sharing the actual violation reason rather than violation scores may have practical impacts both for parents and childcare centers. 

There is a need for a system that parents can access easily, and quickly to communicate with authorities to get information and also share their reviews. This method may catch elements that inspectors have already seen, but it also identifies what the inspectors have not yet seen, and may be unable to detect. 

## Further improvements

Future studies, including the childcare center tuitions and the income level of regions, would contribute to the findings we report here. Also, sentiment analysis of Yelp reviews may be more beneficial than ratings for the benefit of public health.
 




