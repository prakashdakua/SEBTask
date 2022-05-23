# SEBTask : Code sample test - nested boxes
This is a small assignment, designed to provide you, as applicant for a position at SEB, a chance
to give us a taste of the magic you create at the keyboard.

Please read the assignment carefully and write the code like you would do when working on a
production system. Please choose programming language for solving this task from this list of
our used technologies: Python or Java.

Please submit your answers at latest one day in advance of your interview. The preferred format
of your answers is a link to your code in a repository (e.g. GitHub) where you, in addition to your
code, also include a README.MD listing your answers to the two questions below.

...and it goes without saying - please work fully independently on this task.
Best of luck!

Nested boxes
Imagine you are about to buy the perfect gift for your nephew. Luckily, your nephew has told
you his number one wish for this year in confidence. The thing he wishes for birthday is a set of
boxes to nest and stack. Perfect, you say to yourself. That should be easy to find and shouldn't
cost a fortune either.
Right after that thought, your phone beeps. Apparently, your nephew forgot to mention, your
nephew really wants that at least one of the boxes in the set should be colored in shiny gold.
Things just got a bit more complicated.

After doing some research you realize that there's only one store in town that sells boxes to
stack or nest where at least one box is colored in shiny gold. Better than nothing. Well in the
store, you're facing the fact that of course the sets of boxes are nested from the start, meaning
you only see the other most box color. Fortunately, the store is also very generous in listing the
rules that were applied when packaging the boxes.


For example, consider the following rules:
```
light red boxes contain 1 bright white box, 2 muted yellow boxes.
dark orange boxes contain 3 bright white boxes, 4 muted yellow boxes.
bright white boxes contain 1 shiny gold box.
muted yellow boxes contain 2 shiny gold boxes, 9 faded blue boxes.
shiny gold boxes contain 1 dark olive box, 2 vibrant plum boxes.
dark olive boxes contain 3 faded blue boxes, 4 dotted black boxes.
vibrant plum boxes contain 5 faded blue boxes, 6 dotted black boxes.
faded blue boxes contain no other boxes.
dotted black boxes contain no other boxes
```

These rules specify the required contents for 9 box types. In this example, every faded blue box
is empty, every vibrant plum box contains 11 boxes (5 faded blue and 6 dotted black), and so on.

## First part
OMG! You need to make sure the set you buy really contains a shiny gold box. But you also
don't want to give it away to your nephew at first sight just how great of a present you've gotten
for him. You therefore decide to buy a set of boxes that contain at least one shiny gold box BUT,
where the outermost box is of any other color than shiny gold.
Standing in front of the shelf you decide to find out How many different colors of outermost
boxes can, eventually, contain at least one shiny gold box?

### Tip 1
In the above rules, the following options would be available to you:
A bright white box, which can hold your shiny gold box directly.
A muted yellow box, which can hold your shiny gold box directly, plus some other boxes.
A dark orange box, which can hold bright white and muted yellow boxes, either of which
could then hold your shiny gold box.
A light red box, which can hold bright white and muted yellow boxes, either of which
could then hold your shiny gold box.
So, in this example, the number of box colors that can eventually contain at least one shiny gold
**box is 4.**

### Question 1
**How many box colors can eventually contain at least one shiny gold box? (The complete
list of rules (which is attached in the file "input.txt") is quite long; make sure you get all of
it.)**

## Second part
After this initial analysis, you start counting. Will this really be an affordable gift as you
imagined...? The boxes are of high quality and regardless of size, they cost 1 EUR per box. Not
what you imagined but also not outrageous as such. What really makes you realize; this might
call for a visit at the bank to renegotiate your mortgage is not the price per box but because of
the ridiculous number of boxes you need to buy!

Consider again your shiny gold box and the rules from the above example:
```
faded blue boxes contain 0 other boxes.
dotted black boxes contain 0 other boxes.
vibrant plum boxes contain 11 other boxes: 5 faded blue boxes and 6 dotted black boxes.
dark olive boxes contain 7 other boxes: 3 faded blue boxes and 4 dotted black boxes.
```

So, a single shiny gold box must contain 1 dark olive box (and the 7 boxes within it) plus 2
vibrant plum boxes (and the 11 boxes within each of those): 1 + 1 * 7 + 2 + 2 * 11 = 32 boxes!
Already bad. But of course, the actual rules have a small chance of going several levels deeper
than this example; be sure to count all the boxes, even if the nesting becomes topologically
impractical!

```
Here's another example:
shiny gold boxes contain 2 dark red boxes.
dark red boxes contain 2 dark orange boxes.
dark orange boxes contain 2 dark yellow boxes.
dark yellow boxes contain 2 dark green boxes.
dark green boxes contain 2 dark blue boxes.
dark blue boxes contain 2 dark violet boxes.
dark violet boxes contain no other boxes.
```
**In this example, a single shiny gold box must contain 126 other boxes.**

### Question 2
**How many individual boxes are required inside your single shiny gold box?** 
