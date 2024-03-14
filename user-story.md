Full Stack user story and elaboration
=====================================

This document is to be shared with the candidate either just before or during their technical test (check with your recruitment partner if you're not sure).

User Story[​](#user-story "Direct link to User Story")
------------------------------------------------------

> As a user of the food ratings app I want to see food hygiene ratings as percentages in a chosen local authority so that I can understand the profile of establishments in that authority

Elaboration[​](#elaboration "Direct link to Elaboration")
---------------------------------------------------------

The existing application returns only one of two preset results. Expand the functionality to retrieve actual ratings from the Food Ratings API, calculate percentages and return them in order to the UI.

The Food Ratings API documentation can be found here: [http://api.ratings.food.gov.uk/help](https://web.archive.org/web/20230926091423/http://api.ratings.food.gov.uk/help)

In `England` the Food Standards Agency rates establishments using the `FHRS rating scheme`. This uses a star rating from 5 to 0, or "Exempt".

In `Scotland` the Food Standards Agency rates establishments using the `FHIS rating scheme`. This uses a the values "Pass and Eat Safe", "Pass" and "Improvement Required".

For the purposes of this implementation the ratings schemes shall be considered fixed and unlikely to change.

Return order[​](#return-order "Direct link to Return order")
------------------------------------------------------------

### FHRS ratings should be returned in order, as in this example[​](#fhrs-ratings-should-be-returned-in-order-as-in-this-example "Direct link to FHRS ratings should be returned in order, as in this example")

| Rating | Percentage |
| ------ | ---------- |
| 5 | 50% |
| 4 | 0% |
| 3 | 0% |
| 2 | 0% |
| 1 | 20% |
| Exempt | 30% |

### FHIS ratings should be returned in order, as in this example[​](#fhis-ratings-should-be-returned-in-order-as-in-this-example "Direct link to FHIS ratings should be returned in order, as in this example")

| Rating | Percentage |
| ------ | ---------- |
| Pass and Eat Safe | 50% |
| Pass | 15%|
|Improvement Required | 35% |

Acceptance Criteria[​](#acceptance-criteria "Direct link to Acceptance Criteria")
---------------------------------------------------------------------------------

On selecting a local authority the rating values and percentage shall be displayed.

All possible values for the relevant scheme type shall be displayed in the correct order.

Implementation notes[​](#implementation-notes "Direct link to Implementation notes")
------------------------------------------------------------------------------------

The repository contains a starter project that implements some of the functionality in a basic way.

It is recommended that candidates bring their own laptop set up with their preferred IDE, and they should download the code and get it building/running on their machine ahead of the session to avoid using up time on the day.

A sample frontend UI has already been provided and does not need to be modified during the assignment.

The Food Standard Agency's API returns JSON and you may use any frameworks you like to help support accessing the Food Standards API.

Contrary to the API documentation in recent versions, the `pageSize` parameter is not optional and must be supplied. It silently defaults to an unspecified maximum value.

The code and design should meet the above requirements, and should consider future extension or maintenance.
