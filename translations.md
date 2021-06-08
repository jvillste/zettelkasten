# How to implement translated strings?

* Translations are referred to by clojure symbols
  * Jumping to translation definition is done by jumping to the symbol definition
  * Finding unused translations is done by finding unreferred symbols
* Finding out dated and missing translations should be automatic
  * Translations refer to the source language version by a hash
	* Translations are thus automatically invalidated when the source text is changed
* Generating excell sheets for translators and reading them back should be automated
  * When the srouce text changes after translation, the excell sheets should contain the old and new source text and the old translation.
    * The results of each translation batch should be saved to the version control for this purpose. This can be done as edn rather than code that defines symbols.
* An html page could be generated that contains a user interface for translators
* Requirements
  * Editing translations directly from the screen or at least finding the key by clicking the screen
	* Angular leaves the key to the dom element and it can be inspected by browser's developer tools
  * Finding unused translations
	* Finding unreferenced symbols should be supported by ides
  * Renaming transaltion keys and references to them
	* Renaming clojure symbols should be supported by ides

