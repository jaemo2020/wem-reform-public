# Changelog

# RTMS v2 (2022-09-01 MPT)

* Various changes and upgrades designed to reduce submission processing times.

* The export functionality in the Consolidated Submissions UI page has been implemented.

* The GET submissions API endpoint no longer allows queries with a few invalid combinations of parameter filters.

* The defect where the GET submissions API endpoint returns no data when called with the filter status = submitted, even if there are submissions in status submitted, has been fixed.

* The GET consolidated API endpoints now include an “as-at” time in the API response.

* The “grouped” view of the Consolidated Submissions has been developed in the Consolidated Submissions UI page and the GET consolidated API endpoints. The “ungrouped” view has been removed.

* Gate Closure Violations now appear in correct chronological order on the Gate Closure Violations UI page.
Fixed the defect where the Reference ID search filter in the Submissions History UI page is not cleared when the “clear all” button is clicked.

* When the GET submissions endpoint is called with a Reference Id filter, the endpoint previously returned only submissions with a Reference Id exactly matching the filter value. The endpoint will now return any submission with a Reference Id containing the filter value as a sub-string. 

* A defect in the validations relating to Acceptance Horizon (error codes C019 & DS016) has been fixed. The Acceptance Horizon is now calculated correctly.

* Added new validations (C048 and SC048) requiring Submission Reason to be provided when a submission is made within the Pre-Dispatch Schedule Horizon, in accordance with WEM Rule 7.4.26 as updated in Tranche 6 Exposure Draft 2.

* Validations requiring a Submission Reason (C030 and DS006) to be provided when the Submission Reason is not “INITIAL” have been removed.
The list of selectable Submission Codes in the submission schemata have been updated. 

* API path changed from …api/v1.0… to …api/v1…

* Minor updates to data types and formats in the API Swagger and response format.

* GET consolidated API function no longer return empty tranches and FSIP parameters objects when there is no relevant data.


# RTMS v1 (2022-02 MPT)

* Initial release of RTMS UI and API