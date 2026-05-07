---
description: Use regular expressions for powerful searching and rule-based coding.
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/V4pJG7Rv7yabqyiVt2OZ/documentation/ascribe-coder/codebooks/regular-expressions
---

# Regular Expressions

A _regular expression_ is a pattern used to match text. Each code in a codebook can have an associated regular expression. You can enter expressions in the Code Properties dialog from Ascribe Coder or Phrase Analyzer II.

### Code with Expressions <a href="#minitocbookmark2" id="minitocbookmark2"></a>

When a verbatim is displayed to a coder in the Ascribe Coder, the system compares it to each regular expression defined in the codebook for the question. If a match is found, the matched text is underlined and highlighted. The coder can hover over the highlighted text to see which code will be selected. If the coder clicks the underlined text, the code that matched the text is selected and placed in the selected codes pane.

### Simple Regular Expressions <a href="#minitocbookmark3" id="minitocbookmark3"></a>

Use lower case letters in regular expressions. Ascribe views lower case and upper case letters the same.

Letters and digits in the regular expression match the corresponding text in the verbatim response. For example:

| Verbatim response | Regular expression | Result                                                                                |
| ----------------- | ------------------ | ------------------------------------------------------------------------------------- |
| I love cats       | love               | I <mark style="color:$success;">love</mark> cats                                      |
| I love dogs       | dog                | I love <mark style="color:$success;">dog</mark>s                                      |
| I LOVE DOGS       | o                  | I L<mark style="color:$success;">O</mark>VE D<mark style="color:$success;">O</mark>GS |

Notice that these regular expressions simply match the same sequence of characters in the verbatim text. Upper and lower case letters are treated the same.

### Match Words <a href="#minitocbookmark4" id="minitocbookmark4"></a>

In many cases, you will want to match whole words. Use angle brackets around characters to mean "match this word". For example:

| Verbatim response           | Regular expression | Result                                                                                                |
| --------------------------- | ------------------ | ----------------------------------------------------------------------------------------------------- |
| The cat likes Catawba melon | cat                | The <mark style="color:$success;">cat</mark> likes <mark style="color:$success;">Cat</mark>awba melon |
| The cat likes Catawba melon | \<cat>             | The <mark style="color:$success;">cat</mark> likes Catawba melon                                      |

Notice that the first regular expression matches the "cat" in Catawba, which is probably not what you want. When we put the "cat" in angle brackets, we match only that exact word.

Often you will want to match words that begin with a certain sequence of characters. Use two angle brackets at the end of the word to mean "match words that begin with these characters". For example:

<table><thead><tr><th>Verbatim response</th><th width="240">Regular expression</th><th>Result</th></tr></thead><tbody><tr><td>I like Cadillacs and Catalinas</td><td>&#x3C;cad>></td><td>I like <mark style="color:$success;">Cadillacs</mark> and Catalinas</td></tr><tr><td>I like Cadillacs and Catalinas</td><td>&#x3C; ca>></td><td>I like <mark style="color:$success;">Cadillacs</mark> and <mark style="color:$success;">Catalinas</mark></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

You can also match words that end with a certain sequence of characters. Use two angle brackets at the start of the word to mean "match words that end with these characters." For example:

| Verbatim response                        | Regular expression | Result                                                                                                                                               |
| ---------------------------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| I use USMail, email, and SnailMail       | <\<mail>           | I use <mark style="color:$success;">USMail</mark>, <mark style="color:$success;">email</mark>, and <mark style="color:$success;">SnailMail</mark>    |
| I use US Mail, e-mail, and Snail Mail    | <\<mail>           | I use US <mark style="color:$success;">Mail</mark>, e-<mark style="color:$success;">mail</mark>, and Snail <mark style="color:$success;">Mail</mark> |
| I use US Mail, e-mailing, and Snail Mail | <\<mail>           | I use US <mark style="color:$success;">Mail</mark>, e-mailing, and Snail <mark style="color:$success;">Mail</mark>                                   |

