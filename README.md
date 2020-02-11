#Introduction

This SDK's goal is to provide guidance and the components needed for ISVs and Startups to transact their Software as a-Service (SaaS) applications via the Azure and AppSource marketplaces.  

The SDK provides the components required for the implementations of the billing (fulfillment v2 and metered) APIs, and additional components that showcase how to build a customer provisioning interface, logging, and administration of the customer's subscriptions. These are the core projects of the SDK:  

- **Transactable SaaS Client Library** that implements the fulfillment v2 and metered APIs (.NET Core 3.1 LTS) and the Web-hook that handles messages from the Marketplace's E-commerce engine.
- **Customer provisioning sample web application** that showcases how to provision a customer (ASP.NET Core 3.1) that uses the SDK to invoke fulfillment APIs in order to manage the subscriptions against the SaaS offer in Azure.
- **Publisher sample web application** that showcases how to generate metered based transactions, persistence of those transactions and transmission of these transactions to the metered billing API. 
- **Client Data Access library** that demonstrates how to persist the Plans, Subscriptions, and transactions with the fulfillment and Metered APIs.


### Documentation 

The Documentation (doc) repository contains: 

- **Installation instructions** to help you deploy and implement the SDK  components.  
- **Review of the SaaS Offer Patterns** The SDK 

### Sources 

The source (src) repository offers the following components: 

- **Transactable SaaS Client Library** that implements the fulfillment v2 and metered APIs (.NET Core 3.1 LTS) and the Web-hook that handles messages from the Marketplace's E-commerce engine.
- **Customer provisioning sample web application** that showcases how to provision a customer (ASP.NET Core 3.1) that uses the SDK to invoke fulfillment APIs in order to manage the subscriptions against the SaaS offer in Azure.
- **Publisher sample web application** that showcases how to generate metered based transactions, persistence of those transactions and transmission of these transactions to the metered billing API. 
- **Client Data Access library** to persist the Plans, Subscriptions, and transactions with the fulfillment and Metered APIs.
- **Unit Tests project** to help validate the SDK's codebase. 

The sample and the SDK in this repository cover the components that comprise the highlighted area in the below picture

Azure Marketplace Metering SDK enables SaaS applications publish usage data to Azure so that customers are charged  according to non-standard units. 

The metering SDK ( .NET class library ) and a sample web application to report usage events for subscriptions against those plans that support metering ( have the dimensions defined and enabled ) correlate to SaaS Metering and SaaS Service blocks in the below image, respectively.

![Usecase](./docs/images/use-case.png)

More details on the fulfilment APIs can be found [here](https://docs.microsoft.com/en-us/azure/marketplace/partner-center-portal/pc-saas-fulfillment-api-v2#update-a-subscription) 

More details on the metering APIs can be found [here](https://docs.microsoft.com/en-us/azure/marketplace/partner-center-portal/marketplace-metering-service-apis).

Steps to create a SaaS offer are available [here](https://docs.microsoft.com/en-us/azure/marketplace/partner-center-portal/create-new-saas-offer)

## Prerequisites

Ensure the following prerequisites are met before getting started:

- [Visual Studio 2019](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&rel=16#)
- [.NET Core 3.1 SDK or higher](https://download.visualstudio.microsoft.com/download/pr/639f7cfa-84f8-48e8-b6c9-82634314e28f/8eb04e1b5f34df0c840c1bffa363c101/dotnet-sdk-3.1.100-win-x64.exe)

Besides, it is assumed that you have access to the following resources:
- Azure subscription - to host the AMP SDK sample client application.
- Partner Center - to create and publish a marketplace offer.

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.