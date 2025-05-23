# Quotecurl: Pretty Quotes and Dashes

*Quotecurl* is a Javascript “smart quotes” module. It turns boring (but easily
typed) text, from a *straight quote* hellscape, into a sparkly✨ Unicode with
fancy *curly quotes*.—It also fancifies some other common seqences, converting
each of them into the appropriate *fancy* Unicode character.

<toc heading=Contents class=toc>

Do this:

```
import { quotecurl } from './quotecurl.mjs'
…
const prettyText = quotecurl(uglyText)
```


Characters Handled
==================
The following characters are handled:

| Source | Becomes                        | Fancy                |
|:------:|--------------------------------|:--------------------:|
| `'`    | curly single quotes/apostrophe | **‘**…**’** or **’** |
| `"`    | curly double quotes            | **“**…**”**          |
| `--`   | en-dash                        | **–**                |
| `---`  | em-dash                        | **—**                |
| `...`  | ellipsis                       | **…**                |

The conversion of *straight apostrophes* (`'`) into *curly single quotes* (and
*apostrophes*) is slightly more involved than for the other characters. Context
is used to try to figure out what to convert an individual straight quote into.

For quoted section to be recognized as such, the first quote must be preceded
by space, and the last quote must be followed by space (in both other
punctuation may occur between the quote symbol and the space, but no
alphanumeric characters).


Feet & Inches, Minutes & Seconds
--------------------------------
Quotecurl does not currenly handle `'` and `"` as symbols for *feet and inches*
(5′8″), or *minutes and seconds* (as used for both angles, 91°5′30″, and
durations, 4′33″). However, this will hopefully change in the future.

For now, the best workaround is to write `′` *prime* and `″` *double prime,*
either using a literal Unicode character, or one of the corresponding HTML
entities.

| Symbol           | HTML Entities       | Used for         |
|------------------|---------------------|------------------|
| `′` prime        | `&#8242;` `&prime;` | feet & minutes   |
| `″` double prime | `&#8243;` `&Prime;` | inches & seconds |


Author
======
Copyright 2025 by zrajm, Uppsala, Scandinavia.


License
=======
GNU General Public License, Version 2.


Test Cases
==========
The test cases show here are intended as specs for Quotecurl, though they will
evolve as Quotecurl does so.

[Go to Test Case Page][Test Cases] (If you don’t already see the tests below.)

[Test Cases]: https://zrajm.org/quotecurl/#test-cases

<!--[eof]-->
