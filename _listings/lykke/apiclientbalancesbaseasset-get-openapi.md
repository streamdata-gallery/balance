---
swagger: "2.0"
x-collection-name: Lykke
x-complete: 0
info:
  title: Lykke Get API Client Balances Baseasset
  version: 1.0.0
  description: Get api client balances baseasset.
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/BitcoinCash/multisig/balance:
    get:
      summary: Get API Bitcoincash Multisig Balance
      description: Get api bitcoincash multisig balance.
      operationId: ApiBitcoinCashMultisigBalanceGet
      x-api-path-slug: apibitcoincashmultisigbalance-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      responses:
        200:
          description: OK
      tags:
      - Bitcoincash
      - Multisig
      - Balance
  /api/BitcoinCash/private/balance:
    get:
      summary: Get API Bitcoincash Private Balance
      description: Get api bitcoincash private balance.
      operationId: ApiBitcoinCashPrivateBalanceGet
      x-api-path-slug: apibitcoincashprivatebalance-get
      parameters:
      - in: query
        name: address
      - in: header
        name: Authorization
        description: access token
      responses:
        200:
          description: OK
      tags:
      - Bitcoincash
      - Private
      - Balance
  /api/MarginTrading/account/balance:
    post:
      summary: Add API Margintrading Account Balance
      description: Add api margintrading account balance.
      operationId: ApiMarginTradingAccountBalancePost
      x-api-path-slug: apimargintradingaccountbalance-post
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: body
        name: model
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Margintrading
      - Account
      - Balance
  /api/Client/balances/{baseAsset}:
    get:
      summary: Get API Client Balances Baseasset
      description: Get api client balances baseasset.
      operationId: ApiClientBalancesByBaseAssetGet
      x-api-path-slug: apiclientbalancesbaseasset-get
      parameters:
      - in: header
        name: Authorization
        description: access token
      - in: path
        name: baseAsset
      responses:
        200:
          description: OK
      tags:
      - Client
      - Balances
      - Baseasset
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---