# jQuery Foundation Project Lifecycle

## Project Definition

The jQuery Foundation hosts several Projects. These Projects are autonomous from
each other. Projects are governed by Technical Steering Committees (TSC) which
are chartered by the jQuery Foundation Collaboration Board (CB). The CB also
charters its own Working Groups for Foundation-wide and/or cross-TSC
initiatives.

```
 CB
  |
  |-- TSC 1 (Chartered By CB)
  |       |-- Project A (Chartered by TSC)
  |       |-- Project B (Chartered By TSC)
  |
  |-- TSC 2 (Chartered By CB)
  |       |-- Project C (Chartered by TSC)
  |       |-- Project D (Chartered by TSC)
  |       |-- Project E (Chartered by TSC)
  |
  |-- Working Group A (Chartered by CB)
  |-- Working Group B (Chartered by CB)
```

TSCs may nominate a representative to be elected to the CB when a CB seat is up
for election. TSCs with *mentorship* status are not granted voting privileges on
the CB.

## Mentorship

The purpose of mentorship is to support and mentor projects entering the
Foundation. The goal is for projects to be:

* Participatory
* Transparent
* Effective

While certain processes are strongly recommended based on the experiences of the
Foundation and its projects, the goal of mentorship is not to enforce a specific
set of processes but to ensure that the processes adopted and accepted by a
project achieve these goals. Therefore, the requirements for graduating from
mentorship are based on metrics that demonstrate success in terms of these
values. These metrics are:

* TSC is 5 members or greater and the TSC must have at least 1 representative
from each Project.
* No more than 1/3 of the TSC is affiliated with the same employer.
* No more than 1/3 of any Project is affiliated with the same employer.
* The decision making and release process is documented and publicly accessible.

A TSC and its Projects may apply to graduate from mentorship at any time by
calling for a vote in the CB.

While a project is under mentorship, it is assigned at least 2 [mentors][] who
are responsible for working with the project to adopt policies and gain the
health and contributorship it will need in order to graduate from mentorship.
The mentor list is nominated and approved by the CB and is expected to be larger
than the CB.

## Lifecycle

The Foundation shall encourage new Projects and innovation in the community. New
Projects enter the jQuery Foundation through a [Proposal][].

The Project should be considered mature and have a history of releases before
applying to enter the Foundation.

## TSC and Working Group Requirements

All TSCs and WGs are expected to operate in a transparent manner. Decisions must
be made publicly through a documented public process managed by each TSC or WG.

All TSCs and WGs must use a participatory decision making process.

### Security

All Projects in the Foundation share the same base security policy. The
Foundation's security team triages issues sent to security@jquery.org.

## Decision Making Process

All TSCs and WGs must follow a [Consensus Seeking][] process and are responsible
for documenting and keeping up to date their current processes and practices.

Each TSC may nominate a representative for election to the jQuery Foundation CB
or vote to abstain from representation on the CB.

## Applying to join

A proposal to join the jQuery Foundation as a Project or Working Group must
include:

* Introduction and Project description.
* Project history.
* Any available metrics or even estimates about the user base, ecosystem
and community.
* Project scope.
* Current governance process.
* Current contribution process.
* List of current tools in use by the project (forums, issue trackers,
  GitHub orgs, etc).
* Existing IP Policy and relevant intellectual property (trademarks,
  domain names, etc).
* List of initial Project members.
* List of potential TSC member(s).
* List of initial Working Groups.
* Prior to being admitted, the project must include:
 * [CLA][]
 * an [approved license][]. If it is not currently under an approved license, it
 will need to be cleared by the CB and the jQuery Foundation Legal Committee
 prior to acceptance into the mentorship program.
 * a [Code of Conduct][].

Each proposal should be sent as a pull request to this repository in the
Applications directory. Proposals do not have to be complete to be submitted,
the CB can work with the authors and their respective communities in each pull
request.

### Approved Licenses

At this time, the Foundation's approved licenses include MIT, BSD, ISC or
Apache2 license. Other licenses may be accepted on a case-by-case basis.

### Admittance

The jQuery Foundation selects Projects for admission as mentors become
available.

You may apply at any time and the CB and available mentors will help improve
your application while awaiting the next available approval phase.

[mentors]:https://github.com/jquery-foundation/CB/blob/master/README.md#mentors
[Proposal]: #applying-to-join
[Consensus Seeking]: https://en.wikipedia.org/wiki/Consensus-seeking_decision-making
[CLA]: https://contribute.jquery.org/CLA/
[approved license]: #approved-licenses
[Code of Conduct]: https://jquery.org/conduct/
