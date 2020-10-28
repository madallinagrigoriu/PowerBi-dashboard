# Power Bi dashboard 

<u>Context<u>
*Data is exported from Salesforce 
*The pbix.file has been created following the requirments below.


*1.	Data model based on the sources in data.xlsx
*2.	Calculations 
*a.	Amounts are in local currency, but the report needs to display them in EUR and USD; on the charts the total amount is displayed 
*b.	Subscription End Date - Subscription Start Date + Term (months)
c.	New ACV = 
0 if Close Date before 2018 
Upsell if Close Date in 2018 and 2019 and Acquisition Model is Renewal 
ACV if Close Date in 2018 and 2019 and Acquisition Model different from Renewal 
ACV if Close Date after 2020 
d.	Signature = License + 3 * New ACV
e.	Opportunity type = 
“Renewal” if Acquisition Model is Renewal
“Sales” otherwise
f.	Opportunity status = 
“Closed” if Stage is 6 or 7
“Open” otherwise
g.	Opportunity age = 
Number of days between Close Date and Creation Date if opportunity is closed
Number of days between Today and Creation Date if opportunity is open
h.	Catalog Category = 
"MFT" if Main Catalog Line is "AMPLIFY MFT" or "Cloud Services MFT"
"EFSS" if Main Catalog Line is "EFSS"
"APIM" if Main Catalog Line is "API Management" or "Cloud Services API"
"B2B" if Main Catalog Line is "Cloud Services EDI" or "EDI"
"None" if Main Catalog Line is null
"Other" otherwise
i.	Top Parent Account – the top parent name must be extracted from the initial string 
j.	The table must contain the following information: Account Name, Opportunity ID, Opportunity Name, Stage, Forecast Category, Main Catalog Line, Acquisition Model, Close Date, Total Amount, License, TCV, ACV, Service, Upsell, Downsell Maintenance, Signature, Opportunity Owner, Probability, Term, Subscription Start Date, Subscription End Date, Opportunity Source, BU Name, Partner Type, Partner Name, Created Date, Created By  
3.	Report filters: Top Parent Account, Account Name, CSM Segmentation 

<b>Note: In order to see the report you need to have installed Power Bi, you can do it from here https://powerbi.microsoft.com/en-us/downloads/<b>
