List all App Service web apps outbound IP addresses used in a subscription (Old)
================================================================================

            

 

What is proposed

You'll find in this function an easy way to extract the outbound IP addresses information used by all your App Services in a subscription within an authenticated PowerShell Azure session.


 


**There is a new, way faster version that use the Azure Resource Graph that can be found here: **[List App Service web apps outbound IP addresses (New)](https://gallery.technet.microsoft.com/scriptcenter/List-App-Service-web-apps-b4a0bf79)


 

History

[2019-03-12] Updated script to fix a bug when a single address returned a Hashtable instead of an array. Thanks _JamesG_


[2019-01-08] Added support for -IncludePossibleOutputIpAddresses switch


 

Overview
  You will end up with an output in the like of:



PowerShell
Edit|Remove
powershell
Switching to subscription mysub1
Switching to subscription mysub2

Count   IpAddress       Type        Sites
-----   ----            -----       ----
    2   13.85.17.60     Outbound  {sub1-bi-dev-as-webapp, sub2-bi-prod-as-webapp}
    1   13.85.17.60     Possible  {sub3-bi-dev-as-webapp}
    2   13.85.20.144    Outbound  {sub1-bi-prod-as-webapp, sub1-bi-dev-as-webapp}
    1   13.85.20.144    Possible  {sub3-bi-dev-as-webapp}
    2   13.85.22.206    Outbound  {sub2-bi-prod-as-webapp, sub1-bi-dev-as-webapp}
    2   13.85.23.148    Outbound  {sub1-bi-dev-as-webapp, sub2-bi-prod-as-webapp}
    2   13.85.23.243    Outbound  {sub1-bi-dev-as-webapp, sub2-bi-prod-as-webapp}
    1   23.96.184.12    Outbound  {sub1-dev-functions-mmckydd}
    1   23.96.184.209   Outbound  {sub1-dev-functions-mmckydd}
    1   23.96.186.252   Outbound  {sub1-dev-functions-mmckydd}
    1   23.96.187.50    Outbound  {sub1-dev-functions-mmckydd}
    5   23.96.244.71    Outbound  {sub1-stg-webapp-web-n7wfdda, sub1-stg-functions-n7wfdda, sub1-stg-webapp-admin-n7wfdda, sub1-dev-ops-functions-stl4tn5...}

Switching to subscription mysub1 
Switching to subscription mysub2 
 
Count   IpAddress       Type        Sites 
-----   ----            -----       ---- 
    2   13.85.17.60     Outbound  {sub1-bi-dev-as-webapp, sub2-bi-prod-as-webapp} 
    1   13.85.17.60     Possible  {sub3-bi-dev-as-webapp} 
    2   13.85.20.144    Outbound  {sub1-bi-prod-as-webapp, sub1-bi-dev-as-webapp} 
    1   13.85.20.144    Possible  {sub3-bi-dev-as-webapp} 
    2   13.85.22.206    Outbound  {sub2-bi-prod-as-webapp, sub1-bi-dev-as-webapp} 
    2   13.85.23.148    Outbound  {sub1-bi-dev-as-webapp, sub2-bi-prod-as-webapp} 
    2   13.85.23.243    Outbound  {sub1-bi-dev-as-webapp, sub2-bi-prod-as-webapp} 
    1   23.96.184.12    Outbound  {sub1-dev-functions-mmckydd} 
    1   23.96.184.209   Outbound  {sub1-dev-functions-mmckydd} 
    1   23.96.186.252   Outbound  {sub1-dev-functions-mmckydd} 
    1   23.96.187.50    Outbound  {sub1-dev-functions-mmckydd} 
    5   23.96.244.71    Outbound  {sub1-stg-webapp-web-n7wfdda, sub1-stg-functions-n7wfdda, sub1-stg-webapp-admin-n7wfdda, sub1-dev-ops-functions-stl4tn5...}




 

Requirements

Tested with AzureRM.Profile Version 3.2.x & AzureRM.Websites 3.2.x


[2019-01-08] Tested with AzureRM.Profile Version 5.8.x & AzureRM.Websites 5.2.x


 


More information here:


https://www.codeisahighway.com/list-all-app-service-web-apps-outbound-ip-addresses-used-in-a-subscription/


        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
