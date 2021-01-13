# data_engineer

### Instruction

- Provide the answer to each exercise below in a separate file. When the exercises are done, there should be three (3) separate files.
- Push the exercise files to your public Github repository and send the link of the repo to kay@getconsciousgrowth.com


### Exercise 1

- Using both APIs under Sources, create an application that will update fx_price_index table in bidwh database (any SQL-supporting database) in consciousgrowth.1234.com server.
- This application will be scheduled to run every 5 minutes.
- The fx_price_index table should contain daily rates for BPI, USD, EUR, and GBP. Specifically, the table should contain only one rate per day per currency.
- The data in fx_price_index table should be structured so that it can be easily used for data analysis and SQL queries.
- Please state the language(s) and the type of SQL-supporting database you used for this application.

### Exercise 2

- Assume that [fixer.io](http://fixer.io) will now use OAuth 2. You have registered an API application with fixer.io. and have been issued client ID (A8f8B0300v456j7n) and client secret (N35620nff35Ndb05).
- Note the following endpoint:
    - POST https://data.fixer.io/oauth/token
    - Request body type: application/x-www-form-urlencoded
    - Request body
        - grant_type (string) - allowed: client_credentials, refresh_token
        - client_id (string)
        - client_secret (password)
        - refresh_token (password): optional
    - To authorize an API application and receive a token, use grant_type=client_credentials
    - Once a token is expired, it can be restored using grant_type=refresh_token and providing refresh_token
    - An example response:

        ```
        {
           "access_token": "yvMbx_TgwdYE0hOGRZcJiCjQuRGkVIBfjj8uo5uo7_QOXts1s58X30RrGBTyqV9h26SUHcZPNbZ",
           "token_type": "bearer",
           "refresh_token": "0b9KjiBVlZLz7a4H5mgNYwCQ_dWctTDsaIjedAhD1LpsOFJ7x9FHijALYSQ2UeRq5VEVYEaGf6",
           "expires_in": 3600,
           "scope": "all"
        }
        ```

- Develop the application from Exercise 1 using this new assumption on the fixer.io API.

### Exercise 3

- The application created in Exercise 1 or 2 needs to be scheduled and ran as a job. Describe the engine you will design - specify its tech stack. 
- Include as much detail/specification as needed.
