[Travis Oliphant: NumPy, SciPy, Anaconda, Python & Scientific Programming | Lex Fridman Podcast #224](https://youtu.be/gFEE3w7F0ww)

Travis Oliphant is the author of NumPy and SciPy -Python libraries and the founder of Anaconda.

He used to work with MRI images in MEOCLINIC and had used Matlab for the task. Matlab was OK technically, but he did not like the fact that he would have to publish code that needed commercial software to be run. When he switched to Python he realized that Python was missing some tools that he had used in Matlab like integration and function optimization. He decided to implement them in SciPy.

Travis initially liked Python because it had n dimensional arrays and imaginary numbers. He also knew C and so he could extend python. He liked that he could understand his own code even years later, which was not the case for example with Perl.

He likes Fortran because it also has good suport for arrays and imaginary numbers, but would not like to write applications in it. He just likes to use fortran libraries as libraries.

A programmer might think that imaginary numbers are just two floats, but if they are not built into the language then libraries can not interoperate if they use different implementation for them.

He was inspired by Linux Torwalds and also likes science because it's about sharing knowledge. That's why he started to share his code early on. At first it was just sharing the source code and it was really hard to install and use it. Later he started to share binaries so that users would not have to figure out how to compile them.

Later he realized that researchers in the scientific community often envy each other and do not voluntarily work together as opposed to the open source software community.

# Related thoughts
It would be beneficial to be more easily able to write functions in one language and call them from another language. The functions could share value types described as Dabric value types. See [[programming language agnostic functions]]. Also [[function level code depencencies]] could be useful approach to code sharing.