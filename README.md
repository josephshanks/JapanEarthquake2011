# Pschology of the Great East Japan Earthquake

On Friday March 11, 2011 at 2:46 PM local time, a 9.1 magnitude earthquake hit just off the coast of Japan. The earthquake was approximately 43 miles east of the Oshika Peninsula of Tohoku and was calculated to be the fourth morst powerful earthquake in the world since humans started recording earthquake magnitudes in 1900. The earthquake triggered a powerful tsunami that reached heights of up to 40.5 meters. Residents of Sendai (the largest city in Tohoku) had only 8 minutes of warning before they had to decide their best plan of action for safety. The recommended plan of action was to evacuate immedietely, however when push comes to shove and you have 8 minutes to make your best decision for you and your family, you do whatever it is you think will keep you safe. As the great Mike Tyson once said, "Everybody has a plan until we get punched in the mouth." Japan was able to detect that a powerful earthquake was coming but even their earthquake sensors didn't predict one quite this large. 

### Data Sources

I have always been drawn to understanding the way people think, whether it be an interest in psychology, philosophy or nueroscience I'm  fascinated by this type of work. My path to finding this dataset was quite a bumpy one as originally I was looking for a psychology report on the study of nature vs nurture inspired by the great documentary "The Three Identical Strangers" (off topic but I highly recommend giving this documentary a watch). With how little we know about psychology and the human brain finding quality datasets was quite the challenge. I landed on this dataset that contained a personality test on each participant, the degree to which they were impacted by the event, and other interesting tidbits such as how each person reached out for help for various neccesities. The data was collected 2 years after the tragedy and tested on just over 1400 people that were located right at the heart of the tsunami. 

### Data Pipeline

The data was imported through an xlsx file into multiple panda dataframes. All data was in a integer type containing numerous null values throughout all of the dataframes. The integer types created its own challenges however it also gave me ease of access to sorting the data. I started with cleaning the data in each dataframe and renaming numerous column headers to make my EDA easier throughout my time working on this dataset. As I am not a certified psychologist, I relied on the creators of the dataset to categorize each personality question into 8 different personality types. The dataset contained 40 personality test questions such as "When someone asks me to do something for them, I cannot refuse" and " In everyday life, I take care of myself as far as possible." The participants then ranked each question on a scale of 0-5. I then sorted the 40 questions into their corresponding personality type giving me the following groups: altruism, emotional regulation, leadership, problem solving, self-improvement, self-transcendence, stubbornness, and etiquette.

### Analysis

First off, lets look at the demographics of the test participants. Again, all participants in this dataset were located in the Miyagi Prefecture where damage from the earthquake was most severe. 

<img src="Images/StackedBar3.png"
     alt="Demographics" />


As you can see, I categorized each group of people into the degree in which they expierenced mental struggle. This statistic was gathered on a three point scale - 0 being no impact, 1 being some impact, and 2 being a large impact. Unfortunately, this graph does not draw any major conclusions. One could say that the older age groups tend to expierence a larger impact to their mental stability however more testing on this would have to be done to confirm this hypothesis to be true and not just due to the small sample size of the dataset. Other factors might include older people having more wealth, property, and materialistic items that were ultimately lost during the tragedy. So lets move on...

Personality type is a very fluid subject, some might take a test such as the Myeers Briggs test and take it as a fact, some might look at their daily horoscope, and some may think that their personality type changes by the day. Typically, thinking of your personality on a spectrum is a great way to understand where you may be strong in and where you may be weak in. Below is an interesting scatter matrix of each personality type and their correlation to each other. You can definitely see some interesting insight here showing that some personality types are much more correlated to each other than others. 


<img src="Images/scatter.png"
     alt="personality correlation" />

As I mentioned, it is extremely hard to categorize personality and while this scatter matrix helps it is only two dimensional. We would need to categorize numerous personality types and find their correlation between every single one to truly narrow down what type of person is fundamentally different from another. With that said, this scatter matrix definitely gives us a general idea of what personality types correlate with another. For instance, there is high correlation with the problem solving personality type compared to etiquette where there is not much correlation at all. So we continue...

Next you can see a box and whisker plot for each personality type and its correlation to the level of impact the earthquake caused their mental wellbeing. 

<img src="Images/Altruism.png"
     alt="Box1" />
<img src="Images/EmoReg.png"
     alt="Box2" />
<img src="Images/Etiquette.png"
     alt="Box3" />
<img src="Images/Leadership.png"
     alt="Box4" />
<img src="Images/ProblemSolving.png"
     alt="Box5" />
<img src="Images/SelfImprove.png"
     alt="Box6" />
<img src="Images/SelfTranscendence.png"
     alt="Box7" />
<img src="Images/Stubbornness.png"
     alt="Box8" />

As you may notice, many of these personality types really don't differ at all when comparing it to how much of a struggle the earthquake caused them. What stands out to me is the problem solving and emotional regulation personality types where people who scored higher in these peresonality types had a slightly better mental health outcome. On the contrary, etiquette had a negative correlation such that people who scored as having a high amount of etiqutte might of actually fared worse during the disaster.

As I was suspecting, problem solving and emotional regulation seem crucial in combating your daily life tasks and what better way to test that then with an extreme case such as a life or death expierence like the Great East Japan Earthquake. It is considered that in this situation, evacuating the area immediately after the warning was considered the best possible thing you could have done given the circumstances. So, are people who tested high in emotional regulation actually more likely to evacuate immediately?

Lets see if this is true with a hypothesis test.

# State a scientific yes/no question



#### People who tested in Quartile 1 of emotional regulation are more likely to evacuate right away (considered the 'correct' decision) than people who tested below Quartile 3.

# Take a skeptical stance: state a null hypothesis

#### After hearing the warning that a tsunami and earthquake is coming, People in quartile 1 of emotional regulation are no more likely to evacuate the area than people below quartile 3.

<img src="Images/Screen Shot 2020-04-10 at 2.18.28 PM.png"
     alt="HypothesisTest" />


# Calculate p-value

### p-value = .028978

<img src="Images/Pvalue.png"
     alt="Pvalue" />

### P Value is less than alpha thus we may reject our null hypothesis

Our P-Value allows us to reject the null hypothesis. With this said, there are many biases that may have given us a false positive here. First off each person is self diagnosing themselves through a simple 40 question personality test. Realistically, this test can not truly encapsulate the personality of each person. Additionally, the test was given two full years after the event and while that definitely is not long enough to forget about an event as impactful as this earthquake that is a very long time to remember details of the event and your overall mental stability during that time. We also have to keep in mind their mental stability before the earthquake as well, were they already in a tough mental state and the earthquake compounded this feeling of mental trauma or possibly the test subject was in a great state of mind prior to the earthquake and they were able to get by without too much mental impact (reletively speaking). Of course, we can not test people who did not survive this tragic event and maybe their personality type would have shed a better light on where we should all improve upon given an event like this happens to one of us. Maybe that personality type can't even be improved upon no matter how hard we try and that nature is what gives us that skill rather than nurture. 

I hope you find this report interesting as much as I did creating it. Writing this in 2020, Japan still hasn't fully recovered from this tragic event and lives were changed forever. Thoughts and prayers go out to everyone who had to expierence this tragic event. 

Thank you,

Joseph Shanks


