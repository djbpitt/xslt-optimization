* Replace sort with max
* Compare integers instead of strings (row and column labels)
* Append to an array instead of string-join; in general, don’t append to a string
* Store path in something smaller than characters (byte is as small as it gets)
* Store path (d, l, u) as numbers, rather than letters
* Is computing faster than reading and writing?
* Number of cores (Amdahl's Law)
* Tuples (tuple types to support optimizing for the compiler, which knows the length)
* Memo functions (`@saxon:memo-function` in PE and EE)
* Is schema-aware processing with typed attributes faster than non-schema-aware processing with explicit casting upon use?

Kay: comparing integers is faster then comparing strings:
<`https://archive.xmlprague.cz/2015/files/xmlprague-2015-proceedings.pdf>

Comments on XML Prague paper:

1. Michael Kay: Modifying arrays or maps might be more efficient than modifying nodes
2. Accumulators (Michael Kay was skeptical)


Ran some intitial tests with current setup 2020-03-06 basically just to test Saxon-EE was working. Threads seems to slow things down, but if we do longer runs wit a limited number 2-4 it might be beneficial for the baselining.
