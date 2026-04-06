# Lesson 3 - CIA Triad Exercise

## Status
- Not completed

## Objective
- Practice identifying whether a scenario mainly affects confidentiality, integrity, availability, or more than one of them.

## Scenario 1
- A company laptop is stolen and the disk is not encrypted.
- Primary impact: confidentiality.
- Why: unauthorized parties may read sensitive files stored on the device.
- Helpful controls: full-disk encryption, remote wipe, strong login protection.

## Scenario 2
- An attacker changes a DNS record so users are redirected to a fake website.
- Primary impact: integrity.
- Why: the information used to route users has been tampered with.
- Helpful controls: change control, multi-factor authentication, DNS monitoring, registrar lock.

## Scenario 3
- A DDoS attack takes down the public customer portal.
- Primary impact: availability.
- Why: legitimate users cannot access the service.
- Helpful controls: rate limiting, upstream filtering, autoscaling, content delivery networks.

## Scenario 4
- An employee shares a spreadsheet with the wrong external recipient.
- Primary impact: confidentiality.
- Secondary impact: possible compliance and reputational damage.
- Helpful controls: data loss prevention, access review, user awareness training.

## Scenario 5
- Malware encrypts the file server and deletes recent backups.
- Primary impact: availability.
- Secondary impact: integrity, because trusted data and backups have been altered.
- Helpful controls: offline backups, endpoint detection, privileged access control, network segmentation.

## Reflection Questions
- Which part of the CIA triad is most critical for a hospital system, and why?
- Can one control strengthen more than one part of the triad?
- Which incidents in your environment would have the highest business impact?

## Notes
- Real incidents rarely fit into only one category. The exercise is meant to highlight the dominant impact first.
