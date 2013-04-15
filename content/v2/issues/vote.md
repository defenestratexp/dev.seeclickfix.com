---
title: API v2 - Issues - Vote
---

# Issue Voting

To check wether the current user has voted for an issue see the attribute `current_user_relationship` on the issue show or issue list actions.  

## Vote for an Issue

Issues can be voted on any authenticated user. Multiple votes by the same user will be ignored.

    PUT /issues/<issue_id>/vote

### Request

<%=
  json({value: 1})
%>

### Response

<%=
  json({
    metadata: nil,
    result: 'success',
    errors: nil
  })
%>

## Revoke a vote for an Issue

Votes can be revoked by any authenticated user. This removes the user's vote. It does not vote down an issue. 

    PUT /issues/<issue_id>/vote

### Request

<%=
  json({value: -1})
%>

### Response

<%=
  json({
    metadata: nil,
    result: 'success',
    errors: nil
  })
%>