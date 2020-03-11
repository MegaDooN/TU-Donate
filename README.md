# TU-Donate

We should integrate with "Checkout" payment method in Liqpay: https://www.liqpay.ua/documentation/en/api/aquiring/checkout/doc
In this case we do not collect any data from portal visitor and just redirect them to LiqPay payment page. 

The details on how to generate request parameters are here: https://www.liqpay.ua/documentation/en/data_signature.

* "Client-Server" model should be chosen. 
* `action` parameter should have `paydonate` value 

If the payment data is static we can generate the `data` and `signature` parameters using this page: https://www.liqpay.ua/documentation/en/forming_test_data/

In other case (when f.e. we allow the portal visitor to choose the donation amount before redirecting them to LiqPay page) these parameters should be generated on the fly, f.e. by ajax request to server-side script. 

## Example
https://storage.googleapis.com/techukraine/tu_donate.html