Notice in these examples that the definition of a word for matching is a contiguous sequence of characters. Word matching stops at punctuation marks and spaces.

Finally, you can use two angle brackets at the start and end of the word to mean "match words that contain these characters." For example:

| Verbatim response                                 | Regular expression | Result                                                                                                                                                                                                |
| ------------------------------------------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| I send mail by USMailing, emailing, and SnailMail | <\<mail>>          | I send <mark style="color:$success;">mail</mark> by <mark style="color:$success;">USMailing</mark>, <mark style="color:$success;">emailing</mark>, and <mark style="color:$success;">SnailMail</mark> |

It is critical that the opening angle brackets are matched with closing angle brackets. Any of these examples would cause the regular expression matching not to work:

\>cat<

\<cat

cat>>

### Match Phrases <a href="#minitocbookmark5" id="minitocbookmark5"></a>

You can match exact phrases when you place the phrase inside angle brackets:

| Verbatim response | Regular expression | Result                                           |
| ----------------- | ------------------ | ------------------------------------------------ |
| I love cats       | \<love cat>>       | I <mark style="color:$success;">love cats</mark> |

You can also match phrases that are bound by certain words. Use three dots in the regular expression to mean "skip up to thirty characters within this phrase."

The three dots match any sequence of up to 30 characters that do not contain the following characters: .,;:?!

| Verbatim response           | Regular expression | Result                                                         |
| --------------------------- | ------------------ | -------------------------------------------------------------- |
| I love cats                 | \<love…cat>>       | I <mark style="color:$success;">love cats</mark>               |
| I love white cats           | \<love…cat>>       | I <mark style="color:$success;">love white cats</mark>         |
| I love dogs and hate cats   | \<love…cat>>       | I <mark style="color:$success;">love dogs and hate cats</mark> |
| I love dogs, cats, and mice | \<love…cat>>       | I love dogs, cats, and mice                                    |

Notice that the third and fourth examples do not give the desired result. The third one matched, but the phrase is not the intended phrase. The fourth did not match because of the comma between 'love' and 'cats'.

### Match Negative Phrases <a href="#minitocbookmark6" id="minitocbookmark6"></a>

You can use a tilde character '\~' directly in front of a < or << to match the word 'not' in the preceding portion of the phrase. It is another way of writing \<not>…

For example:

| Verbatim response | Regular expression | Result      |
| ----------------- | ------------------ | ----------- |
| Verbatim Response | Regular Expression | Result      |
| I love cats       | \~\<love…cat>>     | I love cats |

### Match Commonly Misspelled Words <a href="#minitocbookmark7" id="minitocbookmark7"></a>

A single dot character matches any character in that location. Use this to handle commonly misspelled words. For example:

| Verbatim response       | Regular expression | Result                                                       |
| ----------------------- | ------------------ | ------------------------------------------------------------ |
| Cadillacs and Catalinas | \<cad.l>>          | <mark style="color:$success;">Cadillacs</mark> and Catalinas |
| Cadallacs and Catalinas | \<cad.l>>          | <mark style="color:$success;">Cadallacs</mark> and Catalinas |

The use of brackets with the single dot can also help with misspelled words. The characters .{1,2} tells the expression tester to look for one or two missing characters between the letters before and after the brackets. For example:

| Verbatim response     | Regular expression | Result                                                     |
| --------------------- | ------------------ | ---------------------------------------------------------- |
| Niether this nor that | \<n.{1,2}ther>     | <mark style="color:$success;">Neither</mark> this nor that |
| Nither this nor that  | \<n.{1,2}ther>     | <mark style="color:$success;">Nither</mark> this nor that  |
| Nether this nor that  | \<n.{1,2}ther>     | <mark style="color:$success;">Nether</mark> this nor that  |

### Match Multiple Cases <a href="#minitocbookmark8" id="minitocbookmark8"></a>

You can join regular expressions together with a vertical bar. The vertical bar means "match either of these expressions." For example:

