# Database

This document does not describe the full spec of the entire database, only what's relevant to this project.

## Tables

### People

- id

### Requesters

- id (internal)
- amzn_requester_name
- amzn_requester_id

### Reviews

- id (internal)
- person_id (internal ID of actor user account)
- hit_id (internal)
- broken (bool)
- broken_info (text)
- tos_viol (bool)
- tos_viol_info (text)
- deceptive
- deceptive_info (text)
- how_many ("none", "one", "some")
- completion_time (int - seconds)
- work_reviewed (bool)
- review_time (int - days)
- rejected ("yes", "no", "some")
- tried_to_communicate (bool)
- satisfactory_response (bool)
- body
- created_at
- updated_at
