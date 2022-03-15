## Abbreviations and acronyms 
* If you're using an acronym or abbreviation that isn't well-known, spell out the full acronym the first time it appears and provide its shortened form in parentheses. You can then use the shortened form throughout the rest of the document.
    * EXAMPLE: The HUMAN Dashboard supports single sign-on (SSO). To configure SSO for your organization...

* Don't abbreviate HUMAN's product names in public-facing documentation.
    * NO: BGforA protects your website or application from bots.
    * YES: BotGuard for Applications protects your website or application from bots.

* Don't use acronyms as verbs.
    * NO: CNAME the domain.
    * YES: Add the domain to your CNAME records.

* It's okay to use Latin abbreviations inside parentheses (e.g., like this), but not in the body of a sentence.
    * NO: The beach is home to fish, crabs, sharks, etc.
    * YES: The beach is home to fish, crabs, and so on.
    * ALSO YES: Many sea creatures (fish, crabs, sharks, etc.) live at the beach.
    * ALSO ALSO YES: Many sea creatures (e.g., the loggerhead turtle) are endangered. 

* Don't confuse "i.e." (*id est*, that is to say) and "e.g." (*exempli gratia*, for the sake of example). When in doubt, spell it out—use the English phrase instead!

## Active and passive voice

* Try to use the active voice (which focuses on the "do-er" of an action) whenever possible. 
    * NO: The data must be updated.
    (Focuses on the data itself, not the subject of the sentence—who needs to update the data? The user? The program itself?)
    * YES: You must update your data before continuing.
    (The subject is *you*—the reader knows who must perform the action.)
    * ALSO YES: Update your data.
    (Imperative verbs are active and speak directly to the reader, which is useful for procedural instructions.)

* However, there may be times when the passive voice is preferable, including:
    * To focus on the outcome or recipient of action rather than who's performing it.
    * To avoid blaming the user for an error.
    * When the reader doesn't need to know who performed an action (in the case of an automatic process or backend system).
    * YES: Your password will be reset.
    (Since the reader doesn't need to do anything, the performer of the action is less important than its outcome.)

## Capitalization 

* Use title case for page titles (h1).

* Use sentence case for headers (h2, h3, and so on).

* Be sure to properly capitalize HUMAN and all appropriate product names. For more information, see HUMAN's brand guidelines.

* Don't capitalize the name of glossary entries or index terms unless the term is a proper noun.

* Don't capitalize the names of product features or processes unless the feature or process in question is a proper noun. (Rule of thumb: when in doubt, leave it lowercase.)

## Contractions

* It's okay to use contractions. 

## Pronouns

* It's okay to refer to HUMAN with first-person pronouns like "we" or "our." For best results, try to mention HUMAN by name at least one time before using a pronoun in its place.
    * EXAMPLE: HUMAN does not collect information about your age or date of birth. But if we did, we might throw you a surprise party.

* However, there may be times when it's clearer to refer to HUMAN by name, especially if you need to specify the name of our product or company.
    * EXAMPLE: This feature prevents a conflict between ACME's servers and HUMAN's integration.

* When addressing the reader, it's okay to use second-person language like "you" and "your." Don't use third-person language like "user" or "customer" in public-facing materials written for those very same users and customers—address them directly instead!

* When referring to a person of indeterminate or unknown gender, use the singular "they" rather than gendered pronouns like "she," "he," or any combination thereof (like "(s)he" or "his or her"). 
    * NO: Someone left his or her bike outside.
    * YES: Someone left their bike outside.

* Make sure that each pronoun has a clear antecedent. (In other words, make sure it's obvious what the pronoun is referring to.) One of the easiest ways to avoid ambiguity is to repeat the actual noun instead of using a pronoun in its place.
    * UNCLEAR: The boy hit the bat against the pillar until it broke.
    (What broke—the pole, or the pillar? There's no way to tell from context alone.)
    * CLEAR: The boy hit the bat against the pillar until the pillar broke.
    (It was the pillar!)

* Similarly, when using relative pronouns like "this" or "that," you can reduce ambiguity by also restating the word or concept you're referring to (or replacing the pronoun entirely).
    * UNCLEAR: Send all data to HUMAN's secure servers via carrier pigeon. This prevents hackers from intercepting your data.
    (Which part thwarts hackers: sending data to HUMAN's secure servers, or the fact it was sent via carrier pigeon?)
    * CLEAR: Send all data to HUMAN's secure servers via career pigeon. This pigeon relay prevents hackers from intercepting your data.
    (The pigeons thwart hackers!)

* Use "who" (not "that") in reference to people.
    * NO: Send an email to users that registered early.
    * YES: Send an email to users who registered early.

* The relative pronouns "that" and "which" are not interchangable. Use "that" for restrictive clauses and "which" for nonrestrictive clauses. (A good rule of thumb: nonrestrictive clauses tend to be offset by commas, while restrictive clauses do not.)
    * RESTRICTIVE: The new bass that I bought last week has two humbucker pickups.
    * NONRESTRICTIVE: The new bass, which I bought last week, has two humbucker pickups.
    
## Sentence structure

* It's okay to start a sentence with "and" or "but."

* It's okay to end a sentence with a preposition. However, if rewriting the sentence to avoid using an end preposition would improve the sentence's overall clarity or structure, you should try to rewrite it.

## Spelling

(techdocs, dev)
* Use standard American English spelling conventions.

(marketing)
* Use standard American English spelling conventions. However, here may be exceptions to this rule when addressing audiences who are accustomed to another form of English—for example, if you're writing a sales deck for a European audience, it may be more appropriate to use British English. 

## Tense 
(techdocs, dev)

* Use present tense whenever possible.

* However, it can sometimes be helpful to use the future tense for specific examples of cause and effect.
    * EXAMPLE: If you run multiple reports, each report will generate its own file. 

## Verb forms

* In API reference documentation (and certain types of non-API glossaries), describe each item or method in the present continual tense rather than as an imperative or procedural instruction. In other words, describe what the method does, not what the user must do.
    * WEAK: `end()`: Cancel the current session. 
    (Implied subject is "you"—the user will cancel the session.)
    * STRONG: `end()`: Cancels the current session. 
    (The subject is the method itself—the method cancels the session.)

* However, if you're describing how to use a method rather than a definition of what the method does, it's okay to use standard procedural instructions.
    * EXAMPLE: Call `end()` to cancel the current session.


## Word choice

* When possible, try to use short and simple words instead of long, abstract words.
    * WEAK: This setting facilitates data filtering.
    * STRONG: This setting lets you filter data.

* Avoid filler words like "very." Rather than describing a task as *very important*, you might say that it's *critical*. 

* [Avoid using weak words - implement (sometimes), utilize, "in order to" ("to" generally suffices), leverage, etc]


## Miscellaneous

* Don't use phrasal nouns and phrasal verbs interchangably. Although "login" and "log in" may look similar, they mean different things—a *login* (noun) is the credential you use to *log in* (verb).

* Treat "data" as a singular, uncountable noun.
    * NO: The data support this conclusion.
    * YES: The data supports this conclusion.