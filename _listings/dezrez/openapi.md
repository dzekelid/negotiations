---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 1
info:
  title: Dezrez.Rezi.Client.Api
  version: 1.0.0
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/branch/{id}/addnegotiator:
    post:
      summary: Adds a negoatiator to a branch
      description: Adds a negoatiator to a branch.
      operationId: Branch_AddNegotiatorByidBycommand
      x-api-path-slug: apibranchidaddnegotiator-post
      parameters:
      - in: body
        name: command
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
      - S
      - Negoatiator
      - To
      - Branch
  /api/chat/unreadsummary:
    get:
      summary: Get a count of unread chat messages for the negotiator plus a list
        of corresponding message id's which are unread.
      description: Get a count of unread chat messages for the negotiator plus a list
        of corresponding message id's which are unread..
      operationId: Chat_UnreadSummary
      x-api-path-slug: apichatunreadsummary-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Count
      - Of
      - Unread
      - Chat
      - Messagesthe
      - Negotiator
      - Plus
      - List
      - Of
      - Corresponding
      - Message
      - Ids
      - Which
      - Are
      - Unread
  /api/dashboard/{id}/addnegotiator:
    put:
      summary: Add negotiator to dashboard id
      description: Add negotiator to dashboard id.
      operationId: Dashboard_AddNegotiatorToDashboardByid
      x-api-path-slug: apidashboardidaddnegotiator-put
      parameters:
      - in: path
        name: id
        description: Dashboard Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Negotiator
      - To
      - Dashboard
      - Id
  /api/todo/assigntasktonegotiator:
    put:
      summary: Assign a task to a negotiator by its Id.
      description: Assign a task to a negotiator by its id..
      operationId: DefaultToDo_AssignTaskToNegotiatorBytaskIdBynegotiatorId
      x-api-path-slug: apitodoassigntasktonegotiator-put
      parameters:
      - in: query
        name: negotiatorId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: taskId
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Task
      - To
      - Negotiator
      - By
      - Its
      - Id
  /api/inboundlead/create:
    post:
      summary: Creates a lead in the system, optinally assigning the lead to a negotiator
      description: Creates a lead in the system, optinally assigning the lead to a
        negotiator.
      operationId: InboundLead_CreateLeadBydataContractByassignToNegId
      x-api-path-slug: apiinboundleadcreate-post
      parameters:
      - in: query
        name: assignToNegId
        description: Negotiator Id to assign lead too
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Lead
      - In
      - System
      - ""
      - Optinally
      - Assigning
      - Lead
      - To
      - Negotiator
  /api/invoice/processreceiptlistitems:
    put:
      summary: Process receipt list items for a specifici negotiator.
      description: Process receipt list items for a specifici negotiator..
      operationId: Invoice_ProcessReceiptListItemsBynegotiatorId
      x-api-path-slug: apiinvoiceprocessreceiptlistitems-put
      parameters:
      - in: query
        name: negotiatorId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Process
      - Receipt
      - List
      - Itemsa
      - Specifici
      - Negotiator
  /api/negotiator/my/keys:
    get:
      summary: Return all Negotiator keys for the side bar display.
      description: Return all negotiator keys for the side bar display..
      operationId: Negotiator_KeysBypageSizeBypageNumberBycheckedOutOnly
      x-api-path-slug: apinegotiatormykeys-get
      parameters:
      - in: query
        name: checkedOutOnly
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Return
      - ""
      - Negotiator
      - Keysthe
      - Side
      - Bar
      - Display
  /api/negotiator/me/setstatus:
    post:
      summary: Set the online/offline status of the logged in negotiator
      description: Set the online/offline status of the logged in negotiator.
      operationId: Negotiator_SetStatusBystatus
      x-api-path-slug: apinegotiatormesetstatus-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: status
      responses:
        200:
          description: OK
      tags:
      - Set
      - Online
      - Offline
      - Status
      - Of
      - Logged
      - In
      - Negotiator
  /api/negotiator/my/preferences:
    get:
      summary: Gets the preferences for current negotiator
      description: Gets the preferences for current negotiator.
      operationId: Negotiator_GetPreferences
      x-api-path-slug: apinegotiatormypreferences-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Preferencescurrent
      - Negotiator
    post:
      summary: Save or Update Negotiator Preferences
      description: Save or update negotiator preferences.
      operationId: Negotiator_SavePreferencesBypreferencesDataContract
      x-api-path-slug: apinegotiatormypreferences-post
      parameters:
      - in: body
        name: preferencesDataContract
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
      - ""
      - Negotiator
      - Preferences
  /api/negotiator/create:
    post:
      summary: Create New Negotiator
      description: Create new negotiator.
      operationId: Negotiator_CreateBydataContract
      x-api-path-slug: apinegotiatorcreate-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - New
      - Negotiator
  /api/negotiator/my/preferences/timeline:
    post:
      summary: Save or Update Negotiator Timeline Preferences
      description: Save or update negotiator timeline preferences.
      operationId: Negotiator_SaveTimelinePreferencesBypreferencesDataContract
      x-api-path-slug: apinegotiatormypreferencestimeline-post
      parameters:
      - in: body
        name: preferencesDataContract
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
      - ""
      - Negotiator
      - Timeline
      - Preferences
    get:
      summary: Get a Negotiators Timeline Preferences
      description: Get a negotiators timeline preferences.
      operationId: Negotiator_GetTimelinePreferences
      x-api-path-slug: apinegotiatormypreferencestimeline-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Negotiators
      - Timeline
      - Preferences
  /api/Negotiator/{id}:
    get:
      summary: Get a Negotiator by its id.
      description: Get a negotiator by its id..
      operationId: Negotiator_GetByid
      x-api-path-slug: apinegotiatorid-get
      parameters:
      - in: path
        name: id
        description: The id of the Negotiator to get
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Negotiator
      - By
      - Its
      - Id
  /api/todo/assignleadstoowningnegotiators:
    put:
      summary: Assign InboundLead Todos to the owning Negotiators of the property.
      description: Assign inboundlead todos to the owning negotiators of the property..
      operationId: DefaultToDo_AssignLeadsToOwningNegotiatorsBytoDoId
      x-api-path-slug: apitodoassignleadstoowningnegotiators-put
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: toDoId
      responses:
        200:
          description: OK
      tags:
      - Assign
      - InboundLead
      - Todos
      - To
      - Owning
      - Negotiators
      - Of
      - Property
  /api/negotiator/statuses:
    post:
      summary: Gets negotiators online / offline status.
      description: Gets negotiators online / offline status..
      operationId: Negotiator_GetNegotiatorStatusByNegotiatorIds
      x-api-path-slug: apinegotiatorstatuses-post
      parameters:
      - in: body
        name: NegotiatorIds
        description: The ids of the negotiators you want to get the status
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - Negotiators
      - Online
      - ""
      - ""
      - Offline
      - Status
  /api/negotiator/getbasic:
    get:
      summary: Get negotiators online / offline status.
      description: Get negotiators online / offline status..
      operationId: Negotiator_GetBasicByteamIdBypageSizeBypageNumber
      x-api-path-slug: apinegotiatorgetbasic-get
      parameters:
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: teamId
        description: (optional) teamId to get negotiators for
      responses:
        200:
          description: OK
      tags:
      - Negotiators
      - Online
      - ""
      - ""
      - Offline
      - Status
  /api/negotiator/my/properties/{roleType}:
    get:
      summary: Used for the Property Sales Dashboard to return a list of the negotiator's
        properties.
      description: Used for the property sales dashboard to return a list of the negotiator's
        properties..
      operationId: Negotiator_PropertiesByroleTypeBypageSizeBypageNumber
      x-api-path-slug: apinegotiatormypropertiesroletype-get
      parameters:
      - in: query
        name: pageNumber
        description: which page number of results to choose
      - in: query
        name: pageSize
        description: how many properties to return (default 10)
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleType
        description: the PropertyMarketingRole type
      responses:
        200:
          description: OK
      tags:
      - Usedthe
      - Property
      - Sales
      - Dashboard
      - To
      - Return
      - List
      - Of
      - Negotiators
      - Properties
  /api/negotiator/my/properties/favourite/add/{propertyId}:
    post:
      summary: Add property to Negotiators favourite list
      description: Add property to negotiators favourite list.
      operationId: Negotiator_AddFavouritePropertyBypropertyIdByroleId
      x-api-path-slug: apinegotiatormypropertiesfavouriteaddpropertyid-post
      parameters:
      - in: path
        name: propertyId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: roleId
      responses:
        200:
          description: OK
      tags:
      - Property
      - To
      - Negotiators
      - Favourite
      - List
  /api/negotiator/my/properties/favourite/remove/{propertyId}:
    delete:
      summary: Remove a property from a Negotiators favourite list.
      description: Remove a property from a negotiators favourite list..
      operationId: Negotiator_RemoveFavouritePropertyBypropertyIdByroleId
      x-api-path-slug: apinegotiatormypropertiesfavouriteremovepropertyid-delete
      parameters:
      - in: path
        name: propertyId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: roleId
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Property
      - From
      - Negotiators
      - Favourite
      - List
  /api/negotiator/my/groups/favourite:
    get:
      summary: Returns a list of the logged in negotiators favourite groups.
      description: Returns a list of the logged in negotiators favourite groups..
      operationId: Negotiator_FavouriteGroupsBypageSizeBypageNumber
      x-api-path-slug: apinegotiatormygroupsfavourite-get
      parameters:
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Returns
      - List
      - Of
      - Logged
      - In
      - Negotiators
      - Favourite
      - Groups
  /api/negotiator/my/groups/favourite/add/{groupId}:
    post:
      summary: Add a favourite group to the negotiators list of favourites.
      description: Add a favourite group to the negotiators list of favourites..
      operationId: Negotiator_AddFavouriteGroupBygroupId
      x-api-path-slug: apinegotiatormygroupsfavouriteaddgroupid-post
      parameters:
      - in: path
        name: groupId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Favourite
      - Group
      - To
      - Negotiators
      - List
      - Of
      - Favourites
  /api/negotiator/my/groups/favourite/remove/{groupId}:
    delete:
      summary: Remove a group from a Negotiators favourite list.
      description: Remove a group from a negotiators favourite list..
      operationId: Negotiator_RemoveFavouriteGroupBygroupId
      x-api-path-slug: apinegotiatormygroupsfavouriteremovegroupid-delete
      parameters:
      - in: path
        name: groupId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Group
      - From
      - Negotiators
      - Favourite
      - List
  /api/Negotiator:
    get:
      summary: Get negotiators online / offline status.
      description: Get negotiators online / offline status..
      operationId: Negotiator_GetByteamIdBypageSizeBypageNumber
      x-api-path-slug: apinegotiator-get
      parameters:
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: teamId
        description: (optional) teamId to get negotiators for
      responses:
        200:
          description: OK
      tags:
      - Negotiators
      - Online
      - ""
      - ""
      - Offline
      - Status
  /api/reporting/csv:
    post:
      summary: Request Csv for either set of negotiators or set of branches, with
        specified set of ReportFacets.
      description: Request csv for either set of negotiators or set of branches, with
        specified set of reportfacets..
      operationId: Reporting_RealtimeReportCsvByreportCsvRequest
      x-api-path-slug: apireportingcsv-post
      parameters:
      - in: body
        name: reportCsvRequest
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Request
      - Csveither
      - Set
      - Of
      - Negotiators
      - Set
      - Of
      - Branches
      - ""
      - Specified
      - Set
      - Of
      - ReportFacets
  /api/event/{id}/setnegotiators:
    post:
      summary: Changes the negotiators for an event
      description: Changes the negotiators for an event.
      operationId: Event_SetNegotiatorsByidBycommandDataContract
      x-api-path-slug: apieventidsetnegotiators-post
      parameters:
      - in: body
        name: commandDataContract
        description: Command Data Contract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Event Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Changes
      - Negotiatorsan
      - Event
  /api/negotiator/getarchived:
    get:
      summary: Get all archived Negotiators for the Agency's branch.
      description: Get all archived negotiators for the agency's branch..
      operationId: Negotiator_GetArchivedByteamIdBypageSizeBypageNumber
      x-api-path-slug: apinegotiatorgetarchived-get
      parameters:
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: teamId
        description: (optional) teamId to get negotiators for
      responses:
        200:
          description: OK
      tags:
      - Archived
      - Negotiatorsthe
      - Agencys
      - Branch
  /api/todo/claimtask:
    put:
      summary: Sets the claiming negotiator for the task
      description: Sets the claiming negotiator for the task.
      operationId: DefaultToDo_ClaimTaskByclaimTask
      x-api-path-slug: apitodoclaimtask-put
      parameters:
      - in: body
        name: claimTask
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Sets
      - Claiming
      - Negotiatorthe
      - Task
  /api/todo/reassigntodo:
    put:
      summary: Reassign a todo to different negotiator(s)
      description: Reassign a todo to different negotiator(s).
      operationId: DefaultToDo_ReassignTodoByreassignTodoCommandData
      x-api-path-slug: apitodoreassigntodo-put
      parameters:
      - in: body
        name: reassignTodoCommandData
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Reassign
      - Todo
      - To
      - Different
      - Negotiator(s)
  /api/todo/reassigntodotasks:
    put:
      summary: Reassign a list of tasks to different negotiator(s)
      description: Reassign a list of tasks to different negotiator(s).
      operationId: DefaultToDo_ReassignTodoTasksByreassignTasksCommandData
      x-api-path-slug: apitodoreassigntodotasks-put
      parameters:
      - in: body
        name: reassignTasksCommandData
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Reassign
      - List
      - Of
      - Tasks
      - To
      - Different
      - Negotiator(s)
---