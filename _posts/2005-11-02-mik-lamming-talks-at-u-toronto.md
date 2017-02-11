---

date: 2005-11-02 18:12:51+00:00
title: Mik Lamming talks at U Toronto
---

Mik Lamming from HP  Labs came to talk today.  He presented his work on ubiquitous, peer-to-peer "Minders", which are RF-capable devices, small form factor, which can sense presence of their peers.  The applications are pretty immense.  He talked of using one Minder on a patient with dementia, and another near, say, the toilet.  The toilet Minder would detect unusual amount of time, indicating perhaps that the patient had fallen, and somehow alert a caregiver.  I wasn't clear on how the Minders uploaded data; he had a basestation type device which would download the data when placed near a Minder, but they didn't seem capable of alerts or anything like that.  I suppose that properly configured they could alert a chain of other peers and eventually filter that information to a more centralized hub.

The point was that the system was about personal control of the system, i.e., no central agency is monitoring you, the data stays with the Minders.  I suspect that won't last long, however.  There are valid reasons to want to have a third-party access the logs, placing the onus on the designers to come up with a thorough security model (no drive-by decoding, for example).

He had some interesting things to say about the path to where they are now (wristwatch sized devices).  He noted that he strongly believes, when building devices/applications for a certain problem, that you need a measurable goal.  For example, they used the goal of reducing caregiver burnout.

He participated in the ActiveBadge system and one of the lessons he had was that you needed to minimize the burden on the users, e.g. setup.  Based on that, Lamming prefers detecting proximity over detecting location (e.g. I'm near A, not I'm in my house in Palo Alto).  RFID technology he rejected due to its power demands on the reader, orientation problems -- essentially he feels the technology isn't yet good enough.

Lamming noted that it was essential to keep trust in the system.  In particular, he noted dead batteries as a serious problem for trust.  For example, you might use it to keep track of all your items.  If you forget something and aren't warned, it's unlikely the user will bother again.  In a similar vein he noted how crucial it was for the devices to either be extremely small (coin sized) or very cool, like an Ipod Shuffle.  Otherwise no one will bother.
