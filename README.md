# CurrencyRates

# Description

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