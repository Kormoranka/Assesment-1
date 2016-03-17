# Assesment-1
Assesment no.1

First I had to [google how to apply search criteria to data sheets] (http://www.mrexcel.com/forum/excel-questions/51386-deleting-lines-starting-certain-char.html).
I needed to eliminate counties that have names beginning with vowels. In English, vowels are  (A, E, I, O, U and sometimes Y (which would exclude Yakima)). Y seems [not to be a vowel at the beginning of a word] (http://www.phonicsontheweb.com/y-roles.php).

I used Data/Standard Filter to eliminate entries in Field Name CZ_NAME that meet the Condition Doesn’t begin with A AND E AND I AND O And U AND Y. Than in the column STATE I unchecked all, than checked WASHINGTON only.

After this I tried to decide what defines a storm. Per Wikipedia:
>A storm is any disturbed state of an environment or astronomical body's atmosphere especially affecting its surface, and strongly implying severe weather. It may be marked by significant disruptions to normal conditions such as strong wind, hail, thunder and lightning (a thunderstorm), heavy precipitation (snowstorm, rainstorm), heavy freezing rain (ice storm), strong winds (tropical cyclone, windstorm), or wind transporting some substance through the atmosphere as in a dust storm, blizzard, sandstorm, etc.

Upon Auto Filtering EVENT_TYPE Field, I decided to go only with Wildfire which seemed like the only positively non storm related event. LibreOffice listed only 7 CZ_NAME entries. 8 entries when I omitted Y from the list of vowels thus showing Yakima Valley. The only one that was listed involving no other EVENT_TYPE (such as strong or high wind that I thought could be an indicator of a storm) was Northeast Blue Mountains (entry 53339). Northeast Blue Mountains range through 3 out of 39 Washington state counties: Walla Walla, Columbia and Garfield. Entry 53339 specified that storm fire happened in Peoly which is in Garfield county.

__So my answer is: only 1, Garfield county.__

But I think I could be wrong here because when I looked up Wikipedia more carefully I realized wildfires could be storm related:
>Storms generally lead to negative impacts on lives and property such as storm surge, heavy rain or snow (causing flooding or road impassibility), lightning, wildfires, and verticalwind shear.

This means I should probably just exclude the word “storm” from data, as I just don’t have sufficient instructions to define a storm better than the word itself. I also decided to go with Y as a consonant at the beginning of a word, so in step one I omitted Y and went only with A, E, I, O, U.

So after filtering Field name CZ_NAME for Condition Does not begin with A, E, I, O and U and Field name STATE for Condition = WASHINGTON and Field name EVENT_TYPE for Condition Does not contain ‘storm’. I ended up with a bunch of entries in the CZ_NAME column which I selected and used command Sort. After that I decided that the fastest way would be to count old school all the instances of entries. (This excluded entries beginning in vowels but contained those beginning with Y).

The answer now was: 111 counties. (It would take me couple days to discern which of the 39 Washington state administrative counties they belong to.)
