FALM-Housekeeping
=================
This package adds a tree node to the developer section with the following tools:
- Umbraco logs manager: with this tool you can view and delete Umbraco log events.
N.B.: in order to improve the performance of the log viewer, you can add SQL indexes to the coloumns DateStamp, UserId and LogHeader of umbracoLog table.
- Media folder cleanup: with this tool you can delete those file system folders under '/media' which have no entry in the DB (orphans)
N.B.: in the current release this feature works only with "UploadAllowDirectories" set to "true".
- Delete users: with this tool you can completely remove Umbraco users.
- Version manager: with this tool you can view and cleanup the version history that Umbraco mantains for each content node.

Versions History
=================
- v6.0.0.0 - Fix: update connectionstring
********************************************************************************************************************
ATTENTION
Please uninstall any previous version before install this version.
********************************************************************************************************************
- v4.11.0.2 - improved multilanguage support (Dictionary)
Now the dictionary items are taken according to the backoffice user's language.
- v4.11.0.1 - fixed issue
No treenode creation
- v4.11.0.0 - compatible with all DB
resolved compatibility with Umbraco v4.8+ 
resolved compatibility with Umbraco v6
multilanguage (with Dictionary)
- v4.5.0.1 - Fixed issue of no removing versions in v4.5 (*** db_owner required ***)
********************************************************************************************************************
ATTENTION
This Version requires that the SQL User is "db_owner" (or has the correct privileges to manage foreign keys) because the installation will modify the "FK_cmsPreviewXml_cmsContentVersion" constraint of the table "cmsPreviewXml" to enable the "ON CASCADE DELETE" rule.
Thank you to Alessandro Ghizzardi (http://umbracoitalia.org/) who helped me for fixing the problem
********************************************************************************************************************
- v4.5.0.0 - Version compatible with Umbraco from v4.5 to v4.7.2
- v1.1.0.0 - Version compatible with Umbraco v4.0 
- Logs manager: 
     - Added filtering capabilities on NodeId
     - Improved date filter: now you can select a range between two dates
- Media folder cleanup:
     - Various fixes in the search algorithm.
- Delete users:
     - Changed sort order and display of disabled users to match standard Umbraco behaviour
- Version manager:
     - Added filtering capabilities on NodeId
     - Improved date filter: now you can select a range between two dates
     - Added paging
     - Rewritten code with direct access to DB to make performance way faster
- v1.0.0.0 - Initial release
