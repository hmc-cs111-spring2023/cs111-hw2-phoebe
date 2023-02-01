_Fill in each this file with your responses, placing each response after its
corresponding question._

---

**Question**

Pick three quotes from the readings about language design. Good candidates
are:

- Something you agreed with / resonates with your own experience
- Something you disagree with
- Something that is interesting, a new idea or perspective you'd like to remember
- Something you didn't understand

For each quote, describe what it was about the quote that led you pick it.

**Response**

“Obey the principle of least astonishment” [Bloch, 2006].
In the talk, Bloch also mentions that it’s worth the extra implementation effort and even [reduced performance](https://youtu.be/aAb7hSCtvGw?t=1543).
I agree with this sentiment. APIs should name things as closely as what the method or field does, no more and no less. If there are side effects to some API calls that are important to know, it is better to take another look at the implementation and see if these side effects can be removed or extrapolated into a different method. 

“Provide Programmatic Access to All Data Available in String Form” [Bloch, 2006].
This is a really specific maxim from Bloch paper, but I see the importance of this and would also like to remember it better. There are so many examples of this in action in existing protocols, such as reporting HTTP status. The convention to report contain a numeric code and a corresponding short message describing the status or exception. Another form that I recently used is using images in Android Compose projects. While I can directly specify the string path to the file, the file structure of Compose allows for a neat [abstraction](https://developer.android.com/guide/topics/resources/drawable-resource) that creates an int variable with the name as the file name to refer to the image in code.


“In other words, a good programmer does language design, though not from scratch, but by building on the frame of a base language” [Steele, 1998].
I think this quote from _Growing a Language_ is particularly interesting because of its ties to internal versus external DSLs from last week. If taken more literally, this quote seems to advocate for internal DSLs because they can take advantage of the frameworks of the general-purpose language they use easily. 
This quote also made me think of levels of interoperability between language “families” like C/C++ and Java/Kotlin. C and C++ are similar, but they seem to require a lot more scaffolding for writing and running their code interchangeably. In contrast, Kotlin is aimed as an evolution of Java and these languages are interoperable, so it seems like Kotlin takes more advantage of its “base” language.

---

**Question**

How would you know a well-designed language? What are the symptoms? How would
you know a poorly designed language? What are the symptoms?

**Response**

Overall, a well-designed language should be accessible to both new and old adopters.

According to Steele, a well-designed language should start off with a small set of words and rules, but has patterns and mechanisms built on it that make adding to this language easy with the help of users. Bloch’s maxims provide a good rule of thumb to building that initial set, specifically: “When in doubt, leave it out” [Bloch, 2006]. To borrow lingo from software development, a scalable language is one that implements what is only needed now but leaves leeway for future development. 

Characteristics of a well-designed language are modularity within the language and active hubs of users discussing the language. Modularity can come in the form of libraries and packages, which add vocabularies and rules that can make specific tasks easier. One concrete example may be the Log4j or Logback Java libraries for recording logs of software activity. Active user hubs indicate that there are users who can help grow the language to suit needs as they arise. 

In contrast, a poorly-designed language can be one that is difficult to change. Symptoms of this may be low user interactivity, and nonexistent forms of version control for the language. Poorly-designed languages are also not intuitive to use. This can mean going against expectations of natural language flow. For example, initializing atomic vectors in R with numbers like 1 may seem like the atomic vector created contains integers. However, R interprets them as floating-point values [Smith, 2016]. Comparisons to other languages popular for their obscure wording or ways of computing may also be a sign of poor design; R is often compared to and used with Perl, a language the Pavlus reading describes as “no more intuitive to novices than a language with a randomly generated syntax” [Pavlus, 2012].

---

**Question**

How might the themes of _Growing a Language_ relate to notions of fluency from last week's
class?

**Response**

The Fowler reading emphasizes limited expressiveness, noting that “the domain focus… is merely a consequence of the limited expressiveness” of DSLs. The action of starting with a small language is to create that limited expressiveness for a nascent language. This strategy prevents potential adopters from being overwhelmed by a newly developed language. Similarly, DSLs can suffer from language cacophony - that DSLs become another set of words to learn, making users reluctant to adopt them despite their potential usefulness.

_Growing a Language_ also mentions the bazaar/shopping mall as an analogy for building mechanisms to encourage users to grow languages as the needs of users grow. This constant polling of information from users is important in developing DSLs too. Fowler sees DSLs as reading material for domain experts, thereby improving mutual understanding of the needs between these experts and engineers. 

_Growing a Language_ talks about libraries, using the example of Java generics as one potential library to help implement many use cases more efficiently. In the section Improving Development Productivity, Fowler talks about an example of “using a DSL to wrap an awkward third-party library”. DSLs and libraries in this scenario have the same intent - to ease frictions in programming a set of operations.



---

**Question**

In what way is an API a language?

**Response**

Developing a new API is similar to creating a language. Like languages, APIs should start off small, where “early drafts of APIs should be short, typically one page” [Bloch, 2006]. “An API should be as small as possible but no smaller” to satisfy its requirements, and “when in doubt, leave it out” [Bloch, 2006]. This maxim’s intent is to hone in on what is really needed at the current moment, just as languages may delay certain unnecessary but ease-of-use features for a future version. APIs can also have the same problems of unintuitive wording as languages like Perl. Therefore, “API design is not a solitary activity” [Bloch, 2006] - user input can help determine how intuitive and easy the API is to use. 

Steele claims that language design should be defined as “a pattern for language designs”. APIs should also have a defined pattern so that amendments to the API can follow that pattern. Bloch’s maxims on the “right” data types, parameters, return values, and exceptions are all suggestions to create a pattern that is easy to read and formalizes how future changes should be made.

To sum up these points, both APIs and languages aim to balance two objectives - “minimizing conceptual weight” [Bloch, 2006] while having enough bulk in types, methods, and other mechanisms for ease of use. 

---

**Question**

What does the post on grayscale tell us about the process of API design?

**Response**

The post on grayscale tells us that API design should be tailored for an envisioned end-user group and take into account the technological contexts in which this API is used. Nonetheless, these objectives can be paradoxical. It seems that the author envisions multiple and conflicting groups in this API that would have different notions for the most intuitive name of a grayscale function. Therefore, they turn to prior knowledge they presume most people would have - such as “grayscale printing”. A comment made by user David Moore in the post suggests grayscale(lightness [, alpha]) as the method name, and user Robin Nixon agrees because “grayscale is the term designers are accustomed to using in graphic editors”. Here, these commenters presume more users would be familiar with this term over others because of pre-existing tools. These conflicting information all serve to show the importance of understanding the API demographic and their backgrounds to make APIs intuitive for more people.

The author also notes how “rgb(x)/rgba(x,a) cannot be polyfilled in that way, as that would overwrite the native rgb()/rgba() functions” as an argument against that choice [Verou, 2014]. Bloch mentioned that “APIs must coexist peacefully with the platform, so do what is customary” [Bloch, 2006], and this issue is an example of negotiating those customs by paying attention to how new changes may affect existing systems using that API.

Finally, this is a post for help - telling us that API design should be a collaborative process.

---

**Question**

The Pavlus article mentions the researchers' comments that people preferred
"natural-language replacements for some of the more abstruse syntax". In other
words, people found it easier to work with code that looks more like a human language (e.g.,
English). Consider the following quote by William R. Cook, one of the creators
of AppleScript:

> The experiment in designing a language that resembled natural languages (English
> and Japanese) was not successful. It was assumed that scripts should be
> presented in “natural language” so that average people could read and write
> them. … In the end the syntactic variations and flexibility did more to confuse
> programmers than to help them out. It is not clear whether it is easier for
> novice users to work with a scripting language that resembles natural language,
> with all its special cases and idiosyncrasies. The main problem is that
> AppleScript only appears to be a natural language: in fact, it is an artificial
> language, like any other programming language. … even small changes to the
> script may introduce subtle syntactic errors that baffle users. It is easy to
> read AppleScript, but quite hard to write it.
> [[Cook 2007, page 1-20]](https://dl.acm.org/citation.cfm?doid=1238844.1238845)

Are these two experiences of natural languages at odds with one another? Would
you choose to include natural language in the design of a DSL? If so, how might
you do so? If not, why not?

**Response**

These two experiences of natural language are not at odds with one another. Natural languages themselves can be confusing. For example, new English learners often have trouble with transitional phrases and [intricacies between synonyms](https://www.scribendi.com/academy/articles/the_10_most_common_esl_mistakes.en.html).

Let us take a closer reading of these sources. The Pavlus article explores the “intuitiveness” and the usability of a language. It suggests that one way to do it is to find natural language replacements for “abstruse syntax”. AppleScript may have taken the replacements a bit too far. By using natural language replacements beyond what is “abstruse”, the language run into ambiguities littered within natural language. 

Both authors allude to the same sentiment: the descriptor “artificial language” is used in the same sense as calling the Java for loops “Klingon”, a fictional language developed from the Star Trek franchise. They are both analogies for the confusion. Only one comes from too many established meanings (Cook) and the other from too much abstraction that no established meaning comes to mind (Pavlus). Put together, the Pavllus and Cook anecdotes support balancing conciseness via notations with natural language replacement for comprehensible reading and writing programs.

I would choose to include natural language in the design of a DSL cautiously. I think a lot of iteration is needed. Personally, I would start by erring more on the side of notations. Using feedback from the DSL’s intended users, comparisons to modern programming language, and related technological contexts, I would identify confusing syntax or phrasings and substitute them for natural language. I would also keep in mind potential connotations these substitutions may have that go against what they represent in the DSL.

---
