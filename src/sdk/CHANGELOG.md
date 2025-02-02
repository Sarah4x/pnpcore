# PnP Core SDK Changelog

*Please do not commit changes to this file, it is maintained by the repo owner.*

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/).

## [unreleased]

### Added

### Changed

- Improved handling of special characters ('#& ) for files and folders [jansenbe - Bert Jansen]
- Fix for single quote in client side page name #348 [Sarah4x - Sarah Wilson]
- Improved CSOM support for content type creation and taxonomy field creation #349 [mgwojciech - Marcin Wojciechowski]
- Uplifted samples to GA v1.0.0 #350 [pkbullock - Paul Bullock]
- Fix for older SharePoint UI created image web parts where links is set to null #347 [Sarah4x - Sarah Wilson]

## [1.0.0]

### Added

- Added Rights support for custom actions [erwinvanhunen - Erwin van Hunen]
- Added support to recycle a list item to the recycle bin [erwinvanhunen - Erwin van Hunen]
- Added support to add a folder to a SharePoint list [erwinvanhunen - Erwin van Hunen]
- Added support to modify roledefinitions for a SharePoint list [erwinvanhunen - Erwin van Hunen]
- Added support to add and remove roledefinitions to a SharePoint group [erwinvanhunen - Erwin van Hunen]
- Added support for breaking role inheritance and resetting role inheritance for a list [erwinvanhunen - Erwin van Hunen]
- Added support for creating and deleting roledefinitions [erwinvanhunen - Erwin van Hunen]
- Added support for deleting SharePoint groups [erwinvanhunen - Erwin van Hunen]
- Added support for adding and removing users from ISharePointGroup [erwinvanhunen - Erwin van Hunen]
- Added support for setting the Compliance Tag on a list [erwinvanhunen - Erwin van Hunen]
- Added support for setting the Compliance Tag on a list item [erwinvanhunen - Erwin van Hunen]
- Added support for retrieving available site Compliance Tags / retention labels [erwinvanhunen - Erwin van Hunen]
- Added support for retrieving the Compliance Tag set for a list [erwinvanhunen - Erwin van Hunen]
- Implemented PnP.Core.Auth [PaoloPia - Paolo Pialorsi]
- Issue templates (#34) [ypcode - Yannick Plennevaux] / [jansenbe - Bert Jansen]
- Enable PnPContext creation from a Microsoft 365 Group id (#39) [jansenbe - Bert Jansen]
- Added the Group model, represents a Microsoft 365 group (#48) [jansenbe - Bert Jansen]
- Added custom exception handling for authentication errors (#45) [jansenbe - Bert Jansen]
- Support to use an externally obtained access token (#44) [jansenbe - Bert Jansen]
- Add step-by-step guide on how to extend the model (#46) [ypcode - Yannick Plennevaux] / [jansenbe - Bert Jansen]
- First iteration of content type support (within the limitations of SharePoint REST) (#47) [ypcode - Yannick Plennevaux]
- Update test code so that custom settings file do not have to be marked as "copy always" #53 [jansenbe - Bert Jansen]
- Use RegisterWaitForSingleObject for the token invalidation thread in combination with IDisposable to prevent threads to leak #56 [jansenbe - Bert Jansen]
- Mark read-only properties as Get only in the interfaces to ensure SDK consumers are not trying to update them #59 [jansenbe - Bert Jansen]
- Request retry mechanism, will handle core http and Graph batch requests #21 [jansenbe - Bert Jansen]
- Tweaking and updating of the writing tests documentation #65 [pkbullock - Paul Bullock]
- Paging support for Graph/Rest #3 [jansenbe - Bert Jansen]
- Added Clone method on PnPContext #49 [jansenbe - Bert Jansen]
- Extend the domain model for Web/Site Feature support #62 [pkbullock - Paul Bullock]
- Extend SP Field model (add operation for each field type) for both Web and List fields #71 [ypcode - Yannick Plennevaux]
- Added support for AddFieldAsXml #71 [ypcode - Yannick Plennevaux]
- Add basic support for FieldLinks #75 [ypcode - Yannick Plennevaux]
- Add support for external access token provider (IOAuthAccessTokenProvider) #76 [ypcode - Yannick Plennevaux]
- Added recursive support for .Include() to define which fields of a collection are loaded [jansenbe - Bert Jansen]
- Add support for getting list items via a CAML query #80 [jansenbe - Bert Jansen]
- Support RenderListDataAsStream method on lists - basic implementation #81 [jansenbe - Bert Jansen]
- Add support for calling client.svc (CSOM) endpoint #86 [jansenbe - Bert Jansen]
- Added SystemUpdate() and UpdateOverwriteVersion() methods on the ListItem model (uses CSOM) [jansenbe - Bert Jansen]
- Async LINQ support [PaoloPia - Paolo Pialorsi]
- Added sync equivalents for all async methods [jansenbe - Bert Jansen]
- Support for list and web folders #78 [ypcode - Yannick Plennevaux]
- Test cases for the Teams model #95 [JarbasHorst - Jarbas Horst]
- Taxonomy support using the Graph API #104 [jansenbe - Bert Jansen]
- Support working with files #78 [ypcode - Yannick Plennevaux]
- Use CSOM to create content types with a specified id #108 [ypcode - Yannick Plennevaux]
- Support for making interactive SharePoint REST requests + upload of files #112 [jansenbe - Bert Jansen]
- Additional test cases - working getting >80% test coverage [pkbullock - Paul Bullock]
- Expansion of the Web object with web properties, root folder, site user info list and more [ypcode - Yannick Plennevaux]
- Rewrite of the auth model, fixes #43 [PaoloPia - Paolo Pialorsi]
- LoadProperties now also supports Graph #145 [jansenbe - Bert Jansen]
- Authentication enhancements #302 [sebastianmattar - Sebastian Mattar]
- CSOM Light client - first step implementation for PropertyBag updates #334 [mgwojciech - Marcin Wojciechowski]
- Support for ListItem permission management #343 [jimmywim - Jim Love]
- CSOM Light client - List item update logic #345 [mgwojciech - Marcin Wojciechowski]

### Changed

- Documentation updates [JarbasHorst - Jarbas Horst]
- EnsurePropertiesAsync takes in account .Include (recursive) usage [jansenbe - Bert Jansen]
- Documentation updates [Ashikpaul - Ashik Paul]
- Moved to complete async internal implementation [jansenbe - Bert Jansen]
- Code cleanup (Teams implementation / ODataQuery) [JarbasHorst - Jarbas Horst]
- When a non loaded model properties is assigned it now is considered as a change and send back to the server on update #106 [jansenbe - Bert Jansen]
- Throw client exception when an API call still contains unresolved tokens before being executed #107 [jansenbe - Bert Jansen]