---
title: Checkout Reference
layout: tutorial

summary: >
  A full API reference for Checkout.

navigation:
  header: na.tocs.na_nav_header
  footer: na.tocs.na_nav_footer
  toc: na.tocs.checkout_reference
  header_active: References

---

# Link parameters
Checkout is configured by the parameters passed in the URL of a GET request. The key/value pairs of the query string are secured by passing a hashed string created from the query string, in addition to the query string itself.

**URL:** https://web.na.bambora.com/scripts/payment/payment.asp

#### Authorization

| Name | Description |
| ---- | ----------- |
| merchant_id | Your 9-digit Bambora merchant ID |
| hashValue | The value for hashValue is generated by appending a hash key to the transaction request query string and using a hash algorithm (either MD5 or SHA-1) on the resulting string. |

#### Order info

| Name | Description |
| ---- | ----------- |
| trnAmount | The total amount for the transaction including tax and additional fees. Max 2 decimal places. Max 9 digits total. |
| trnOrderNumber | The invoice or order ID you want associated with the transaction. Up to 30 characters. |
| trnType | **P** - Purchase. **PA** - Pre-Authorization. |
| trnCardOwner| The name of the cardholder. 4-64 characters. |
| trnLanguage| **eng** - English, **fre** - French. |

#### Billing address

| Name | Description |
| ---- | ----------- |
| ordName | The billed contact's name. Up to 64 characters. |
| ordEmailAddress | The email address of the billed contact and destination for email receipts in a valid email format. Up to 64 characters. |
| ordAddress1 | The billing address for the card holder. With Address Verification, this will need to match the card issuer's records. Up to 32 characters. |
| ordAddress2 | The second line for the card holder's billing address. Up to 32 characters |
| ordCity | The city associated with the billing address. Up to 32 characters. |
| ordProvince | The province or state associated with the billing address. As a variable, the two-letter ISO code. |
| ordPostalCode | The postal or ZIP code associated with the billing address. Up to 16 characters. |
| ordCountry | The country associated with the billing address. As a variable, the two-letter ISO code. |

#### Shipping address

| Name | Description |
| ---- | ----------- |
| shipName | The name of the contact receiving the shipment. Up to 64 characters. |
| shipEmailAddress | The shipping contact's email address in a valid email format. Up to 64 characters. |
| shipAddress1 | The shipping contact's destination address. Up to 32 characters. |
| shipAddress2 | The second line of the shipping contact's destination address. Up to 32 characters |
| shipCity | The shipping contact's destination city. Up to 32 characters. |
| shipProvince | The shipping contact's province or state destination. As a variable, the two-letter ISO code. [Provinces](https://en.wikipedia.org/wiki/ISO_3166-2:CA) and [States](https://en.wikipedia.org/wiki/ISO_3166-2:US). |
| shipPostalCode | The shipping contact's postal or ZIP code. Up to 16 characters.
| shipCountry | The shipping contact's destination country. As a variable, the [two-letter ISO code](https://www.iso.org/obp/ui/#search/code/). |
| shipPhoneAddress | The shipping contact's phone number. Up to 32 characters. |

#### Redirects

| Name | Description |
| ---- | ----------- |
| approvedPage | The URL the cardholder will be sent to after their transaction is approved. |
| declinedPage | The URL the cardholder will be sent to after their transaction is declined. |

#### Hash expiry

| Name | Description |
| ---- | ----------- |
| hashExpiry | The time when the hash secured link will expire. The format is YYYYMMDDHHMM on PST. |

#### References info

| Name | Description |
| ---- | ----------- |
| ref1 | A custom identifier. 256 characters. |
| ref2 | A custom identifier. 256 characters. |
| ref3 | A custom identifier. 256 characters. |
| ref4 | A custom identifier. 256 characters. |
| ref5 | A custom identifier. 256 characters. |