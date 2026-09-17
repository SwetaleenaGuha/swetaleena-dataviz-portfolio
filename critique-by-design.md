|[home page](https://swetaleenaguha.github.io/swetaleena-dataviz-portfolio/)| [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Critique by Design: AI Risk Rankings

For this project, I redesigned a MakeoverMonday visualization exploring how occupations differ in their exposure to AI automation. I selected this topic because the impact of AI on different occupations is timely and relevant to a broad audience. The dataset also provides several variables—including AI automation risk, wages, and employment—that offered opportunities to rethink how the information could be communicated more clearly.

My goal throughout the redesign process was to make the differences in AI automation risk easier to compare at a glance while maintaining enough context for readers who wanted to explore the occupations in more detail.

## Step one: the visualization

I selected the **2026/W16 AI Risk Rankings** visualization from MakeoverMonday. The visualization presents occupations ranked by their estimated AI automation risk and also provides information about wages and employment.

[View the original MakeoverMonday dataset and visualization](https://makeovermonday.vercel.app/dataset/ai-risk-rankings)

I chose this visualization because the topic of AI automation and its potential impact on occupations immediately interested me. The visualization contains useful information, but the original presentation separates the highest-risk and lowest-risk occupations into table-style lists. While the values are available, I felt that the format made it harder to quickly compare the magnitude of risk across occupations.

This gave me an opportunity to explore whether a more visual comparison could make the main story easier to understand. In particular, I wanted readers to be able to quickly identify which occupations have the highest AI automation risk, see the contrast between high- and low-risk occupations, and still have access to contextual information such as wages and employment.

### Original AI Risk Rankings Visualization

<img width="1291" height="756" alt="AI_Risk_Original" src="https://github.com/user-attachments/assets/f69712f5-8985-468c-8348-1af76bab0ba4" />


## Step two: the critique

I evaluated the original visualization using Stephen Few's Data Visualization Effectiveness Profile through the course Google Form. My ratings were:

| Criterion | Rating |
|---|---:|
| Usefulness | 8/10 |
| Completeness | 7/10 |
| Perceptibility | 6/10 |
| Truthfulness | 8/10 |
| Intuitiveness | 7/10 |
| Aesthetics | 6/10 |
| Engagement | 6/10 |

The critique helped me recognize that the original visualization is useful and provides valuable context beyond the AI risk ranking itself. In particular, including wage and employment information allows the reader to understand more about each occupation rather than seeing only a risk score. The separation between the highest-risk and lowest-risk occupations also makes the overall comparison relatively easy to understand.

However, I found that the table-based design requires the reader to scan individual rows and numbers to compare occupations. This makes broader patterns and differences in AI automation risk harder to identify quickly. Although color is used to distinguish the two risk groups, the primary comparison still depends heavily on reading numerical values.

Based on this critique, I decided that my redesign should preserve the useful contextual information while creating a stronger visual hierarchy. I wanted to experiment with a ranked horizontal bar chart so that differences in AI automation risk could be compared through bar length rather than primarily through individual numbers. I also wanted to use color more intentionally while avoiding unnecessary visual clutter.

## Step three: Sketch a solution

After completing the critique, I sketched a horizontal bar chart as an alternative to the original table-based presentation. My main goal was to make differences in AI automation risk visually comparable instead of requiring the reader to compare individual numbers across rows.

In my initial wireframe, occupations were placed on the y-axis and AI automation risk on the x-axis, with the occupations ordered from higher to lower risk. I also considered using color to reinforce the direction from lower to higher risk. At this stage, I intentionally kept the sketch simple so that I could test the overall structure and visual hierarchy before building the final visualization.

### Initial Wireframe
<img width="4000" height="3000" alt="SKETCH" src="https://github.com/user-attachments/assets/cc99b3d5-abb3-488b-81b3-51f9ff879f48" />

## Step four: Test the solution
I tested my initial wireframe with three classmates during an in-class group critique. My goal was to determine whether the horizontal bar chart communicated the intended message clearly before I developed the final visualization in Tableau.

Before showing the wireframe, I prepared a short set of open-ended questions. I intentionally avoided explaining the visualization first because I wanted to see how participants interpreted the design on their own.

### Testing Questions

- Can you tell me what you think this visualization is showing?
- Can you describe what the visualization is telling you?
- Is there anything you find surprising or confusing?
- What aspects of the design make the information easier or harder to understand?
- Is there anything you would change or do differently?

### Participant Feedback

Three classmates participated in the critique. Because the discussion took place as a group, I recorded my notes cumulatively rather than attributing every comment to a specific participant. I therefore did not assign comments to individual participants after the session when I could not reliably remember who made each comment. The table below documents the specific feedback captured during the critique.

| Area Discussed | Specific Feedback |
|---|---|
| Overall interpretation | The participants understood that the visualization was comparing occupations according to their level of AI automation risk. |
| Chart format | The horizontal bar chart was considered easy to read and easier to compare than scanning individual values in a table. |
| Eye movement | The bar-chart structure reduced the amount of eye movement required to compare occupations. |
| Simplicity | The participants appreciated that the proposed design was simple and clearly understandable. |
| Color | The participants suggested adding purposeful color so that differences in risk would be easier to recognize visually. |
| Axes and labels | The participants suggested adding clearer x-axis and y-axis information so that the measure being displayed would be immediately understandable. |
| Narrative | The participants suggested being more explicit about the story of the visualization and why the topic of AI risk across occupations was selected. |
| Scope | The discussion suggested showing a broader range of occupations rather than limiting the final visualization to only a small subset. |

### Patterns Across the Feedback

Several common themes emerged from the critique. First, the horizontal bar-chart structure itself was working well. The participants found it simple, readable, and useful for comparing occupations, which supported my decision to retain this structure in the final design.

At the same time, the feedback identified areas where the wireframe could communicate the story more effectively. The strongest opportunities were clearer labeling, more intentional use of color, a stronger narrative, and a broader representation of the occupations in the dataset.

There were no major conflicting reactions about the basic chart type during the group critique. The feedback was primarily additive: rather than recommending a different visualization, the participants suggested ways to strengthen the existing horizontal bar-chart concept.

### Changes Made After Testing

Based on the critique, I made several changes when developing the final visualization:

| Feedback | Change in Final Design |
|---|---|
| The horizontal bar chart was easy to read and compare. | I retained the horizontal bar-chart structure. |
| Color could make the differences easier to understand. | I added risk-based color encoding, using red for high-risk occupations and green for low-risk occupations. |
| The axes and measure needed to be clearer. | I labeled the x-axis as **AI Automation Risk (%)** and made the occupation labels clearly visible. |
| The story needed to be more explicit. | I used the title **“Which Occupations Are Most at Risk from AI?”** and added a subtitle explaining the risk categories. |
| A broader range of occupations would provide more context. | I expanded the final visualization to include all 30 occupations in the dataset. |
| Additional information could be useful but might clutter the chart. | I kept wage and employment information in Tableau tooltips rather than displaying these variables directly on every bar. |

### Testing Takeaway

The testing process showed me that the basic structure of my redesign was understandable, but that clarity depends on more than selecting an appropriate chart type. Labeling, color, narrative, and the amount of information displayed all influence how quickly a reader can understand the visualization.

The peer feedback therefore did not lead me to replace the horizontal bar chart. Instead, it helped me refine the initial concept into a more complete final design with clearer visual hierarchy and context.

### Peer Feedback Notes
<img width="1911" height="2397" alt="Peer Feedbacks" src="https://github.com/user-attachments/assets/7a973071-5c46-44b8-8841-c070d951874a" />


## Step five: build the solution

After reviewing the critique and peer feedback, I built my final redesign in Tableau. I retained the horizontal bar chart from my wireframe because it allows readers to compare AI automation risk across occupations through bar length rather than relying primarily on individual numerical values.

The final visualization includes all 30 occupations in the dataset and sorts them from highest to lowest AI automation risk. I used red to identify high-risk occupations (risk score of 80 or above) and green to identify low-risk occupations (risk score below 40). Interestingly, there are no occupations in this dataset with risk scores between 40 and 79, which creates a noticeable separation between the two groups.

I also incorporated the feedback I received during testing. I added clearer axis labeling, purposeful color, and a more descriptive title and subtitle. Wage and employment information were retained in the Tableau tooltips so readers can access additional context without adding unnecessary information to the main chart.

### Final Redesign

[View the interactive visualization on Tableau Public](https://public.tableau.com/views/AIRiskRankingsRedesign/AIAutomationRiskbyOccupation?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

<img width="1000" height="398" alt="AI_Risk_Redesign_Final" src="https://github.com/user-attachments/assets/866b5ae7-8e68-467b-8ea2-b1cbe43dbc54" />

### Reflection

Compared with the original table-based visualization, my redesign shifts the reader's task from scanning individual rows to visually comparing bar lengths. The most immediate pattern is the large separation between the high-risk and low-risk occupations in this dataset. Telemarketers and Data Entry Keyers appear at the high end of the ranking, while occupations such as Dentists and Advertising, Marketing, Promotions, Public Relations, and Sales Managers appear at the low end.

This process showed me how critique, sketching, and user feedback can work together as part of an iterative design process. My initial critique identified comparison and visual hierarchy as opportunities for improvement, the sketch helped me test a simpler visual structure, and peer feedback led me to strengthen the use of color, labeling, narrative, and the range of occupations displayed. The final visualization therefore reflects several rounds of refinement rather than simply recreating the original visualization in a different chart type.

## References

- MakeoverMonday. “2026/W16 AI Risk Rankings.” Original data source credited as AI Exposure. https://makeovermonday.co.uk/
- Few, Stephen. “Data Visualization Effectiveness Profile.” *Visual Business Intelligence Newsletter*, January/February/March 2017. https://www.perceptualedge.com/articles/visual_business_intelligence/data_visualization_effectiveness_profile.pdf
- Tableau. Used to create and publish the final redesigned visualization. https://public.tableau.com/views/AIRiskRankingsRedesign/AIAutomationRiskbyOccupation

## AI acknowledgements

I used ChatGPT as a support tool during this assignment. I used it to help interpret the assignment requirements, organize and refine my written critique, troubleshoot Tableau during the redesign process, and improve the clarity and organization of this portfolio write-up.

I selected the original visualization, completed and submitted the critique form, created the hand-drawn wireframe, collected peer feedback, built and reviewed the final Tableau visualization, and made the final decisions about what to include in the redesign and portfolio.
