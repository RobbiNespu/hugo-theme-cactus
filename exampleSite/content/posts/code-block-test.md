---
title: Code Block Test
date: 2021-06-27 09:00:00
tags:
    - test
    - tag1
    - tag2
    - tag3
    - tag4
    - tag5
    - tag6
    - tag7
    - tag8
    - tag9
    - tag10
categories:
    - tech
keywords:
    - markdown
    - code block
---

> KUALA LUMPUR, Dec 3 — Malaysia’s new Covid-19 infections dropped to 4,896 today as compared to 5,551 cases yesterday. Health director-general Tan Sri Dr Noor Hisham Abdullah said this bring the cumulative number of Covid-19 cases nationwide now to 2,654,474.

|    | date       |   time_over_max |   time_under_min |   time_normal |
|---:|:-----------|---------------------------:|----------------------------:|-------------------------:|
|  0 | 2021-08-16 |0%    |                        1.15% |                    98.85% |
|  1 | 2021-08-17 |0.79% |                       13.34% |                    85.87% |
|  2 | 2021-08-18 |4.9%  |                        4.44% |                    90.66% |
|  3 | 2021-08-19 |2.43% |                        0%    |                    97.57% |
|  4 | 2021-08-20 |0%    |                        0%    |                   100%    |
|  5 | 2021-08-22 |1.16% |                        0%    |                    98.84% |
|  6 | 2021-08-23 |0%    |                        3.59% |                    96.41% |
|  7 | 2021-08-24 |0%    |                       43.38% |                    56.62% |
|  8 | 2021-08-25 |0%    |                       62.44% |                    37.56% |


`String`

Using indents:

    text
    text
    text


Fenced code block:

```
text
text
<tag>
```

Fenced code block with language (lineNumbersInTable = false):

```Java
// JavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJavaJava
public final class String
    implements java.io.Serializable, Comparable<String>, CharSequence
{
    /** The value is used for character storage. */
    private final char value[];

    /** The offset is the first index of the storage that is used. */
    private final int offset;

    /** The count is the number of characters in the String. */
    private final int count;

    /** Cache the hash code for the string */
    private int hash; // Default to 0

    // ...

    // Package private constructor which shares value array for speed.
    String(int offset, int count, char value[]) {
        this.value = value;
        this.offset = offset;
        this.count = count;
    }

    // ...

    /**
     * Returns a new string that is a substring of this string. The
     * substring begins at the specified <code>beginIndex</code> and
     * extends to the character at index <code>endIndex - 1</code>.
     * Thus the length of the substring is <code>endIndex-beginIndex</code>.
     * <p>
     * Examples:
     * <blockquote><pre>
     * "hamburger".substring(4, 8) returns "urge"
     * "smiles".substring(1, 5) returns "mile"
     * </pre></blockquote>
     *
     * @param      beginIndex   the beginning index, inclusive.
     * @param      endIndex     the ending index, exclusive.
     * @return     the specified substring.
     * @exception  IndexOutOfBoundsException  if the
     *             <code>beginIndex</code> is negative, or
     *             <code>endIndex</code> is larger than the length of
     *             this <code>String</code> object, or
     *             <code>beginIndex</code> is larger than
     *             <code>endIndex</code>.
     */
    public String substring(int beginIndex, int endIndex) {
        if (beginIndex < 0) {
            throw new StringIndexOutOfBoundsException(beginIndex);
        }
        if (endIndex > count) {
            throw new StringIndexOutOfBoundsException(endIndex);
        }
        if (beginIndex > endIndex) {
            throw new StringIndexOutOfBoundsException(endIndex - beginIndex);
        }
        return ((beginIndex == 0) && (endIndex == count)) ? this :
            new String(offset + beginIndex, endIndex - beginIndex, value);
    }

    // ...
}
```

Using hugo's `highlight` [shortcode]([highlight](https://gohugo.io/content-management/syntax-highlighting/#highlight-shortcode)) (lineNumbersInTable = true):

{{< highlight typescript "linenos=table, hl_lines=8 18-21" >}}
// TypeScript
type OptionalUser = {
    [K in keyof User]?: User[K]
}

// ! we can remove optional constraint
type RequiredUser = {
    [K in keyof OptionalUser]-?: User[K]
}

type NullableUser = {
    [K in keyof User]: User[K] | null
}
type ReadonlyUser = {
    readonly [K in keyof User]: User[K]
}

// ! we can remove readonly constraint
type ModifiableUser = {
    -readonly [K in keyof User]: User[K]
}
{{< /highlight >}}

Without line number

{{< highlight javascript "linenos=false" >}}
(() => {

  function createCopyButton(codeNode) {
    const copyBtn = document.createElement('button')
    copyBtn.className = 'code-copy-btn'
    copyBtn.type = 'button'
    copyBtn.innerText = 'copy'
    copyBtn.parentElement = codeNode.parentElement

    let resetTimer
    copyBtn.addEventListener('click', () => {
      navigator.clipboard.writeText(codeNode.innerText).then(() => {
        copyBtn.innerText = 'copied!'
      }).then(() => {
        clearTimeout(resetTimer)
        resetTimer = setTimeout(() => {
          copyBtn.innerText = 'copy'
        }, 1000)
      })
    })

    return copyBtn
  }

  document.querySelectorAll('pre > code').forEach((codeNode) => {
    const copyBtn = createCopyButton(codeNode);
    codeNode.parentNode.insertBefore(copyBtn, codeNode)
  })

})()
{{< / highlight >}}
