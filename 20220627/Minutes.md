# ROLL Interim Monday 27th June 2022
From 14:00 to 15:00 UTC
---

# Agenda

|       Time       |  Duration |           Draft/Topic           |    Presenter    |
| ---------- | --------- | ------------- | ---------- |
|   14:00 - 14:10  |   10 min  |            WG Status            |  Ines/Dominique |
|   14:10 - 14:25  |   15 min  |     draft-ietf-roll-aodv-rpl    |      Charlie    |
|   14:25 - 14:40  |   15 min  |  draft-ietf-roll-dao-projection |     Pascal      |
|   14:40 - 14:55  |   15 min  |       draft-ietf-roll-rnfd      |     Konrad      |
|   14:55 - 15:00  |   5 min   |            Open Floor           |     Everyone    |

# Summary of action points

# Meeting notes (time in UTC)

## [14:0x] Meeting starts

* note well, scribes
* agenda

## [14:0x] WG Status

* planning for IETF114.

## [14:13] draft-ietf-roll-aodv-rpl (Charlie)

* goes through AODV RPL overview. New multicast group all-AODV-RPL-nodes
* Pascal: Instance ID is unique within domain of root node
* Charlie: 
* when TargNode receives RREQ, the InstanceID in RREQ might hae already been used by TargNode for something else. Delta is used to establish correspondance between RREQ and RREP InstanceIDs.
* if intermediate router does not recognize AODV option, would drop option but still forward DIO. Could be problematic. New multicast group for AODV RPL routers solves this.
* Dominique: lot of progress happened in the last weeks. Some more time needed to converge, then LC.

## [14:35] draft-ietf-roll-dao-projection (Pascal)

* major text rework in -21 to make draft more readable
* more reviews still welcome.
* Konrad willing to review 2nd half Sept.
* Submission to IESG likely to take place before that.
* Review still useful in Sept, make sure to grab the latest revision at the time you are ready to review

## [14:46] draft-ietf-roll-rnfd (Konrad)

* Overview of the draft
* Looked at open source RPL implementations behavior in the face of an LBR crash.
* Proposed a specific algorithm for fast BR crash detection.
* Sentinel nodes exchange information between them about the suspected status of the BR.
* MCR suggested Experimental status. Less "friction" to publish.
* Pascal: in worst case, the first circle is hub-and-skope, sentinel don't hear one another.
* Konrad: if there's any connection between the sentinel, even through the edge, the consensus will work.
* Psacl: what if many links to the root fail?
* Konrad: then it's probably a good idea to kill the DODAG and rebuild
* Pascal: why not ask the root if it is dead?
* Dominique: let's discuss on the ML, or at next meetings.

## Open Floor


## [15:03] Meeting adjourned
