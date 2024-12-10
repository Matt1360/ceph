# RFC: My Project

| Key                        | Value |
|:-------------------------: |:----- |
| **Status**                 | Draft |
| **Sponsor**                | [DigitalOcean](https://digitalocean.com) |
| **Author(s)**              | [@matt1360](https://github.com/matt1360) |
| **Change Impact**          | RADOS, RBD, scrubbing |
| **Original Merge Request** | (reference link to the MR where this was introduced) |

### Approvers

People who have approved this RFC, along with the date of their approval.
The state may be one of `Not started`, `Under review`, `Pending feedback`, `Approved`, or `Rejected`.
One approver **must** be the sponsor, or an individual from the sponsoring company.
If the author is an employee of the sponsor company, another approver **must** be listed.

| **Approver** | **State** | **Date** |
|:------------ |:--------- |:-------- |
| [@matt1360](https://github.com/matt1360) (DigitalOcean) | Approved    | 2024-12-10 |
| [@zdover23](https://github.com/zdover23)                | Not Started | YYYY-MM-DD |

## Problem Statement

The thing that describes an existing limitation or missing feature.
The reason this RFC comes to be.

## Current Process

How we approach the problem today.
A few paragraphs as necessary to expand on the problem statement.
Describe any manual process here, steps required to remediate, etc.
For a new feature, there may not be a current process, and that’s okay.

## Problem

We sometimes describe the different problems faced that this RFC may aim to address.
Examples include:

1. Opportunities for user error
1. Cost in engineering time
1. Complexity
1. Missing history, missed opportunities
1. Scope too limited
1. Other limitations

## Opportunity

Describe opportunities this RFC may help realize.
Wins in turnaround time for operators, devs, etc.

## Considered Solutions

1. **Do Nothing**\
   The “Do Nothing” solution should always be considered, and should describe what is expected over time if nothing is done, or if this RFC were not acted on.
   This could include a description of burden on different people, increasing complexity, etc.
   It is meant to be forward looking, so it should consider growth of scale.

1. **Some Other Solution**\
   A possible solution should be described here.
   Link to possible pre-existing possibilities, such as “we could leverage [`ceph_exporter`](https://github.com/digitalocean/ceph_exporter), or [`pgremapper`](https://github.com/digitalocean/pgremapper)”.
   Describe how this solution might be leveraged assuming this were a solution that might use existing tools.

1. **The Solution We Want**\
   A possible solution that might be what the RFC author is looking to implement.
   This should describe the benefits of going down the path of implementing a new thing.

## Proposed Path

The proposed path is a pick from the list of solutions above.
It should expand on that section with more detail.
It may describe dependencies this solution may rely on (does it need `rocksdb`?), for example.
If it needs to communicate with another service, it should detail what protocol is used, whether it’s `gRPC` or likely more relevant, using the `AsyncMessenger`.
Is the `mon` or another daemon involved?
A dependency callout is important to ensure no circular dependencies are built.
It should define the path towards completion, and effectively describe what done looks like.

## Dependencies

An explicit callout to each dependency required for this RFC.

1. `mon`  
   The `mon` is needed for this path because we need to add some config option to it.

## User Impact

<!-- TODO: decide on inclusive terminology to bridge the gap between users, operators, and devs -->
How will this change affect users at different scales?
Do cluster operators need to perform any migration, or change configuration to enable the change?

## Development Plan

This generally describes the path we intend to use for development.
The cycle here may vary, but a suggestion might be to iterate through proof of concept, MVP, Release Candidate, Release, and Future.
It should describe what is expected in each of these states.
Is scrubbing expected in the MVP, and repairing in the RC?
When do some dependencies come into play?
