# Shutting Down an Open Source Project: Steps

## Initiation Phase

- [ ] Determine why you want to do this.
- [ ] Either write a document describing your reasons, or have access to someone else's writing.
- [ ] Ensure your communication plan is filled out
- (TODO): Lots more steps.

## Research Phase

- [ ] Determine any potential legal obligations from existing Service Reliabilty Obligation (SRO) documents (if they exist)
- [ ] Determine customer impact of service termination
  - How many known customers?
  - Do those customers offer a service as well?
  - Is it possible to reach out to the impacted primary customers?
- [ ] Determine customer mitigation steps.
  - Is there a replacement availble to customers?
  - Can they run a temporary "stand-alone" version?
  - Is there a vetted, trusted party that can take on the library?
- [ ] Determine appropriate lede time before official sunsetting.
  - Large systems (e.g. languages, APIs with thousands of users, etc.) require a minimum of 1 calendar year. Small systems (2 or 3 customers) may only require 2 weeks. A bit of empathy for the overworked, highly distracted devs is a well earned kindness. Folk have a remarkably long memory about these things.
- [ ] Determine end of life date.
  - This date should occur in the first half of the common work week, ideally when the greatest population of users are least likely to be impacted. Be mindful of major holidays (even ones that your culture may not actively participate in.) Don't burn someone's weekend or make them log in from the beach.
- [ ] Determine communications avenues to primary customers
  - How will the library / service indicate the end of life to it's customers?
  - How can you contact major customers / peers at other organizations?

## Announcement Phase

- [ ] Determine One source of Service Halting Truth (OSHT) (e.g. the repository README, project site, etc.)
- [ ] Add appropriate links to published library information pointing to OSHT. (e.g. online documentation, promotional sites, mail services, etc.)
- [ ] Add internal messaging (e.g. WARN logging messages on library initialization, response meta data (if possible) indicating service termination, adding "OBSOLETE" flagging to library functions, submitting planned abandonment notices to CVE monitoring, etc.) that point to the OSHT for detailed information.

## Shutdown Phase

- [ ] For services: Introduce artificial delay to the called functions / slowly diminish service availability. (You're trying to get the attention of the Dev/SRE/Ops person watching the metrics. Not everyone follows your CHANGELOGs.)

See additional set of steps for your type of project:

- [npm](shutdown-steps-npm.md)
- [rust](shutdown-steps-rust.md)
- [services](shutdown-steps-service.md)

## Followup Phase

- [ ] Monitor social media
- [ ] Be willing to change your mind
- [ ] What to do if you get a lawyer letter?
