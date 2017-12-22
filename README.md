# regex-reverse-acronym-finder

<h2> Regex that  finds potential acronym meanings.</h2>

I had a sloppy document with acronyms that aren't in the document glossary or explicitly defined elsewhere.

I created this regex to try to help. It basixcally detects possible candidates for these such acronyms without manually looking for strings of words that this might represent.

For example one such acronym was END. I copied the text from the document into Notepad++ 6.9.2 and did a Regex find and replace (Ctrl+H, check the Regular expression radio button) and fed each letter (it's lower and uppercase character) into the relevant square brackets.

\b[<b>eE</b>]\w+[\s-?][<b>nN</b>]\w+[\s-?][<b>dD</b>]\w+

matches

ethyl nitrate Dihydrate</br>
ethyl-Nitrate dihydrate</br>
Ethyl Nitrate-dihydrate</br>
Ethyl-Nitrate-dihydrate</br>
