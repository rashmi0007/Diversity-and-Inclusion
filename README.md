# Pwc Switzerland - Power BI Virtual Case Experience - Diversity and Inclusion Analysis

## Problem Statement :
This project was based on Power BI, where an HR Diversity and Inclusion dataset was analyzed, a Power BI dashboard report was being designed, and KPIs were defined to measure the organization's progress.

The following actions could assist in establishing appropriate KPIs:-

•  '#' of men

•  '#' of women

•  '#' of leavers

•  % turnover

•  Average performance rating: Men

•  Average performance rating: Women


## Datasource :
Dataset used for this task was presented by [Pwc Switzerland](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html) and can be downloaded directly from [here](https://github.com/rashmi0007/Diversity-and-Inclusion/blob/master/03%20Diversity-Inclusion-Dataset.xlsx).

## 🛠 Tools & Technologies Used in project :
▪ Power BI Desktop

▪ DAX

▪ MS Excel

▪ PowerPoint (For Dashboard background design)

## Data Analysis :
Measures used in visualization are:

•  Total Employee =  DISTINCTCOUNTNOBLANK('Peoples Details'[Employee ID])

•  Avg Perf Rating Men =  CALCULATE(AVERAGE('Peoples Details'[FY20 Performance Rating]),FILTER('Peoples Details','Peoples Details'[Gender]="Male"))

•  Avg Perf Rating Women =  CALCULATE(AVERAGE('Peoples Details'[FY20 Performance Rating]),FILTER('Peoples Details','Peoples Details'[Gender]="Female"))

•  Employees Promoted in 2020 =  CALCULATE([Total Employee],FILTER('Peoples Details','Peoples Details'[Promotion in FY20?]="Y"))

•  Employees Promoted in 2021 =  CALCULATE([Total Employee],FILTER('Peoples Details','Peoples Details'[Promotion in FY21?]="Yes"))

•  Leaver =  CALCULATE([Total Employee],FILTER('Peoples Details','Peoples Details'[Leaver FY] IN {"FY20"}))

•  Men Count =  CALCULATE([Total Employee],'Peoples Details'[Gender]="Male")

•  Women Count =  CALCULATE([Total Employee],'Peoples Details'[Gender]="Female")

•  New Hire 2020 =  CALCULATE([Total Employee],FILTER('Peoples Details','Peoples Details'[New hire FY20?]="Y"))

•  % Turnover =  DIVIDE(CALCULATE(DISTINCTCOUNTNOBLANK('Peoples Details'[Employee ID]),FILTER('Peoples Details','Peoples Details'[FY20 leaver?]="Yes")),Divide(Calculate(distinctcount('Peoples Details'[Employee ID]),Filter('Peoples Details','Peoples Details'[In base group for turnover FY20]="Y"))+Calculate(DISTINCTCOUNT('Peoples Details'[Employee ID]),Filter('Peoples Details',NOT('Peoples Details'[Department @01.07.2020]=BLANK()))),2))

## [Dashboard](https://github.com/rashmi0007/Diversity-and-Inclusion/blob/master/Diversity_Inclusion_Dashboard.pbix):

![image](https://github.com/rashmi0007/Diversity-and-Inclusion/assets/87612040/defca7ec-7f11-4f73-96a9-f3d59f5695a2)

![image](https://github.com/rashmi0007/Diversity-and-Inclusion/assets/87612040/df730522-6bb1-4bb5-949f-c307a00356f9)


## Insights :

•  Out of the 500 employees, 295 (59%) are Male and 205 (41%) are Female.

•  In FY 20, more females were recruited than males, accounting for 51.52%.

•  Average Rating Female 2.42%.

•  Average Rating Male 2.41%.

•  Switzerland had the highest number of employees, followed by Europe and other regions.

•  Majority of employees, 44.6%, were between the ages of 20 and 29.

•  A total of 47 employees left the organization, comprising 26 males (55.32%) and 21 females (44.68%).
