# Lab 4 Part 2: RLS Security Test Matrix

## Purpose
Verify that Row-Level Security (RLS) blocks unauthorized database access.

| ID | Scenario | Expected result | Actual result |
|---|---|---|---|
| RLS-01 | Public user reads an approved property | Allowed | Not tested |
| RLS-02 | Public user reads an unapproved property | Denied | Not tested |
| RLS-03 | Public user reads an active sponsor | Allowed | Not tested |
| RLS-04 | Public user reads an inactive sponsor | Denied | Not tested |
| RLS-05 | Owner updates their own unapproved property | Allowed | Not tested |
| RLS-06 | Owner updates another owner's property | Denied | Not tested |
| RLS-07 | Owner changes their own property to approved | Denied | Not tested |
| RLS-08 | Unauthenticated user reads private inquiries | Denied | Not tested |
| RLS-09 | Owner attempts to grant themselves admin privileges | Denied | Not tested |
| RLS-10 | Unauthorized user attempts to delete protected data | Denied | Not tested |

## Testing notes
- RLS must be enabled on every table.
- Test using separate public, owner, and administrator database roles or authenticated identities.
- Verify both rows returned by SELECT and rows affected by UPDATE or DELETE.
- Record actual results only after running the tests.
- Administrator permissions must use trusted server-side authorization.
