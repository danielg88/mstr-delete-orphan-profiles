MicroStrategy Orphan Profiles Removal
=====================================

This command manager script removes profiles objects and folders for users that don't exist anymore in the metadata. 

The list of users to be analyzed can be passed as:
*   File with list of users separated by ";" the file is called usuarios_profile_borrar.txt
*   Query to Platform Analytics or Enterprise Manager to get a list of users, by default the query gets users that have not connected to the platform for mor than a year.

Requires libraries for connecting to EM databases, for PA mysql-connector-java-8.0.16.jar can be used

**This script doesn't delete the profiles for all the users in the list, only those that have been deleted from metadata. If an object is a dependency for another shared object it will NOT be deleted.**

Run using 

    EXECUTE PROCEDURE Delete_Orphan_User_Profiles ('db_user','db_pwd','db_svr','db_port','db_sid')

