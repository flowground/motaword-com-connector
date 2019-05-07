# ![LOGO](logo.png) MotaWord **flow**ground Connector

## Description

A generated **flow**ground connector for the MotaWord API (version 1.0).

Generated from: https://api.apis.guru/v2/specs/motaword.com/1.0/swagger.json<br/>
Generated at: 2019-05-07T17:43:05+03:00

## API Description

Use MotaWord API to post and track your translation projects.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Available endpoints

> The root endpoint will provide you a JSON Swagger definition.

*Tags:* `Static`

### Get a list of supported formats

> Get a list of supported formats for documents, style guides and extensions.

*Tags:* `Static`

### Download the global glossary.

> Download your corporate account's global glossary. This endpoint is available only for corporate account customers.

*Tags:* `Account` `Glossary`

### Create or update the global glossary.

> Update your corporate account's global glossary. This endpoint is available only for corporate account customers.

*Tags:* `Account` `Glossary`

### Get a list of supported languages

*Tags:* `Static`

### Get your account information and summary.

*Tags:* `Account`

### Get a list of your projects

*Tags:* `Project`

#### Input Parameters
* `page` - _optional_
* `per_page` - _optional_

### Get a new quote

> Create a new project

*Tags:* `Project`

### Delete a project

> Delete(cancel) a project.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Get single project

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Update project language pairs

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Trigger a call to your callback URL related to this project.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID
* `actionType` - _required_ - Callback type
    Possible values: translated, proofread, completed.

### Cancel your translation project

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Download the latest translation package.

> Download the latest translation package. You must have given a /package call beforehand and wait until the packaging status is 'completed'.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Download the latest translation package.

> Download only the translation package of this language. You must have given a /package call beforehand and wait until the packaging status is 'completed'.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID
* `language` - _required_ - Language code. You can download the translation of only a specific language.

### Launch your translation project

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Package the translation of all languages to be downloaded.

> Package the translation project, make it ready to be downloaded.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID
* `async` - _optional_ - If you want to package and download the translation synchronously, mark this parameter as '0'. It will package the translation and then return the packaged file in the response, identical to /download call after an asynchronous /package call.

### Track the status of translation packaging.

> This request will tell you the current progress of the translation packaging. You will use the 'key' provided by the /package call.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID
* `key` - _optional_ - This is the package tracking key provided in the response of a /package call.

### Package the translation of a specific target language to be downloaded.

> Package the translation project, make it ready to be downloaded.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID
* `language` - _required_ - Language code. You can package the translation of only a specific language.
* `async` - _optional_ - If you want to package and download the translation synchronously, mark this parameter as '0'. It will package the translation and then return the packaged file in the response, identical to /download call after an asynchronous /package call.

### Get project progress

> Get the progress of an already launched project.

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Submit reports for a project

*Tags:* `Project`

#### Input Parameters
* `id` - _required_ - Project ID

### Get a list of realtime activities.

> Get a list of realtime activities on the project, such as translation suggestion and translation approval.

*Tags:* `Activity`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `page` - _optional_
* `per_page` - _optional_

### Get a single realtime activity.

*Tags:* `Activity`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `activityId` - _required_ - Activity ID

### Submit a comment to an activity.

*Tags:* `Activity`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `activityId` - _required_ - Activity ID

### Get a list of comments belonging to this activity.

*Tags:* `Activity`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `activityId` - _required_ - Activity ID

### Get a list of activity comments throughout the whole project.

*Tags:* `Activity`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `page` - _optional_
* `per_page` - _optional_

### Get a list of documents

*Tags:* `Document`

#### Input Parameters
* `projectId` - _required_ - Project ID

### Upload a new document

*Tags:* `Document`

#### Input Parameters
* `projectId` - _required_ - Project ID

### Delete the document

*Tags:* `Document`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `documentId` - _required_ - Document ID

### Get single document

*Tags:* `Document`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `documentId` - _required_ - Document ID

### Update the document.

> Update the document. File name and contents will replaced with the new one.

*Tags:* `Document`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `documentId` - _required_ - Document ID

### Download a document

*Tags:* `Document`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `documentId` - _required_ - Document ID

### Get a list of glossaries

*Tags:* `Glossary`

#### Input Parameters
* `projectId` - _required_ - Project ID

### Upload a new glossary

*Tags:* `Glossary`

#### Input Parameters
* `projectId` - _required_ - Project ID

### Delete the glossary

*Tags:* `Glossary`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `glossaryId` - _required_ - Glossary ID

### Get single glossary

*Tags:* `Glossary`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `glossaryId` - _required_ - Glossary ID

### Update the glossary.

> Update the glossary. File name and contents will replaced with the new one.

*Tags:* `Glossary`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `glossaryId` - _required_ - Glossary ID

### Download a glossary

*Tags:* `Glossary`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `glossaryId` - _required_ - Glossary ID

### Get a list of style guides

*Tags:* `Style Guide`

#### Input Parameters
* `projectId` - _required_ - Project ID

### Upload a new style guide

*Tags:* `Style Guide`

#### Input Parameters
* `projectId` - _required_ - Project ID

### Delete the style guide

*Tags:* `Style Guide`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `styleGuideId` - _required_ - Style Guide ID

### Get single style guide

*Tags:* `Style Guide`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `styleGuideId` - _required_ - Style Guide ID

### Update the style guide.

> Update the style guide. File name and contents will replaced with the new one.

*Tags:* `Style Guide`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `styleGuideId` - _required_ - Style guide ID

### Download a style guide

*Tags:* `Style Guide`

#### Input Parameters
* `projectId` - _required_ - Project ID
* `styleGuideId` - _required_ - Style Guide ID

### Download the global style guide.

> Download your corporate account's global style guide. This endpoint is available only for corporate account customers.

*Tags:* `Account` `Style Guide`

### Create or update the global style guide.

> Update your corporate account's global style guide. This endpoint is available only for corporate account customers.

*Tags:* `Account` `Style Guide`

### Retrieve an access token to interact with the API.

> MotaWord API is using OAuth2 procedures when authenticating or authorizing your API call. Currently, we only allow Client Credential type flow.

*Tags:* `Auth`

#### Input Parameters
* `Authorization` - _required_ - HTTP Basic Authorization header.

## License

**flow**ground :- Telekom iPaaS / motaword-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
