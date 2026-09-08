# FIFA Women's World Cup 2023 — Football Analytics Case Study

## Project Overview

This project analyses the FIFA Women's World Cup 2023 using football event and match data to identify the tactical and performance indicators most strongly associated with success.

The objective is to understand not only which teams performed best, but also why they were successful, with a particular focus on attacking efficiency, chance creation, defensive performance, possession, transitions, and tactical profiles.

The analysis aims to translate tournament-level insights into actionable recommendations and performance benchmarks for a national women's football team.

## Client Brief

The client wants to understand which tactical and performance indicators were most strongly associated with success at the FIFA Women's World Cup 2023.

Rather than simply identifying the tournament's best-performing teams, the analysis focuses on understanding *what contributed to their success* and whether these performance patterns can be translated into actionable recommendations for a national women's team.

### Key Question

**What separates successful teams from unsuccessful teams at the FIFA Women's World Cup 2023?**

### Analytical Questions

The analysis investigates:

- Does possession correlate with winning?
- Do teams that create more shots necessarily score more goals?
- Which teams were most efficient in front of goal?
- Which teams overperformed or underperformed their expected goals?
- How important was defensive efficiency?
- Did successful teams create better-quality chances or simply more chances?
- Which teams were most effective in transition?
- How important were set pieces?
- Can different tactical profiles be identified among the tournament's strongest teams?
- Which performance indicators can be used as benchmarks for a national team?

## 3. Dataset & Methodology

**1. Does possession correlate with winning?**

*To interpret the relationships between performance indicators, Pearson's correlation coefficient (r) was used.*

*The coefficient ranges from -1 to +1:*

*+1 indicates a perfect positive correlation, meaning that both variables increase together.*
*0 indicates no linear correlation between the variables.*
*-1 indicates a perfect negative correlation, meaning that as one variable increases, the other decreases.*

**Possession showed a moderate positive correlation with winning (r = 0.422).**

This indicates that teams with higher possession tended to achieve better match outcomes during the tournament. However, the relationship was not strong enough to suggest that possession alone determines success.

The finding suggests that controlling possession can contribute to competitive performance, but must be combined with other factors such as chance creation, attacking efficiency, and defensive effectiveness.

**2. Do teams that create more shots necessarily score more goals?**

Not necessarily. To justify this answer, let's take a look at the xG metric:

Expected Goals (xG) estimates the likelihood of the chances created by a team resulting in a goal. Therefore, if the xG is higher than the actual number of goals scored, it means the team scored fewer goals than expected based on the quality of the chances created, which may indicate inefficiency in finishing.

The difference between *shots* and *shots on target* also helps explain this. A team can create many shooting opportunities, but if most of those shots are off target, they are less likely to result in goals. Therefore, a higher number of shots does not necessarily translate into more goals.

To add more depth to the analysis, I also calculated the correlation between *shots and goals* (0.525), as well as *xG and goals* (0.340). The correlation between the number of shots and the number of goals scored is moderate and positive, meaning that teams that took more shots tended to have more opportunities to score. However, this relationship isn't strong enough to make this conclusion a rule.

Additionally, the correlation between xG and goals was lower than the previous one, indicating a weaker linear relationship in this dataset. This reinforces the idea that creating opportunities is only part of the equation: teams also need to create accurate and high-quality chances and convert them efficiently.

**3. Which teams were the most efficient in front of goal?**

The teams that were the most efficient in front of goal were:

- *Japan:* 15 goals scored, 10.68 xG, *+4.31 goals above xG*
- *Netherlands:* 12 goals scored, 8.28 xG, *+3.72 goals above xG*
- *Germany:* 8 goals scored, 5.13 xG, *+2.87 goals above xG*

Although Spain won the tournament, they scored almost exactly as many goals as expected based on their xG, with 18 goals from 18.19 xG. In contrast, Japan significantly overperformed its xG, scoring 15 goals from 10.68 xG. This highlights the difference between *tournament success and finishing efficiency*.

