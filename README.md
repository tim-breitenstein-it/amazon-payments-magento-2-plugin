# Amazon Pay for Magento 2
This extension provides an official integration of your Magento 2 store with **Amazon Pay** services. The extension is a checkout and payment solution that does not share any item level information (product information, prices, basket content, etc) with Amazon. The extension integrates Amazon Pay seamlessly into the Magento 2 shop backend (configuration, order management, billing, etc.).

## About Amazon Pay
Amazon Pay offers a familiar and convenient buying experience that can help your customers spend more time shopping and less time checking out. Amazon Pay is used by large and small companies. From years of shopping safely with Amazon, customers trust their personal information will remain secure and know many transactions are covered by the Amazon A-to-z Guarantee. Businesses have the reassurance of our advanced fraud protection and payment protection policy.

## What's new in Amazon Pay for Magento 2?
Starting from version 5.0.0, Amazon Pay is hosted on Magento Marketplace and features our next generation web checkout technology. This places the Amazon shipping and payment widgets outside the Magento checkout template system, improving usability and transaction error handling. Here are some of the improvements over the previous module:

* Hosted checkout experience (replacing inline widgets solution)
* Fewer checkout steps (merging consent and address/payment selection screen)
* Avoids problems on browsers that have active cookie blocking or tracking protection mechanisms
* Supports digital goods as well as physical goods
* Automatic, graceful handling of declined authorization, increasing checkout conversion rate
* Built-in Alexa Notifications feature support
* Ability to hide Amazon Pay as a checkout option for specific product categories

## Full feature list
* _Amazon Pay_ button in the shopping cart, mini-cart, on product pages and in the 1st step of checkout
* _Amazon Sign-in_ optional button on customer login and registration page
* _Amazon Pay_ in the list of available payment methods during the final step of checkout
* Configuration of _Amazon Pay_ extension from within Magento admin
* Support for payment authorizations, captures and refunds (also partial refunds)
* Support for synchronous and asynchronous authorization mode
* Supports _Amazon Pay_ Instant Payment Notifications
* Live & Sandbox modes available
* Options for simulating payment states in Sandbox mode
* Custom Front-Ends / Headless Commerce support
* Physical and Digital Goods support
* Ability to hide Amazon Pay as a checkout option for specific product categories
* Built-in Alexa Notifications feature support
* [EU/UK only] Multi-currency support
* [EU/UK only] Support for Strong Customer Authorization (PSD2 compliant)
* [EU/UK only] Billing Address available at checkout
* [US/JP only] Split Shipments (Multi-authorization) support

## Prerequisites
* Magento CE/EE/ECE 2.3.0 or higher (limited support for Magento 2.2.6 up to 2.2.11)
* valid SSL certificate
* A verified Amazon Pay merchant account - [sign up here](https://pay.amazon.com/signup)!

## Installation and Configuration
The extension is available via composer as *amzn/amazon-pay-magento-2-module* or in [Magento Marketplace](https://marketplace.magento.com/amzn-amazon-pay-magento-2-module.html). The User Guide can be found [here](https://amzn.github.io/amazon-payments-magento-2-plugin/). Any previous module versions should be removed. Please refer to the [Installation](https://amzn.github.io/amazon-payments-magento-2-plugin/installation.html) section of our guide to get more details concerning installation procedure.

## Branch information
The following table provides an overview on which Git branch is compatible to which Magento 2 version. The last column “Latest release” refers to the latest version of our extension that is compatible to the Magento 2 version in the first column. If you are on a Magento version below 2.2.6, please take a look at [Amazon Pay and Amazon Sign-in for Magento 2 (Legacy) documentation](https://amzn.github.io/amazon-payments-magento-2-plugin/legacy/installation.html#manual-composer-install-method).

Magento Version | Github Branch | Latest release
---|---|---
2.2.6 - 2.2.11 (EOL) | [V2Checkout-1.2.x](https://github.com/amzn/amazon-payments-magento-2-plugin/tree/V2Checkout-1.2.x)  | 1.11.0 (EOL)
2.3.0 - 2.4.x | [master](https://github.com/amzn/amazon-payments-magento-2-plugin/tree/master) | 5.0.0

## Release Notes
### 5.0.0
* General Availability release, replacing versions that were previously included in core Magento releases
* Fixed creating a credit memo against a split capture invoice
* Added input validation and test upon saving for credentials
* Changed calling `closeChargePermission` instead of `cancelCharge` when voiding an order
* Fixed loading correct config when switching store view before a cart is initiated
* Changed the button to create the session directly instead of through Magento
* Removed redirect to cart on login if the customer has products in cart
