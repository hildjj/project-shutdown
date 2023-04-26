# Shutting Down an Open Source Project

Say you maintain a piece of open source software that is used by other people,
and you decide that your project should no longer be available.  Some possible
scenarios:

- Your project makes it easy to use a corporation's REST API in a particular
  language, and that corporation has started to act in ways you think are
  incompatible with the kind of society you want to live in.
- You should have realized that the main use for your project was to create
  scams or distribute the sort of content that all file transfer projects are
  used for, and you have a sudden flash of moral insight.
- Someone makes a compelling legal case against you, and your lawyer says it's
  time to take down your code.
- There's a better package out there now since you wrote it, and in
  the spirit of "less, better, software"
  you want to encourage people to use the better package and contribute fixes there, rather than using yours which has now numerous bugs and security issues, runs on an old framework etc etc.
- You wish to retire from maintaining this code for personal or
  professional
  reasons.
- (TODO): more examples here, please.  I'd like people who are
  directed here
  to see a use case that they identify with.

How do you take down your project correctly?  What is the industry best
practice?

## Goals

- Fewer people are surprised when your project stops working.
- You have the choice of spreading the word about *why* you are
  stopping your project, so that you might influence others might make similar
  choices.
- You have the choice of making it easier or more difficult for someone else
  to fork the code and take over maintenance.
- You have the choice of trying to remove your name from future forks of the
  project.  This might not be possible in practice.
- All decisions are explicit and documented.
- There is recourse for the other parties in the discussion to change your
  mind.
- You have displayed systematic empathy for all of the participants in your
  ecosystem.  You've thought through how this is going to affect them and made
  intentional decisions about them.
- You have a draft communications plan for how to notify everyone you can.
- You are not seen as "going rogue" and taking down a larger chunk of the
  Internet than you intended.  Nobody suspends any of your accounts you still
  want.
- You have some recourse to objections, even if it's just "I followed the
  industry best practice".

## Non-goals

- Making it impossible for someone to fork from a previous version.  Assume
  that your project has been published with a permissive license, so any copy
  of the code anywhere is a legitimate starting point for someone else.
- Speed.  Doing this carefully is more important than hitting a news cycle.

## Disclaimer

There are no lawyers involved in this project yet.  Laws vary widely around
the world.  Nothing in this project is legal advice or should be construed
that way.  Please consult your own lawyer familiar with the laws of whatever
locales are important to you when you need legal support.

## History

Examples of previous times this has gone wrong:

- [left-pad](https://qz.com/646467/how-one-programmer-broke-the-internet-by-deleting-a-tiny-piece-of-code)
- [colors and faker](https://www.bleepingcomputer.com/news/security/dev-corrupts-npm-libs-colors-and-faker-breaking-thousands-of-apps/)
- (TODO): Add more

## Approach

We will iterate on a [checklist](shutdown-steps.md).  See the
[contribution guidelines](CONTRIBUTING.md).

The first thing being considered is node packages published in NPM, because
that's the first project the original author was interested in shutting down.
There will likely need to be multiple sub-lists for different kinds of
projects as people want to work on those.

Decision making will be by fiat after discussion until we get to the point
where we need something else.

## Reading List

These are things that you'll want to have read before wading in:

- [npm deprecation guidelines](https://docs.npmjs.com/deprecating-and-undeprecating-packages-or-package-versions)
- [npm unpublish policy](https://docs.npmjs.com/policies/unpublish)
- [node's util.deprecate](https://nodejs.org/dist/latest-v19.x/docs/api/util.html#utildeprecatefn-msg-code)
- [Remember When We Broke the Internet?](https://www.youtube.com/watch?v=uvdzTD6ZAlY) ([slides](https://docs.google.com/presentation/d/1JWzE92jykf7PwMFFCwzr4ok8A2bwKv8yHXvZ2uGy0bs/edit#slide=id.gf71d39d4d6_0_0))
- [Corporate open source shutdowns](https://github.com/todogroup/guides/blob/master/shutting-down-an-open-source-project.md#killing-a-project-outright)

## Other Languages/projects

### Rust

- [Rust's `#[deprecated] attribute](https://doc.rust-lang.org/reference/attributes/diagnostics.html#the-deprecated-attribute)
- [Rustsec Advisory database](https://github.com/RustSec/advisory-db) In the Advisory Format note `informational = "unmaintained"`

## License

MIT
