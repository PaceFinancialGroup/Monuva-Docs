Static Data Endpoints
=====================

Our static data endpoints provide access to frequently used refererence data. Please note that these endpoints do **not** require the client to be authenticated.

.. attention:: Although it is possible to cache this data for long periods we would recommend refreshing it at regular intervals 


Bank Accounts
-------------

GET api/v1/bankaccounts
^^^^^^^^^^^^^^^^^^^^^^^
Retrieves a list of Monuva bank accounts to which bank transfers and invoice payments can be made.


Request Parameters
''''''''''''''''''
*None*


Response
''''''''
=============  ======   =====
Property       Type     Notes
=============  ======   =====
BankName       string
AccountName    string 
AccountNumber  string
SortCode       string
IBAN           string
BIC            string
CCY            string
CountryCode    string
=============  ======   =====

.. code-block:: json

    [
        {
            "BankName": "Lloyds Bank Plc",
            "AccountName": "PACE EUR",
            "AccountNumber": "86383401",
            "SortCode": "30-93-74",
            "IBAN": "GB75LOYD30937486383401",
            "BIC": "LOYDGB21022",
            "CCY": "EUR",
            "CountryCode": "GBR"
        },
        {
            "BankName": "Lloyds Bank Plc",
            "AccountName": "PACE GBP",
            "AccountNumber": "01142805",
            "SortCode": "30-93-74",
            "IBAN": "GB59LOYD30937401142805",
            "BIC": "LOYDGB21022",
            "CCY": "GBP",
            "CountryCode": "GBR"
        },
        {
            "BankName": "Lloyds Bank Plc",
            "AccountName": "PACE USD",
            "AccountNumber": "11649396",
            "SortCode": "30-93-74",
            "IBAN": "GB57LOYD30937411649396",
            "BIC": "LOYDGB21022",
            "CCY": "USD",
            "CountryCode": "GBR"
        }
    ]


Countries
---------

GET api/v1/countries
^^^^^^^^^^^^^^^^^^^^
Retrieves a list of supported countries.


Request Parameters
''''''''''''''''''
*None*


Response
''''''''
=============  ======   =====
Property       Type     Notes
=============  ======   =====
Name           string
Iso3           string   The 3 letter country ISO code
Iso2           string   The 2 letter country ISO code
Rank           int      Used to order the countries for display
=============  ======   =====

.. code-block:: json

    [
        {
            "Name": "United Kingdom",
            "Iso3": "GBR",
            "Iso2": "GB",
            "Rank": 1
        },
        {
            "Name": "United States of America",
            "Iso3": "USA",
            "Iso2": "US",
            "Rank": 2
        },
        {
            "Name": "Canada",
            "Iso3": "CAN",
            "Iso2": "CA",
            "Rank": null
        },
        {
            "Name": "Spain",
            "Iso3": "ESP",
            "Iso2": "ES",
            "Rank": null
        }
    ]


Currencies
----------

GET api/v1/currencies
^^^^^^^^^^^^^^^^^^^^^
Retrieves a list of supported currencies.


Request Parameters
''''''''''''''''''
*None*


Response
''''''''
=============  ======   =====
Property       Type     Notes
=============  ======   =====
Name           string
Symbol         string   The currency symbol used for display 
Iso3           string   The 3 letter country ISO code
Rank           int      Used to order the currencies for display
=============  ======   =====

.. code-block:: json

    [
        {
            "Name": "British Pound",
            "Symbol": "£",
            "Iso3": "GBP",
            "Rank": 1
        },
        {
            "Name": "Euro",
            "Symbol": "€",
            "Iso3": "EUR",
            "Rank": 2
        },
        {
            "Name": "US Dollar",
            "Symbol": "$",
            "Iso3": "USD",
            "Rank": 3
        },
        {
            "Name": "Canadian Dollar",
            "Symbol": "$",
            "Iso3": "CAD",
            "Rank": 4
        }
    ]

