[teams]: https://github.com/hmc-cs111-fall2016/language-design/wiki/Teams
[betterdesign]: https://www.fastcompany.com/1665735/why-arent-computer-programming-languages-designed-better
[apipdf]: https://dl.acm.org/citation.cfm?id=1176617.1176622&coll=DL&dl=GUIDE&CFID=372348918&CFTOKEN=51331222
[apitalk]: https://www.youtube.com/watch?v=aAb7hSCtvGw
[growpdf]: https://www.cs.virginia.edu/~evans/cs655/readings/steele.pdf
[growtalk]: https://www.youtube.com/watch?v=_ahvzDzKdB0
[whenandhow]: http://dl.acm.org/citation.cfm?id=1118892
[applescript]: https://dl.acm.org/citation.cfm?doid=1238844.1238845
[whatisgray]: http://lea.verou.me/2014/07/an-easy-notation-for-grayscale-colors/
[languagestereotypes]: https://modelviewculture.com/pieces/c-is-manly-python-is-for-n00bs-how-false-stereotypes-turn-into-technical-truths
[arrgh]: http://arrgh.tim-smith.us/
[perl]: https://dl.acm.org/citation.cfm?id=2089159&CFID=578519747&CFTOKEN=43192998

# Language Design

In this assignment, we will focus language design. The goals are to:

- find ideas that are new and interesting to you or which are presented in
  new and interesting ways
- identify good and bad practices for language design
- understand more about the benefits and drawbacks of DSLs
- challenge your currently held beliefs about programmers and programming
  languages

To do so, you will read about language design, then answer some questions, citing
the readings as evidence.

## Teamwork

You can work with a partner or by yourself. If you work with a partner, only one team
member needs to fork this repository.

## The Readings

Here are the readings, in their recommended (but certainly not required!) order.

1.  [_Growing a Language_][growpdf] by Guy Steele
    - cite as: [Steele, 1998]
    - This one starts out a little weird, with some anachronistically gendered language,
      but hang with it.
1.  [_Why Aren't Computer Programming Languages Designed Better?_][betterdesign]
    by John Pavlus
    - cite as: [Pavlus, 2012]
1.  [_How to Design a Good API and Why It Matters_][apipdf]\* by Joshua Bloch
    - cite as: [Bloch, 2006]
    - There is also a [talk][apitalk], which expands on the tips in the
      reading and provides lots more detail. Feel free to use the talk to
      understand this material better, or as extra supporting material. If you
      cite the talk, cite it as [Bloch, 2007] _and_ provide [a link to the time at
      which the material you cite occurs](http://www.wikihow.com/Link-to-a-Certain-Time-in-a-YouTube-Video).
1.  [_An Easy Notation for Grayscale Colors_][whatisgray] by Lea Verou
    - cite as: [Verou, 2014]
    - An interesting post on how to choose a name for _one_ feature of an
      API. The comments are a good source of additional material.

_\*This paper belongs to the Association for Computing Machinery's digital
library. You should be able to access them from any computer on the Claremont
Colleges' network. If you have trouble accessing, please post on Piazza._

Each reading also describes how to cite it. For example, if you are going to
cite the Steele paper in your responses, you might write something like:

> "Domain-specific languages are the best thing ever, except for taking a class
> _about_ domain-specific languages, which is better than petting unicorns"
> [Steele, 1998].

_(not an actual quote)_

## The Responses

After completing the readings, answer the questions in `language-design.md`
(see the suggestions below for how to approach the writing).

## Grading

Good responses will:

- state a clear opinion
- support the opinion with evidence from the readings, cited properly
- be well-written, i.e., clear yet concise, and organized to convey a well-formed idea
- (if you are working with a partner) be the result of teamwork. A response can have
  multiple opinions, e.g., if the two of you disagree about something. The only
  requirement is that the response contain the ideas and efforts of both
  partners.

Great responses will go a bit beyond, e.g., by using (and citing) a source outside of the
readings. Here are some excellent additional readings:

- [_C is Manly, Python is for “n00bs”: How False Stereotypes Turn Into
  Technical "Truths"_][languagestereotypes] by Jean Yang & Ari Rabkin
  - cite as: [Yang and Rabkin, 2015]
- [_When and How to Develop Domain-Specific Languages_][whenandhow]\* by
  Marjan Mernik, Jan Heering, and Anthony M. Sloane
  - cite as: [Mernik _et al._, 2005]
  - Of most interest might be sections 1 and 2.
- [_aRrgh: a newcomer’s (angry) guide to R_][arrgh] by Tim Smith
  - cite as: [Smith, 2016]
- [_An empirical comparison of the accuracy rates of novices using the quorum, perl, and randomo programming languages_][perl]\* by Andreas Stefik, Susanna Siebert,
  Melissa Stefik, and Kim Slattery
  - cite as: [Stefik _et al._, 2011]
  - Raises the question: Is Perl's syntax design any better than a randomly
    designed syntax?

_\*These papers belong to the Association for Computing Machinery's digital
library. You should be able to access them from any computer on the Claremont
Colleges' network. If you have trouble accessing, please post on Piazza._

These readings take various forms, including peer-reviewed, academic papers
and popular-press articles.

## Suggestions for working on the assignment

Although the responses should be clear and cite evidence, they do not need to
be formal. It's fine to say "Jordan believes _A_ because _X_. Napur disagrees
because _Y_." (where Jordan and Napur are the two people writing the response).

Here are some suggestions for how to work on this assignment. Following these
suggestions should produce good work; but you will be graded on your work, not
on whether you followed these suggestions. (In particular, we won't be grading
based on word count. We'll be grading on whether the work satisfies the criteria
above.)

1.  Read over the questions you'll be answering.
1.  If working in a team, do the readings together or separately, your choice. Either way,
    discuss things that interested you both or that one or both of you doesn't yet
    understand.
1.  Draft an outline of your response. (If you are working in a team, do this together.)
    The outline should be at the pseudocode level, i.e., clear enough that someone writing
    the full version doesn't have to make significant decisions about what to write.
1.  Draft an initial version of the response. (If you are working in a team, you don't
    have to do this together. If the outline is sufficiently specific _and_ it contains
    both your ideas, you can divvy up the writing responsibilities.) A good response will
    probably be 250-500 words (shorter for the questions with smaller scope, longer for
    the more open-ended questions).
1.  Iterate until you're satisfied.

## Peer-review

After the submission deadline, I will post critique partners. Each person will add
feedback to someone else's work; though that might mean that some people receive multiple
critiques. You don't need to cover _all_ of your partner's work. It is better to provide
quality feedback on one part than to provide shallow feedback on lots of things.

Here are some suggestions for critiques:

- Find something in their work that interests you, and engage in that.
- Did they have a different opinion than you? If so, have they changed your
  mind? How so?
- Did they have the same opinion as you? If so, did they support it in the
  same way that you did (e.g., using the same sources). Do you have any
  additional evidence that might bolster their claim / opinion?
- Did they mention part of the readings that you had missed, but which you
  find interesting? In what way does it relate to the work that you submitted?
- Is their idea / opinion clear? Is it novel to you? Let them know!
  If the work is not clear, which aspect is unclear? How could they help you
  understand better?

## Tasks

- [ ] Read all the things :)
- [ ] Write all the responses :).
- [ ] Submit your work.
- [ ] Comment on your critique partners' work.
