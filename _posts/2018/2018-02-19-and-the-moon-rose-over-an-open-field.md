---
title: '"And the Moon Rose over an Open Field"'
categories:
- "2018"
---

Long ago, I used to say that the complex is simple and the simple is complex. Pure obfuscation wasn't the intent on my part—loved the extra points it dinged however. During that time, I'd go and talk about the number of lines of code in DOS vs. Windows 95 and 98 and their respective GUIs...

—you know it! That kind of banter picked up all the ladies! It made them as hot as when I'd pontificate on "up" when I was asked what it was. Ahh...social gatherings: the plight of the hapless INTJ not in his natural environment: "The gentleman caller in the blue suede shoes; he don't know what to do...." With the passage of time and self-analysis, we have [David Attenborough](https://www.youtube.com/watch?v=enu-qR0H_uk).


FWIW, I prefer [Leo's cover](https://www.youtube.com/watch?v=LtQUJMBH8uE).

But, back on point...

Simple and complex: Is -4.25 lbs a weight gain or a weight loss?

For this site, in displaying the weightloss from one day to the next, I wanted the widget formatted so that weightloss wouldn't be a negative number and weight gain would add a "+" The first part is easy. 318.75 – 314.25 = 4.5. No work needed. However flip it and 314.25 – 318.75 has semantic implications.

So, I made this toilsome equation in Google sheets. It's an if / then statement with some conversion added:

    =if(WeightCalcTab!c1<0,concatenate("+",text(abs(WeightCalcTab!c1),"_## ?/?")," lbs"),concatenate(text(WeightCalcTab!c1,"_ ## ?/?")," lbs"))

What is happening?

* If the weight difference is negative, make it positive, turn it into a fraction, change it to a string and append "+" to the front and "lbs" to the back.
* If the weight difference is not negative, same thing, but there's no need to turn it positive and don't append the "+" part.

It's a lot of work for just 1 character—even more for a scenario that won't happen in a fast. But, it's likely something that's going to be a holdover into the next phase.

Simple, but complex.