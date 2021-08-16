# Description 

The objective of this project was to display an understanding of SPSS and specific ML algorithms. 

My team and I answered the following questions about the SkillSet_Dataset file, which contains video game telemetric data from a cognitive study of a Complex SKill Leaning project.

1. What affects the expert level? How can the players improve their level? 
2. Are there any identifiable sets or “groups” of players within the data? If so, what are their distinguishing features? 
3. Investigate the association of the different variables. How many hidden factors are related to these characteristics? Can you interpret these factors?

I had to answer **question one**. Multiple linear regression analysis was applied to uncover what influenced player level. I chose regression analysis because of its ability to explain the outcome variable based on the relative contribution of the predictor variables.

I carried out the data preparation and modelling in r-studio. I found r-studio to be much more robust and allow more room for customization. So, I carried out the complete analysis in r-studio and then confirmed my findings in SPSS. Major decisions and key findings included: 

- Tested assumptions: normality, homoscedasticity, linearity, multicollinearity
- Found r-squared of each independent variable using loops
- Rearranged data using dplyr to order variables in order of r-squared
- Created MLR adding each independent variable, one at a time, based on r-squared in descending order using a loop
- Visualised MLR's adjusted r-squared by each variable added in order to determine the optimal number of variable 

The image below shows the MLR's adjusted r-squared as each respective variable was added. The final model needed to consider two things: total adjusted r-squared and the principal of parsimony. From the below image, I felt that the optimal model contained all variables until "TotalHours." This model had an adjusted r-squared which was 1% less than the maximum but contained three fewer variables. SPSS found the same variables as the optimal choice with the exception of "SelectByHotKeys," which was deemed as insignificant and removed.
