---
tags: # These tags will be added to all cards
  - 100-days-log
props: # These are static variables that can be referenced in cards and templates.
  startDate: 1-5-2020
computed: # These are computed variables that can be referenced in cards and templates
  daysIn: Math.ceil(((new Date()).getTime() - (new Date('${startDate}')).getTime()) / (1000 * 3600 * 24))
  daysToGo: 100 - Number(${daysIn})
  startDay: (new Date('${startDate}')).toDateString()
  today: (new Date()).toDateString()
  now: (new Date()).getTime()
template: | # This is the template for new cards
  :100: Days of code, Day ${daysIn}: ${today}
  :rocket: **Progress:**  your progress here
  :thought_balloon: **Thoughts:**  your thoughts here
  :link: **Links to work:**  your links here
  #100DaysOfCode
links: # These are links that will be added to cards.  Notice how href is using a built in variable "encodedText"
  # All props and computed are available for href formatting
  # default props include "encodedText", "encodedMD" and the task object itself 
  - pack: fab # Can be fab or fas https://fontawesome.com/how-to-use/on-the-web/referencing-icons/basic-use
    icon: fa-twitter # The font-awesome icon to use 
    title: Tweet this card # What the user see's when they hover over the icon
    href: https://twitter.com/intent/tweet?text=${encodedText}%0ATweeted%20with%20@imdoneio
---

# 100 Days Of Code - Log
<!-- 
#NOTE:0 # :100: Days of code: Day ${daysIn} expand:1 refresh:300000
**Days to go: ${daysToGo}**
**Started on: ${startDay}**
- [Rules](rules.md)
- [Log - click here to see my progress](log.md)
- [FAQ](FAQ.md)
- [Resources](resources.md)
- [#100DaysOfCode Official Website](https://www.100daysofcode.com/)
- [#100DaysOfCode on Twitter](https://twitter.com/search?q=%23100DaysOfCode)
- [Edit My 100 Days of Code log](log.md:0:1)
-->

