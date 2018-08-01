# Changelog

## Release 0.9.4

_Planned for August 13, 2018_

## Release 0.9.3

[Released on July 16, 2018](https://github.com/adobe/xdm/releases/tag/v0.9.3)

Fixed Issues

* #364 Video Analytics additions for ExperienceEvent
  * PR #417 Added Timed Media schemas to `Experience Event` based schemas PR
* #409 Fix campaign extension bugs
  * PR #410 Issue409-Fix campaign extension bugs
* #413 WebPageDetails.server shouldn't be constrained to a hostname
  * PR #414 Removed hostname format constraint from context/webpagedetails.xdm:server
* #419 Change Identity schema identifier to unstructured string from URI
  * PR #420 Change `Identity` Schema `@id` property renamed to `xdm:id`
* #425 Added datasourceID to the ExperienceCloud Extension for Experience Event.
  * PR #426 add dataset id as part of event

Merged Pull Requests

* #391 📝 Clarify CLA section of contribution guidelines.
* #416 Remove definition of xmp:numberOfPixels
* #423 Add post office box to align with Microsoft CDM
* #431 Create RELEASING.md file
* #436 Update Changelog preparing for V0.9.3 release
* #437 Fixing RELEASING.md

## Release 0.9.2

[Released on June 15, 2018](https://github.com/adobe/xdm/releases/tag/v0.9.2)

* `xdm:dataSource` in `ExperienceEvent` is no longer required #363
* Changed and added new concepts `Organizational Unit` and `Geographical Unit`. Existing links with the `Profile` schema updated. In `Profile`, `xdm:orgUnitID` is now `xdm:orgUnit`, and a simple reference to the `Organizational Unit` schema. #323
* Added Phone Number and Email Address to EndUserIDs. #381
* Changed Adobe Analytics Extension - Alter analytics custom lists to allow keys #376
* Added `"meta:extends": true` to the schemas that can be extended in `context` #332
* Changed extension `extensions/adobe/experience/implementations.schema.json` properties to include the name `implementation` #403
* Added Reporting Events to Experience Event in the Campaign Extension #307
* Improved the representation of Extensibility to `context\*` schemas #332
* Changed a circular reference introduces in the Campaign Extension to Experience Event #377 / #378
* Added Segment Membership and related schemas for `context\profile.schema.json` #380
* Added searchEngineID field to search schema to Experience Event #394
* Added the created/modified dates from auditable for `context\profile.schema.json`, address and person schemas #393
* Adding relationship descriptor #388

## Release 0.9.1

[Released on May 23, 2018](https://github.com/adobe/xdm/releases/tag/v0.9.1)

* Introduced Point of Interest details and metrics. #285
* Renamed all `Metric` schemas to `Metric Definition` #254
* Moved web metrics used in ExperienceEvent `metrics` to the webinteraction and webpageview contexts #316
* Renamed web metrics to `xdm:*` compressed type property names #316
* Moved `commerce` metrics used in ExperienceEvent `metrics` to the `commerce` context #317
* Renamed `commerce` metrics to `xdm:*` compressed type property names #317
* `abandons` metric field name change to `cartAbandons` . #317
* The `commerce` schema is now extensible to allow for additional dimensions and metrics. #317
* Removed the required constraint from `schemas/external/schema/geo*.schema.json` #315
* Moved `direct-marketing` metrics used in ExperienceEvent `metrics` to a new `xdm:directMarketing` contexts #331
* Introduced advertising context to ExperienceEvent #280
* Introduced advertising and viewability metrics under the advertising context #280
* Moved impressions and clicks metrics under advertising context #280
* Added `xdm:primary` flag to `schemas/context/identity.schema.json` #335
* Corrected naming of EndUserIDs by making them consistent (aaid and acid) `schemas/external/schema/geo*.schema.json` #333
* Renamed `webPageView` to `webPageDetails` e.g `context/webpagedetail.schema.json` #336
* Added application and mobile context via `context\application.schema.json` #318
* Fixed issue where `context\experienceevent` `xdm:application` referred to the 'application.schema.json' in `channels` #318
* `xdm:application` in `context\experienceevent` `@id` renamed to `xdm:id` #318
* Changed `xdm:channel` in `ExperienceEvent` to be a reference to `Channel` #289
* Changed `xdm:pageDepth` data type from number to integer in `context\search.schema.json` #346

## Release 0.9.0

[Released on April 13, 2018](https://github.com/adobe/xdm/releases/tag/v0.9)

* Release 0.9 is preview release which updates the `ExperienceEvent` schema to 'stabilizing' status, along with many of the schemas it depends on. This release is intended to get early feedback from implementers and the community before a 1.0 release.