Interestingly, Spain does not even rank among the top 10 teams in terms of goals scored above xG. This suggests that being highly efficient in front of goal does not necessarily translate into winning the tournament. Japan, for example, was the most efficient team by this measure but was eliminated in the quarter-finals, while Spain went on to win the competition.

**4. Which teams overperformed or underperformed their expected goals?**

As for the teams that underperformed their expected goals, we have one of the finalists:

- *Australia:* 10 goals scored, 19.37 xG *-9.36 goals under xG*
- *USA:* 4 goals scored, 13.37 xG, *- 9,37 goals under xG*
- *France:* 12 goals scored, 17,45 xG, *- 5,48 goals under xG*

As for the opposite (overperformed), we have the same ones as the previous question:

- *Japan:* 15 goals scored, 10.68 xG, *+4.31 goals above xG*
- *Netherlands:* 12 goals scored, 8.28 xG, *+3.72 goals above xG*
- *Germany:* 8 goals scored, 5.13 xG, *+2.87 goals above xG*

These results reinforce that creating high-quality chances does not automatically translate into goals. Finishing efficiency can have a significant impact on a team's ability to convert its opportunities into actual results. Finishing efficiency can have a significant impact on a team's ability to convert its opportunities into actual results. They also show that xG overperformance alone does not determine tournament success, as some teams significantly overperformed their xG but were eliminated before reaching the final stages of the competition.

**5. How important was defensive efficiency?**

The results were particularly impressive, with Nigeria (84.68), United States (84.22), and Netherlands (83.98) achieving the three highest Defensive Efficiency Scores.

However, these results also highlight an important aspect of defensive performance: defensive efficiency is strongly influenced by the opponent and by a team's overall style of play.

Nigeria, for example, often adopted a more defensive approach, prioritising compactness and protecting their own goal. This naturally resulted in a high number of defensive actions and helped them achieve the highest Defensive Efficiency Score.

In contrast, the United States and Netherlands displayed more balanced approaches, combining defensive organisation with greater involvement in possession and attacking phases. Their high scores therefore suggest that defensive efficiency does not necessarily come from simply defending deeper or making more defensive actions, but can also result from maintaining a strong balance between defensive and attacking phases.

This comparison shows that there is no single defensive profile associated with success. A team's defensive performance needs to be interpreted within the context of its tactical approach, the quality of its opponents, and the way it chooses to manage games.

**6. Did successful teams create better-quality chances or simply more chances?**

The data suggests that successful teams benefited from creating chances and, more importantly, converting them into accurate attempts, rather than simply taking a higher number of shots.

The strongest correlation with goals scored among the metrics analysed was found between shots on target and goals, with a correlation of 0.570. This represents a moderate positive relationship, indicating that teams that managed to put more shots on target tended to score more goals.

For comparison, the correlation between total shots and goals was 0.525, while the correlation between shot assists and goals was 0.467.

These results suggest that shot accuracy was more closely associated with goals than simply generating a high volume of shots or creating opportunities for shots. However, the correlations are still moderate, meaning that no single metric can fully explain a team's success.

Overall, the findings point towards the importance of creating opportunities and being able to turn them into accurate attempts, rather than simply taking more shots.

**7. Which teams were most effective in transition?**

According to the data, *Sweden had the highest transition efficiency (41.7%)*, followed by the *Netherlands (35.7%)* and *Spain (23.8%)*, the tournament winners.

This metric reflects a team's ability to *turn ball recoveries into attacking opportunities and, ultimately, goals*. It also provides insight into how effectively teams can adapt their approach during transitions, particularly when applying pressure after regaining possession.

Interestingly, Spain created the highest volume of shots after turnovers, with *42 attempts*, but had a lower conversion rate than Sweden and the Netherlands. This shows that creating more opportunities in transition does not necessarily mean being more efficient.

Overall, the results highlight the importance of *team coordination and efficiency during transitions*, as successful transition play depends not only on recovering the ball but also on collectively turning those recoveries into dangerous attacking situations and goals.

**8. How important were set pieces?**

Set pieces proved to be an important and, in some matches, decisive factor during the 2023 FIFA Women's World Cup.

