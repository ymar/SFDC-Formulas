# SFDC-Formulas


A checkbox returns "true" or "checked" if the user viewing the record, report, or list view is the same user who created it, even if they don't "own" the record. This is useful for dynamic reports and list views.

$User.Id = CreatedById


Use a standard or custom Lookup User field, such as CreatedBy, LastModifiedBy, or reference other fields on the User Object such as:
$User.ProfileId  
$User.ProfileId 
$User.Department


You can't Bucket a Date Field in reports, so you can create a custom field to bucket quarters such as:

CloseDate (Quarter)
Datatype = Formula
Result = Text
'Q'+ TEXT(CEILING(MONTH( CloseDate ) / 3 ))


Power of 1
Custom Field
Datatype = Formula
Result = Number(0, decimals)
Formula = 1
That's it, just a number 1


