---
title: "Typography - Long title (Lid est laborum et dolorum fuga. Et harum quidem rerum!"
date: 2021-12-03T12:13:38+05:30
draft: true
---
# Heading 1

Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod amets untra dolor amet sad. Sed ut perspser iciatis unde omnis iste natus error sit voluptatem accusantium doloremque laste. Dolores sadips ipsums sits.

## Heading 2

Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod amets untra dolor amet sad. Sed ut perspser iciatis unde omnis iste natus error sit voluptatem accusantium doloremque laste. Dolores sadips ipsums sits.

### Heading 3

Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod amets untra dolor amet sad. Sed ut perspser iciatis unde omnis iste natus error sit voluptatem accusantium doloremque laste. Dolores sadips ipsums sits.

#### Heading 4

Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod amets untra dolor amet sad. Sed ut perspser iciatis unde omnis iste natus error sit voluptatem accusantium doloremque laste. Dolores sadips ipsums sits.

##### Heading 5

Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod amets untra dolor amet sad. Sed ut perspser iciatis unde omnis iste natus error sit voluptatem accusantium doloremque laste. Dolores sadips ipsums sits.

###### Heading 6

Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod amets untra dolor amet sad. Sed ut perspser iciatis unde omnis iste natus error sit voluptatem accusantium doloremque laste. Dolores sadips ipsums sits.

## Typography
### Image with caption
{{< figure src="/abstract-projection-1.png" caption="An abstract video still projected onto my kitchen cabinets." >}}

### Just simple text
Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod

### Blockquote

> Lid est laborum et dolorum fuga. Et harum quidem rerum facilis est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit quo minus id quod amets untra dolor amet sad. Sed ut perspser iciatis unde omnis iste natus error sit voluptatem accusantium doloremque laste. Dolores sadips ipsums sits.
> – Bruce Schneier

### Code - inline
Lid est laborum et dolorum fuga, This is [an example](http://example.com/ "Title") inline link. Et harum quidem rerum facilis, **This is bold** and *emphasis* cumque nihilse impedit quo minus id quod amets untra dolor amet sad. While this is `code block()` and following is a `pre` tag

	print 'this is pre tag'

### Code - block
Following is the syntax highlighted code block

```go
func getCookie(name string, r interface{}) (*http.Cookie, error) {
	rd := r.(*http.Request)
	cookie, err := rd.Cookie(name)
	if err != nil {
		return nil, err
	}
	return cookie, nil
}

func setCookie(cookie *http.Cookie, w interface{}) error {
	// Get write interface registered using `Acquire` method in handlers.
	wr := w.(http.ResponseWriter)
	http.SetCookie(wr, cookie)
	return nil
}
```

### Code - block with line num
Line number with highlighter lines
{{< highlight java "linenos=table,hl_lines=8 13-14,linenostart=1" >}}
cvs diff -N -u -l "/dev-ops-tools/src/com/ssp/support/commons/connection/ConnectionController.java"
    Index: src/com/ssp/support/commons/connection/ConnectionController.java
    ===================================================================
    RCS file: /cvs/dev-ops-tools/src/com/ssp/support/commons/connection/ConnectionController.java,v
    retrieving revision 1.5
    diff -u -r1.5 ConnectionController.java
    --- src/com/ssp/support/commons/connection/ConnectionController.java	8 Mar 2016 16:08:05 -0000	1.5
    +++ src/com/ssp/support/commons/connection/ConnectionController.java	22 Sep 2020 03:32:09 -0000
    @@ -61,6 +61,7 @@
             }
           }
         } else {
    +      LOG.info("ROB WAS HEREZ");
           LOG.info("connections.xml file found");
         }
         return pathname;
{{< / highlight >}}

This is blockquote, Will make it *better now*

> 'I want to do with you what spring does with the cherry trees.' <cite>cited ~Pablo Neruda</cite>*


> Et harum quidem *rerum facilis* est et expeditasi distinctio. Nam libero tempore, cum soluta nobis est eligendi optio cumque nihilse impedit

Unordered list

*   Red
*   Green
*   Blue

Ordered list

1.	Red
2.  Green
3.  Blue

## Table
To add a table, use three or more hyphens (---) to create each column’s header, and use pipes (|) to separate each column. You can optionally add pipes on either end of the table.

### Table with simple data
```md
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

You can align text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both side of the hyphens within the header row.
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |

### Table with lot data
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

End of TEST!