| Verbatim response | Regular expression         | Result                                           |
| ----------------- | -------------------------- | ------------------------------------------------ |
| I love cats       | \<love…cat>>\|\<love…dog>> | I <mark style="color:$success;">love cats</mark> |
| I love dogs       | \<love…cat>>\|\<love…dog>> | I <mark style="color:$success;">love dogs</mark> |

You should only use the vertical bar to separate words surrounded by angle brackets, unless you are using the advanced features described in the next section.

### The "And" Operator: && <a href="#minitocbookmark9" id="minitocbookmark9"></a>

The "And" operator of && can be used to search for two distinct regular expression matches in a single response.

For example, <\<dixie>>&&<\<solo>> would return this response: 'Solo cups and Dixie plates'. It would not return responses that only say 'Dixie' or 'Solo'.

The "And" operator can be used in conjunction with the "OR" operator (the vertical bar).

For example, <\<dixie>>&&<\<solo>>|<\<store>> would return this response, 'Solo cups and Dixie plates', or this response, 'Dixie store brand'. It would not return responses that only say 'Dixie' or 'Solo' or 'store'.

### The "And Not" Operator: &\~ <a href="#minitocbookmark10" id="minitocbookmark10"></a>

The "And Not" operator of &\~ can be used to search for response that contain one regular expression pattern and that do not contain a secondary pattern.

For example, <\<red>>&&<\<white>>&\~blue would return this response, 'The car has white stripes with a red interior.' It would not return this response, 'Hail to the red, white and blue'.

The "And Not" operator can be used in conjunction with the "OR" operator (the vertical bar).

For example, <\<red>>&\~<\<blue>>|<\<white>> would return this response, 'The car has red stripes'. It would not return this response, 'The car has white stripes with a red interior' or 'The car has red stripes with a blue interior'.

### The "Plain Text Matching" Prefix: \* <a href="#minitocbookmark11" id="minitocbookmark11"></a>

The "Plain Text Matching" operator of \* allow users to match an entire word, with or without specific punctuation (such as question marks or exclamation points.)

For example, \*dixie? would return this response, 'I don't know, Dixie?' It would not return this response, 'Maybe Dixie'.

This prefix will not work with the "Or", the "And", and the "And Not" operators.

### The "Standard Regular Expression Matching" Prefix: > <a href="#minitocbookmark12" id="minitocbookmark12"></a>

This prefix allows users to search by standard regular expression statements.

For example, >^dix would return any response that contains a string starting with 'dix', such as 'dixie plates' or 'dixey'. It would not return responses where 'dix' occurs later in the response, such as 'solo cups and dixie plates'.

Another example is >cups$, which will return any response that contains a string ending with 'cups', such as 'solo cups'.

This prefix will not work with the Ascribe regular expression operators.

### Advanced Use of Regular Expressions <a href="#minitocbookmark13" id="minitocbookmark13"></a>

Simple regular expressions are sufficient for most uses. However, this section covers the additional applications you can use with regular expressions. Use them only if you have a clear understanding of how they work.

You can use the special characters described in the table below to build more complex regular expressions.