Set pieces include goals scored from corners, free kicks and other dead-ball situations. Unlike open play, these situations give teams the opportunity to organise their positioning and execute previously prepared movements, creating structured scoring opportunities.

The data shows that set-piece goals could have a significant impact on the outcome of matches. In closely contested games, a single goal from a corner or free kick could be enough to change the result and determine which team progressed to the next stage.

This highlights the importance of set-piece organisation and execution, as these situations can provide teams with additional opportunities to score beyond what they create during open play.

Overall, set pieces should not be viewed simply as secondary attacking situations. They can be a decisive tactical weapon, particularly in matches where there is little difference between the teams in open play.

**9. Can different tactical profiles be identified among the tournament's strongest teams?**

Yes. All teams played at least three matches, which made it possible to identify recurring patterns throughout the competition.

The data suggests that teams adopted different tactical profiles. For example, *England showed a relatively balanced profile*, combining possession, attacking output and defensive organization rather than relying heavily on one particular aspect of the game.

On the other hand, *Switzerland appeared to be more adaptable*, changing their approach depending on the characteristics of their opponents. This suggests a more flexible tactical profile, where the team adjusted its style according to the demands of each match.

These differences show that there was no single tactical approach associated with success. Strong teams could achieve good results through different strategies, whether by maintaining a balanced approach or adapting their game plan to the opposition. 

Also, *formation provides an additional layer of context*, as teams can adopt different structures depending on their tactical approach and opposition. However, the same formation does not necessarily imply the same style of play.

**10. Which performance indicators can be used as benchmarks for a national team?**

The combination of all the metrics analysed throughout this project provides a comprehensive view of what to expect from a national team.

Rather than relying on a single performance indicator, attacking output, finishing efficiency, possession, passing, defensive performance, transition efficiency, set pieces and tactical profile can be analysed together to create a more complete benchmark of team performance.

One of the main advantages of using StatsBomb data is the large number of detailed metrics available, allowing teams to be analysed from multiple perspectives and providing a much more precise view of what happens during a match.

However, the value of the data can be further increased by creating a custom dataset that combines StatsBomb data with specifically engineered features. Through feature engineering, raw event data can be transformed into meaningful indicators tailored to the team's objectives, such as the Defensive Efficiency Score and Transition Efficiency developed in this analysis.

This approach allows a national team to establish its own benchmarks, monitor performance across different areas of the game, identify strengths and weaknesses, and compare tactical and performance patterns over time.

Overall, the analysis shows that there is no single metric that defines a successful team. A combination of indicators, supported by detailed event data and appropriate feature engineering, provides a much stronger foundation for evaluating and benchmarking national team performance.

# Conclusion: What separates successful teams from unsuccessful teams at the FIFA Women's World Cup 2023?

A Women's World Cup was not just a case study. For me, it provided an opportunity to understand the complexity of a tournament of this scale.

The metrics analysed do not define a team's strategy on their own. There are several factors that need to be considered, such as:

Efficiency
Attacking performance
Adaptability
The quality and difficulty of the group
The teams faced throughout the competition
The knockout stages, where a single result can determine progression even when teams are closely matched

*A team's success can therefore be measured by consistency throughout its journey*. For example, when analysed individually, Spain did not necessarily stand out as the strongest team across every metric. Sweden and the Netherlands performed better in some specific areas, and other teams also showed exceptional strengths. Nevertheless, Spain won the tournament.

This does not necessarily mean that Spain was the best team in every aspect of the game. Instead, their success can be understood through their consistency across different matches and phases of the competition.

There were teams with very strong individual characteristics: Nigeria showed outstanding defensive efficiency, Sweden had the highest transition efficiency, and Japan was the most efficient in converting goals relative to their expected output. However, Spain remained consistently competitive throughout the tournament and ultimately won the title.

This highlights an important lesson from the analysis: successful teams are not necessarily the best in one particular metric. They are able to maintain a strong and consistent level of performance across different areas of the game and adapt to the challenges presented by each opponent.

For this reason, analysing the performance of different teams can be valuable for a national team. It allows us to identify successful patterns and strategies, understand what works in different contexts, and potentially incorporate these insights into our own tactical approach.