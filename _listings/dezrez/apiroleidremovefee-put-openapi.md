---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Remove a fee from a given PropertyMarketingRole.
  version: 1.0.0
  description: Remove a fee from a given propertymarketingrole..
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/agency/feestructure:
    get:
      summary: Gets the fee structure of the agency
      description: Gets the fee structure of the agency.
      operationId: Agency_GetFeeStructure
      x-api-path-slug: apiagencyfeestructure-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Fee
      - Structure
      - Of
      - Agency
  /api/admin/agency/{id}/setfeestructure:
    post:
      summary: Sets the fee structure on an agency
      description: Sets the fee structure on an agency.
      operationId: AgencyAdmin_SetFeeStructureByidByfeeStructure
      x-api-path-slug: apiadminagencyidsetfeestructure-post
      parameters:
      - in: body
        name: feeStructure
        description: The fee structure text
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The agency id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Sets
      - Fee
      - Structure
      - "On"
      - Agency
  /api/branch/updatefeelevel:
    put:
      summary: Update the Fee Level Setting for branch
      description: Update the fee level setting for branch.
      operationId: Branch_UpdateFeeLevelByfeeLevel
      x-api-path-slug: apibranchupdatefeelevel-put
      parameters:
      - in: query
        name: feeLevel
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Fee
      - Level
      - Settingbranch
  /api/fee/save:
    post:
      summary: Save a new fee into the system
      description: Save a new fee into the system.
      operationId: Fee_SaveFeeByfeeDataContract
      x-api-path-slug: apifeesave-post
      parameters:
      - in: body
        name: feeDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Save
      - New
      - Fee
      - Into
      - System
  /api/invoice/{id}/linkfees:
    post:
      summary: Add a fee to an existing invoice
      description: Add a fee to an existing invoice.
      operationId: Invoice_AddLinkedFeesByidByfees
      x-api-path-slug: apiinvoiceidlinkfees-post
      parameters:
      - in: body
        name: fees
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Fee
      - To
      - Existing
      - Invoice
  /api/invoice/{id}/removefee:
    put:
      summary: Remove fee from existing invoice
      description: Remove fee from existing invoice.
      operationId: Invoice_RemoveLinkedFeeByidByattachedFeeId
      x-api-path-slug: apiinvoiceidremovefee-put
      parameters:
      - in: query
        name: attachedFeeId
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Fee
      - From
      - Existing
      - Invoice
  /api/role/lettings/{id}/setfeestructure:
    post:
      summary: Sets the fee structure on a letting role
      description: Sets the fee structure on a letting role.
      operationId: LettingRole_SetFeeStructureByidByfeeStructure
      x-api-path-slug: apirolelettingsidsetfeestructure-post
      parameters:
      - in: body
        name: feeStructure
        description: The fee structure text
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The role id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Sets
      - Fee
      - Structure
      - "On"
      - Letting
      - Role
  /api/role/lettings/{id}/feestructure:
    get:
      summary: Gets the fee structure on a letting role
      description: Gets the fee structure on a letting role.
      operationId: LettingRole_GetFeeStructureByid
      x-api-path-slug: apirolelettingsidfeestructure-get
      parameters:
      - in: path
        name: id
        description: The role id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Fee
      - Structure
      - "On"
      - Letting
      - Role
  /api/role/{id}/removefee:
    put:
      summary: Remove a fee from a given PropertyMarketingRole.
      description: Remove a fee from a given propertymarketingrole..
      operationId: Role_RemoveFeeByidByfeeId
      x-api-path-slug: apiroleidremovefee-put
      parameters:
      - in: query
        name: feeId
        description: The Id of the fee to remove
      - in: path
        name: id
        description: the id of the role
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Fee
      - From
      - Given
      - PropertyMarketingRole
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