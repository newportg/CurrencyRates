# CurrencyRates


| Process | Outcome|
|-|:-|
| **Build**     | [![Build Status](https://dev.azure.com/zoomalong/CurrencyRates/_apis/build/status/CurrencyRates-CI?branchName=master)](https://dev.azure.com/zoomalong/CurrencyRates/_build/latest?definitionId=5&branchName=master)
| **Dev**       | [![Dev status](https://vsrm.dev.azure.com/zoomalong/_apis/public/Release/badge/b444efd2-a37f-47de-92dd-27598a147b24/2/2)](https://vsrm.dev.azure.com/zoomalong/_apis/public/Release/badge/b444efd2-a37f-47de-92dd-27598a147b24/2/2)
| **Prd**       | [![Prd Status](https://vsrm.dev.azure.com/zoomalong/_apis/public/Release/badge/b444efd2-a37f-47de-92dd-27598a147b24/2/4)](https://vsrm.dev.azure.com/zoomalong/_apis/public/Release/badge/b444efd2-a37f-47de-92dd-27598a147b24/2/4)
| **Coverage**  | [![Coverage Status](https://coveralls.io/repos/github/newportg/CurrencyRates/badge.svg?branch=master)](https://coveralls.io/github/newportg/CurrencyRates?branch=master)
| **Project**   |[![Board Status](https://dev.azure.com/zoomalong/b444efd2-a37f-47de-92dd-27598a147b24/64f38721-702c-4b91-ab73-3a60ea6cd889/_apis/work/boardbadge/dea5cb40-fe34-46d6-bd26-5b69db76f356?columnOptions=1)](https://dev.azure.com/zoomalong/b444efd2-a37f-47de-92dd-27598a147b24/_boards/board/t/64f38721-702c-4b91-ab73-3a60ea6cd889/Microsoft.RequirementCategory)


Within many applications, there is a need to show or translate prices into different currencies. 
By having this facility available within the code, it allows you to 
* Store all prices in the same currency, 
* Display the price in whatever is the local currency of the viewer.

# Requirement

* Create a simple currency application to demostrate how this could work in practice.
* The application should have sufficent tests, so that it can be automatically tested during the build process.
* The application should be able to be torned down and redeployed from scripts.
* The deployed application should be configured to use a free currency service.
* The application should not have any currency pre configuration
    * When a user requests a rate that rate should be noted and then got daily
    * If a rate has not been requested for a period of time then the app should remove that rate from the update
* The application should maintain a list of available rates
  * For each rate note when it was last accessed.
* The application should be able to supply basic stats for health monitoring.
* There is no requirement for a GUI interface.
 
# Implementation

![Implementation](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.github.com/newportg/CurrencyRates/master/puml/Implementation.puml)