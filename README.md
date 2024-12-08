# SQL Project #
# Free-to-Paid-Conversion-Rate-with-SQL-
===========================================================================
**Objective**
          - This project explores user engagement patterns on an e-learning platform, aiming to understand how free users transition to paying customers. It focuses on the timeline of student activities, including registration, content engagement, and purchases, to measure conversion rates and evaluate user behavior.
===========================================================================

**Overview of the Database**
                - The project utilizes a sample database, db_course_conversions, containing three key tables:
1.	student_info: Holds student registration details, including student_id and date_registered.
2.	student_engagement: Tracks content engagement data, such as student_id and date_watched.
3.	student_purchases: Logs purchase details with student_id and date_purchased.

===========================================================================
**Key Questions Addressed**
1.	What percentage of students convert from free users to paying customers?
2.	How much time typically passes between registration and the first engagement?
3.	What is the average duration from the first engagement to the first purchase?

===========================================================================
**Implementation Details**

**Part 1: Extracting Key Engagement Metrics**
•	Joins student_info, student_engagement, and student_purchases to compile a dataset with:
 1. The first date of content engagement (first_date_watched).
 2. The earliest purchase date (first_date_purchased).
•	Calculates two time intervals:
 1. Registration to first content engagement (days_diff_reg_watch).
 2. First engagement to purchase (days_diff_watch_purch).
 3. Applies filtering to exclude invalid cases, such as missing purchases or mismatched engagement sequences.

**Part 2: Calculating Aggregated Metrics**
•	Uses the processed data from Part 1 to compute:
1. Conversion rate as a percentage of students who purchased after engaging.
2. Average time between registration and first engagement.
3. Average time between first engagement and purchase.
4. Aggregations and metrics are rounded for clarity and practical interpretation.

===========================================================================
### Findings ###
1.	The percentage of students convert from free users to paying customers is 11%
2.	Approx 3:42 Hours time typically passes between registration and the first engagement.
3.	26 days is the average duration from the first engagement to the first purchase.

===========================================================================
**Results and Insights:**
1.	Conversion Rate: Helps assess the effectiveness of the platform’s engagement-to-purchase funnel.
2.	Behavioral Timelines: Highlights the average time it takes for students to move from registration to engagement and engagement to purchase, offering actionable insights for marketing and retention strategies.
3.	Optimization Opportunities: Identifies patterns that can guide improvements in user onboarding, content delivery, and promotional campaigns.

===========================================================================
**Use Case Scenarios**

This project serves as a blueprint for companies in the e-learning industry to:
1. Monitor and enhance user engagement.
2. Design targeted campaigns to reduce conversion times.
3. Predict purchase likelihood based on engagement behavior.

By leveraging SQL’s analytical power, this project provides a data-driven foundation for boosting customer acquisition and retention.

===========================================================================
