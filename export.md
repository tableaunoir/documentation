# Export

Tableaunoir enables you to export your board in PNG and PDF.

## PNG image

Tableaunoir exports your board as a strip.


## PDF document

Tableaunoir exports your board as a PDF document. There are two behaviors depending on your board is a classical one or a presentation with slides:
- The typical case is a classical board. Almost all boards are classical one. For instance, if you never edited the timeline and never added new slide, then your board is *classical*.  Technically, a board is classical when it ss made up of a single "slide".
- A presentation is a board which contains several slides. To make presentations, read [How to make presentations/animations](timeline.md).


### Classical board

Tableaunoir splits your board in "screen" or "window". Each window is a page in your PDF. 

#### Example 1
If you have drawn on a single window only, then the PDF is made up of a single page containing all the board.

#### Example 2
If you have drawn on two windows, then the PDF is made up of two pages. The first page contains the leftmost window; the second page contains the rightmost window.

### Presentation

Tableaunoir makes a page for each slide. The size of each page is the size of the board, and is at least the size of a window. The first PDF page is the first slide, the second PDF page is the second slide, and so on.
