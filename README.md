# Pschology of the Great East Japan Earthquake

On Friday March 11, 2011 at 2:46 PM local time, a 9.1 magnitude earthquake hit just off the coast of Japan. The earthquake was approximately 43 miles east of the Oshika Peninsula of Tohoku and was calculated to be the fourth morst powerful earthquake in the world since humans started recording earthquake magnitudes in 1900. The earthquake triggered a powerful tsunami that reached heights of up to 40.5 meters. Residents of Sendai (the largest city in Tohoku) had only 8 minutes of warning before they had to decide their best plan of action for safety. The recommended plan of action was to evacuate immedietely, however when push comes to shove and you have 8 minutes to make your best decision for you and your family, you do whatever it is you think will keep you safe. As the great Mike Tyson once said, "Everybody has a plan until we get punched in the mouth." Japan was able to detect that a powerful earthquake was coming but even their earthquake sensors didn't predict one quite this large. 

### Data Sources

I have always been drawn to understanding the way people think, whether it be an interest in psychology, philosophy or nueroscience I'm  fascinated by this type of work. My path to finding this dataset was quite a bumpy one as originally I was looking for a psychology report on the study of nature vs nurture slightly inspired by the great documentary "The Three Identical Strangers." Off topic but I highly recommend giving this documentary a watch. With how little we know about psychology and the human brain finding quality datasets was quite the challenge. I landed on this dataset that contained a personality test on each participant, the degree to which they were impacted by the event, and other interesting tidbits such as how each person reached out for help for various neccesities. The data was collected 2 years after the tragedy to just over 1400 people that were located right at the heart of the tsunami. 

### Data Pipeline

The data was imported through an xlsx file into multiple panda dataframes. All data was in a integer type containing numerous null values throughout all of the dataframes. The integer types created its own challenges however it also gave me ease of access to sorting the data. I started with cleaning the data in each dataframe and renaming numerous column headers to make my EDA easier throughout my time working on this dataset. As I am not a certified psychologist, I relied on the creators of the dataset to categorize each personality question into 8 different personality types. The dataset contained 40 personality test questions such as "When someone asks me to do something for them, I cannot refuse" and " In everyday life, I take care of myself as far as possible." The participants then ranked each question on a scale of 0-5. I then sorted the 40 questions into their corresponding personality type giving me the following groups: altruism, emotional regulation, leadership, problem solving, self-improvement, self-transcendence, stubbornness, and etiquette.

### Analysis

First off, lets look at the demographics of the test participants. Again, all participants in this dataset were located in the Miyagi Prefecture where damage from the earthquake was most severe. 

INSERT ANALYSIS HERE

As you can see, I categorized each group of people into the degree in which they expierenced mental struggle. This statistic was gathered on a three point scale - 0 being no impact, 1 being some impact, and 2 being a large impact. Unfortunately, this graph does not draw any major conclusions. One could say that the older age groups tend to expierence a larger impact to their mental stability however more testing on this would have to be done to confirm this hypothesis to be true and not just due to the small sample size of the dataset. Other factors might include older people having more wealth, property, and materialistic items that were ultimately lost during the tragedy. So lets move on...