<table><thead><tr><th width="194.6666259765625" valign="top">Character</th><th valign="top">Description</th></tr></thead><tbody><tr><td valign="top"><strong>\</strong></td><td valign="top">Marks the next character as either a special character or a literal. For example, "n" matches the character "n". "\n" matches a newline character. The sequence "\\" matches "\" and "\(" matches "(".</td></tr><tr><td valign="top"><strong>^</strong></td><td valign="top">Matches the beginning of input.</td></tr><tr><td valign="top"><strong>$</strong></td><td valign="top">Matches the end of input.</td></tr><tr><td valign="top"><strong>*</strong></td><td valign="top">Matches the preceding character zero or more times. For example, "zo*" matches either "z" or "zoo".</td></tr><tr><td valign="top"><strong>+</strong></td><td valign="top">Matches the preceding character one or more times. For example, "zo+" matches "zoo" but not "z".</td></tr><tr><td valign="top"><strong>?</strong></td><td valign="top">Matches the preceding character zero or one time. For example, "a?ve?" matches the "ve" in "never".</td></tr><tr><td valign="top"><strong>.</strong></td><td valign="top">Matches any single character except a newline character.</td></tr><tr><td valign="top"><strong>(</strong><em>pattern</em><strong>)</strong></td><td valign="top">Matches pattern and remembers the match. The matched substring can be retrieved from the resulting <strong>Matches</strong> collection, using Item <strong>[0]...[n]</strong>. To match parentheses characters ( ), use "\(" or "\)".</td></tr><tr><td valign="top"><em>x</em><strong>|</strong><em>y</em></td><td valign="top">Matches either <em>x</em> or <em>y</em>. For example, "z|food" matches "z" or "food". "(z|f)oo" matches "zoo" or "food".</td></tr><tr><td valign="top"><strong>{</strong><em>n</em><strong>}</strong></td><td valign="top"><em>n</em> is a nonnegative integer. Matches exactly <em>n</em> times. For example, "o{2}" does not match the "o" in "Bob," but matches the first two o's in "foooood".</td></tr><tr><td valign="top"><strong>{</strong><em>n</em><strong>,}</strong></td><td valign="top"><em>n</em> is a nonnegative integer. Matches at least <em>n</em> times. For example, "o{2,}" does not match the "o" in "Bob" and matches all the o's in "foooood." "o{1,}" is equivalent to "o+". "o{0,}" is equivalent to "o*".</td></tr><tr><td valign="top"><strong>{</strong><em>n</em><strong>,</strong><em>m</em><strong>}</strong></td><td valign="top"><em>m</em> and <em>n</em> are nonnegative integers. Matches at least <em>n</em> and at most <em>m</em> times. For example, "o{1,3}" matches the first three o's in "fooooood." "o{0,1}" is equivalent to "o?".</td></tr><tr><td valign="top"><strong>[</strong><em>xyz</em><strong>]</strong></td><td valign="top">A character set. Matches any one of the enclosed characters. For example, "[abc]" matches the "a" in "plain".</td></tr><tr><td valign="top"><strong>[^</strong><em>xyz</em><strong>]</strong></td><td valign="top">A negative character set. Matches any character not enclosed. For example, "[^abc]" matches the "p" in "plain".</td></tr><tr><td valign="top"><strong>[</strong><em>a</em><strong>-</strong><em>z</em><strong>]</strong></td><td valign="top">A range of characters. Matches any character in the specified range. For example, "[a-z]" matches any lowercase alphabetic character in the range "a" through "z".</td></tr><tr><td valign="top"><strong>[^</strong><em>m</em><strong>-</strong><em>z</em><strong>]</strong></td><td valign="top">A negative range characters. Matches any character not in the specified range. For example, "[m-z]" matches any character not in the range "m" through "z".</td></tr><tr><td valign="top"><strong>\b</strong></td><td valign="top">Matches a word boundary, that is, the position between a word and a space. For example, "er\b" matches the "er" in "never" but not the "er" in "verb".</td></tr><tr><td valign="top"><strong>\B</strong></td><td valign="top">Matches a nonword boundary. "ea*r\B" matches the "ear" in "never early".</td></tr><tr><td valign="top"><strong>\d</strong></td><td valign="top">Matches a digit character. Equivalent to [0-9].</td></tr><tr><td valign="top"><strong>\D</strong></td><td valign="top">Matches a nondigit character. Equivalent to [^0-9].</td></tr><tr><td valign="top"><strong>\f</strong></td><td valign="top">Matches a form-feed character.</td></tr><tr><td valign="top"><strong>\n</strong></td><td valign="top">Matches a newline character.</td></tr><tr><td valign="top"><strong>\r</strong></td><td valign="top">Matches a carriage return character.</td></tr><tr><td valign="top"><strong>\s</strong></td><td valign="top">Matches any white space including space, tab, form-feed, etc. Equivalent to "[ \f\n\r\t\v]".</td></tr><tr><td valign="top"><strong>\S</strong></td><td valign="top">Matches any nonwhite space character. Equivalent to "[^ \f\n\r\t\v]".</td></tr><tr><td valign="top"><strong>\t</strong></td><td valign="top">Matches a tab character.</td></tr><tr><td valign="top"><strong>\v</strong></td><td valign="top">Matches a vertical tab character.</td></tr><tr><td valign="top"><strong>\w</strong></td><td valign="top">Matches any word character including underscore. Equivalent to "[A-Za-z0-9_]".</td></tr><tr><td valign="top"><strong>\W</strong></td><td valign="top">Matches any nonword character. Equivalent to "[^A-Za-z0-9_]".</td></tr><tr><td valign="top"><strong>\</strong><em>num</em></td><td valign="top">Matches <em>num</em>, where <em>num</em> is a positive integer. A reference back to remembered matches. For example, "(.)\1" matches two consecutive identical characters.</td></tr><tr><td valign="top"><strong>\</strong><em>n</em></td><td valign="top">Matches <em>n</em>, where <em>n</em> is an octal escape value. Octal escape values must be 1, 2, or 3 digits long. For example, "\11" and "\011" both match a tab character. "\0011" is the equivalent of "\001" &#x26; "1". Octal escape values must not exceed 256. If they do, only the first two digits comprise the expression. Allows ASCII codes to be used in regular expressions.</td></tr><tr><td valign="top"><strong>\x</strong><em>n</em></td><td valign="top">Matches <em>n</em>, where <em>n</em> is a hexadecimal escape value. Hexadecimal escape values must be exactly two digits long. For example, "\x41" matches "A". "\x041" is equivalent to "\x04" &#x26; "1". Allows ASCII codes to be used in regular expressions.</td></tr></tbody></table>

### Check Expressions for a Specific Codebook <a href="#minitocbookmark14" id="minitocbookmark14"></a>

Use Ascribe Coder to see all of the expressions used in a codebook. On the Codebook toolbar, click the Tools icon, and a dialog displays. The Expression List is one of the tabs in the dialog.

### Commonly Used Regular Expressions

<table><thead><tr><th valign="top">Symbol</th><th valign="top">Meaning</th><th valign="top">Example</th><th valign="top">Result</th></tr></thead><tbody><tr><td valign="top">No symbols</td><td valign="top">Match corresponding text no matter where it appears in the word</td><td valign="top">the</td><td valign="top">matches the and then and anthem and bathe</td></tr><tr><td valign="top">&#x3C; ></td><td valign="top">Exact match of text</td><td valign="top">&#x3C;the></td><td valign="top">matches the but not then or anthem or bathe</td></tr><tr><td valign="top">&#x3C; >></td><td valign="top">Match words beginning with text</td><td valign="top">&#x3C;the>></td><td valign="top">matches the and then but not anthem or bathe</td></tr><tr><td valign="top">&#x3C;&#x3C; ></td><td valign="top">Match words ending with text</td><td valign="top">&#x3C;&#x3C;the></td><td valign="top">matches the and bathe but not then or anthem</td></tr><tr><td valign="top">|</td><td valign="top">Match either text string</td><td valign="top">red|blue</td><td valign="top">matches “red, white, and blue” and also matches “red river” and also matches “blue sky”</td></tr><tr><td valign="top">…</td><td valign="top">Match strings within 30 char</td><td valign="top">red…blue|blue…red</td><td valign="top">matches “red, white, and blue”</td></tr><tr><td valign="top">&#x26;&#x26;</td><td valign="top">Match both strings</td><td valign="top">red&#x26;&#x26;blue</td><td valign="top">matches “red, white, and blue”; matches “blue or red” but not “red river” or “blue sky”</td></tr><tr><td valign="top">&#x26;~</td><td valign="top">Exclude string; matches the first string only if the second string is not present</td><td valign="top">red&#x26;~blue</td><td valign="top">not match “red, white, and blue”; not match “blue or red” but matches “red river” or “red and white stripes”</td></tr><tr><td valign="top">^$</td><td valign="top">Match entire verbatim</td><td valign="top">^nothing$</td><td valign="top">Matches “nothing” but not “nothing!”</td></tr></tbody></table>
