# Ceph Request for Comments (RFC)

A Ceph RFC intends to propose a new large feature or change to the larger Ceph community.
It is meant to gather feedback from the community at large, and from folks with domain specific knowledge.
Additionally, it is meant to help understand and define what "done" means for a large feature.

## Participation

There are a number of people who will participate in an RFC.

**Anyone** in the community is invited to comment on an RFC within the merge request that it might be introduced in.

The **Status** of the RFC will define where in its lifetime it is.
The valid status values are: `Draft`, `Feedback Requested`, `Active`, `Abandoned`, and `Retired`.

A **Sponsor** is a company or individual maintainer with domain specific knowledge that will assist the author(s) in moving the RFC through the process.
It may be a CLT member, or experienced developer.

One or more **Authors** will write and lead the RFC.
These are the people who will submit the RFC for review, and who are expected to respond to comments and feedback.
The authors can be anyone within the community.
If the author is an employee of the sponsoring company, there must be an additional approver.

The **Change Impact** is a list of subsystems within Ceph that the RFC will affect.
It is expected that at least one subsystem will be affected by any authored RFC.

<!-- TODO: figure out how this might work with a git flow -->
<!--       as written below, it implies the RFC will be merged early, and updated often which is potentially a lot of churn -->
<!--       it might make more sense to do this all in one MR, but require approvers to be named -->
There is expected to be at least one **Approver** for an RFC.
There is a table that lists each approver, and the state that they are in.
The approvers are folks that are explicitly requested to review the RFC, and should have a solid understanding of their content.
As an RFC may take some time to complete, there are a number of states that an approver may be in:
`Not Started`, `Under Review`, `Pending Feedback`, `Approved`, or `Rejected`.
Approvers must update their own state in the table for at least the final `Approved` or `Rejected` state.
