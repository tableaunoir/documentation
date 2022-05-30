# Export

Tableaunoir enables you to export your board in PNG and PDF.

## PNG image

Tableaunoir exports your board as a strip.


## PDF document

Tableaunoir exports your board as a PDF document. There are two behaviors depending on your board is a classical one or a presentation with slides:
- The typical case is a classical board. Almost all boards are classical one. For instance, if you never edited the timeline and never added new slide, then your board is *classical*.  Technically, a board is classical when it ss made up of a single "slide".
- A presentation is a board which contains several slides. To make presentations, read [How to make presentations/animations](timeline.md).


### Classical board

Each "screen" (i.e. "window") of your board is a page in your PDF. 

![image](https://user-images.githubusercontent.com/43071857/171044677-394bf1f8-a5e8-4a4c-8553-31ed37adde85.png)


As shown in the illustration, if you have drawn on three screens, then the PDF is made up of three pages. The first page contains the first (leftmost) window; the second page contains the second window; the third page contains the third (rightmost) window.
If you have drawn on a single window only, then the PDF is made up of a single page containing all the board.


### Presentation

Tableaunoir makes a page for each slide. The size of each page is the size of the board, and is at least the size of a window. The first PDF page is the first slide, the second PDF page is the second slide, and so on.
