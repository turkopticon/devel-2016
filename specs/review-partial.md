# Review partial

The review partial template will be used as a view to present information from the database to the user.

# Table of contents
<!-- TOC anchor -->

- [Review partial](#review-partial)
- [Table of contents](#table-of-contents)
- [Locations](#locations)
- [Contents](#contents)
- [Appearance](#appearance)
  - [Requester page](#requester-page)
  - [HIT page](#hit-page)

## Locations

- search results
- requester page (all reviews for a given requester)
- HIT page (all reviews for a given HIT)
- review page (specific review and its child comments)
- my reviews
- reviews by user
- reviews flagged by user

## Contents

- requester name (except on the requester page and the HIT page, where it will appear at the top of the page)
- HIT title (except on the HIT page, where it will appear at the top of the page)
- completion time (how long it took the reviewer to do the HIT)
- HIT pay
- hourly wage computed from the HIT pay and the completion time [in USD and INR?]
- time the requester took to approve or reject the HIT
- how many of the HITs the reviewer did (none, one, or more than one)
- tags
  - `violates TOS` (reviewer checked `violates TOS` in review)
  - `deceptive` (reviewer checked `deceptive` in review)
  - `broken` (reviewer checked `broken` in review)
  - `good response` (reviewer attempted communication and requester provided satisfactory response)
  - `bad response` (reviewer attempted communication and requester provided unsatisfactory response)
  - `no response` (reviewer attempted communication and did not provide any kind of response)
  - `would recommend` (reviewer checked `yes` to 'would you recommend this HIT')
  - `wouldn't recommend` (reviewer checked `no` to 'would you recommend this HIT)
- body of the review
- reviewer's display name and a link to their reviews (except on 'my reviews' and 'reviews by user X', where it will appear at the top of the page)
- time the review was posted
- if the logged in user is allowed to flag reviews, a link to flag the review
- if the logged in user is allowed to comment, a link to post a comment on the review

## Appearance

### Requester page

- three columns
  - first column with header "Requester summary"
    - the requester name
    - a list of the requester's aliases
    - the requester's MTurk requester ID
    - a link to add a review for the requester [but for which HIT?]
    - a link to the requester's HITs on MTurk
  - second column with header "last 90 days"
    - the number of reviews [? -- this is the same as the 'base' number in 'would recommend']
    - the average wage (in USD and INR? let the user decide?)
    - the average time to review
    - the percentage of people satisfied with the requester's response to communication, of those who tried to communicate (e.g., "76% of 5 satisfied with response")
    - the percentage of people who said they would recommend the HIT
    - all on one line (e.g., "2 violates TOS, 3 broken HIT, 1 deceptive"; if any are zero, leave out):
      - the number of "violates TOS" checks
      - the number of "broken HIT" checks
      - the number of "deceptive" checks
  - third column with header "all time"
    - same figures as middle column, but aggregated without date restrictions

If there are no reviews older than 90 days, only the "all time" statistics will be shown, in the second column, and there will be no third column.

### HIT page

Same as requester page with the follow exceptions:

- the first column header will say "requester info", not "requester summary"
- change links in the first column
  - "add a review for this HIT"
  - "find this requester's HITs on MTurk"
- all aggregates will be over reviews for the given HIT only


