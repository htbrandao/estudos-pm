# Rascunho

Recortes de sites e artigos (cross-reference).

<br><br>

## [[1] What is CRISP DM?](https://www.datascience-pm.com/crisp-dm-2/) (2023)

A process model that serves as the base for a data science process. It has six sequential phases:

    1) Business understanding: What does the business need?
    2) Data understanding: What data do we have / need? Is it clean?
    3) Data preparation: How do we organize the data for modeling?
    4) Modeling: What modeling techniques should we apply?
    5) Evaluation: Which model best meets the business objectives?
    6) Deployment: How do stakeholders access the results?

- Fase 1: Business understanding
    - Focuses on understanding the objectives and requirements of the project. Aside from the third task, the three other tasks in this phase are foundational project management activities that are universal to most projects:
        - A) Determine business objectives: You should first “thoroughly understand, from a business perspective, what the customer really wants to accomplish.” (CRISP-DM Guide) and then define business success criteria.
        - B) Assess situation: Determine resources availability, project requirements, assess risks and contingencies, and conduct a cost-benefit analysis.
        - C) Determine data mining goals: In addition to defining the business objectives, you should also define what success looks like from a technical data mining perspective.
        - D) Produce project plan: Select technologies and tools and define detailed plans for each project phase

- Fase 2: Data Understanding
    - Adding to the foundation of Business Understanding, it drives the focus to identify, collect, and analyze the data sets that can help you accomplish the project goals. This phase also has four tasks:
        - A) Collect initial data: Acquire the necessary data and (if necessary) load it into your analysis tool.
        - B) Describe data: Examine the data and document its surface properties like data format, number of records, or field identities.
        - C) Explore data: Dig deeper into the data. Query it, visualize it, and identify relationships among the data.
        - D) Verify data quality: How clean/dirty is the data? Document any quality issues.

- Fase 3: Data Preparation
    - This phase has five tasks:
        - A) Select data: Determine which data sets will be used and document reasons for inclusion/exclusion.
        - B) Clean data: Often this is the lengthiest task. Without it, you’ll likely fall victim to garbage-in, garbage-out. A common practice during this task is to correct, impute, or remove erroneous values.
        - C) Construct data: Derive new attributes that will be helpful. For example, derive someone’s body mass index from height and weight fields.
        - D) Integrate data: Create new data sets by combining data from multiple sources.
        - E) Format data: Re-format data as necessary. For example, you might convert string values that store numbers to numeric values so that you can perform mathematical operations.

- Fase 4: Modeling
    - Build and assess various models based on several different modeling techniques. This phase has four tasks:
        - A) Select modeling techniques: Determine which algorithms to try (e.g. regression, neural net).
        - B) Generate test design: Pending your modeling approach, you might need to split the data into training, test, and validation sets.
        - C) Build model: As glamorous as this might sound, this might just be executing a few lines of code like “reg = LinearRegression().fit(X, y)”.
        - D) Assess model: Generally, multiple models are competing against each other, and the data scientist needs to interpret the model results based on domain knowledge, the pre-defined success criteria, and the test design.
    - Although the CRISP-DM Guide suggests to “iterate model building and assessment until you strongly believe that you have found the best model(s)”,  in practice teams should continue iterating until they find a “good enough” model, proceed through the CRISP-DM lifecycle, then further improve the model in future iterations.

- Fase 5: Evaluation
    - Looks more broadly at which model best meets the business and what to do next. This phase has three tasks:
        - A) Evaluate results: Do the models meet the business success criteria? Which one(s) should we approve for the business?
        - B) Review process: Review the work accomplished. Was anything overlooked? Were all steps properly executed? Summarize findings and correct anything if needed.
        - C) Determine next steps: Based on the previous three tasks, determine whether to proceed to deployment, iterate further, or initiate new projects.

- Fase 6: Deployment
    - This final phase has four tasks:
        - A) Plan deployment: Develop and document a plan for deploying the model.
        - B) Plan monitoring and maintenance: Develop a thorough monitoring and maintenance plan to avoid issues during the operational phase (or post-project phase) of a model.
        - C) Produce final report: The project team documents a summary of the project which might include a final presentation of data mining results.
        - D) Review project: Conduct a project retrospective about what went well, what could have been better, and how to improve in the future.

CRISP-DM Agile: Vertical Slicing

![](img/1-crispdm-agile.png)


## [[1.1] Agile Data Science](https://www.datascience-pm.com/agile-data-science/) (2023)

Simply put, Agile Data Science merges Agile philosophies with data science practices.

It does not shoehorn data science into practices that compromise the natural data science life cycle.

Rather Agile data science respects data science for what it is — a highly exploratory process centered around scientific experimentation.

Although Agile’s underlying philosophy is the same for data science as in other industries, there are some important nuances for what this means in practice for data science

- Benefits of Agile Data Science:
    - More Relevant Deliverables: By defining requirements just before development (as opposed to all upfront in a project), the features are more likely to meet the most current needs. Indeed, the stakeholders’ initial requests often do not map to their needs. Agile practices help you discover the true needs earlier.
    - Quicker Delivery of Customer Value: By delivering incremental product features such as exploratory data reports, Tableau dashboards, or Minimal Viable Models, users gain value before the project’s end.
    - Real Feedback: By soliciting feedback on the functional product, the data scientists can more accurately assess whether their deliverables work “in the wild”. Meanwhile, the product manager can assess whether the deliverables provide the intended business value.
    - Cut Losses Early: No matter what you do, some data science projects simply fail. The sooner you get feedback that you’re headed to failure, the sooner you can pivot to related objectives or kill off the project.
    - Improved Communication: Agile focuses on individuals, collaboration, and clear communication. As data science teams scale and become more diverse, the benefits of effective communication also increase — both within the team and with the stakeholders.


## [[1.2] CRISP-DM – a Standard Methodology to Ensure a Good Outcome](https://www.datasciencecentral.com/crisp-dm-a-standard-methodology-to-ensure-a-good-outcome/) (2016)

To ensure quality in your data science group, make sure you’re enforcing a standard methodology.

The process or methodology of CRISP-DM is described in these six major steps:

    1) Business Understanding: Focuses on understanding the project objectives and requirements from a business perspective, and then converting this knowledge into a data mining problem definition and a preliminary plan.
    2 )Data Understanding: Starts with an initial data collection and proceeds with activities in order to get familiar with the data, to identify data quality problems, to discover first insights into the data, or to detect interesting subsets to form hypotheses for hidden information.
    3) Data Preparation: The data preparation phase covers all activities to construct the final dataset from the initial raw data.
    4) Modeling: Modeling techniques are selected and applied.  Since some techniques like neural nets have specific requirements regarding the form of the data, there can be a loop back here to data prep.
    5) Evaluation: Once one or more models have been built that appear to have high quality based on whichever loss functions have been selected, these need to be tested to ensure they generalize against unseen data and that all key business issues have been sufficiently considered.  The end result is the selection of the champion model(s).
    6) Deployment: Generally this will mean deploying a code representation of the model into an operating system to score or categorize new unseen data as it arises and to create a mechanism for the use of that new information in the solution of the original business problem.  Importantly, the code representation must also include all the data prep steps leading up to modeling so that the model will treat new raw data in the same manner as during model development.

In our recent article ([1.2.1](#121-3-tips-for-getting-the-most-out-of-your-data-science-team-2016)) about getting the most out of your data science team, we argued that if you are responsible for a data science group, one of your main tools for quality and efficiency is to ensure that a common methodology is being used.

For non-Traditional modeling projects like Deep Learning or Sentiment Analysis, all these projects need to be evaluated for their ability to generalize in the real world.  So yes, CRISP-DM provides strong guidance for even the most advanced of today’s data science activities.


## [[1.2.1]  3 Tips for Getting the Most Out of Your Data Science Team](https://www.datasciencecentral.com/3-tips-for-getting-the-most-out-of-your-data-science-team/) (2016)

1) Common Platform: There’s no longer a place for the lone wolf data scientist in an advanced analytics shop.  That almost assuredly means that you’ve needed to drive them toward a common advanced analytics platform.  Could be R or Python, or it could be SAS, SPSS, or one of the other proprietaries, but you can’t have everybody doing their own thing. Unless everybody’s speaking the same language the communication will suffer, meaning fewer minds can share a problem and that there’s less supervision and collaboration. 

2) Common Methodology: All data scientists are originally raised with certain principles and these are most commonly embodied in the CRISP-DM methodology (Cross Industry Standard Process for Data Mining).  I had the pleasure of helping to develop this back in the 90s and there’s nothing magic here, just good common sense.  But unless you have an agreed methodology and enforce it, you won’t know who is cutting corners and with what consequences.

3) How Much Accuracy Do You Need? Start keeping some metrics and figure out how long it is taking for your data scientists to produce models. Some problems are tougher than others but you can figure out the categories and which are comparable. The question is at what point did the cost of that increase in accuracy break even with the business value?  In many modeling situations especially those that involve buying behavior the breakeven is fairly straightforward to calculate.


## [[1.3] Comparing Data Science Project Management Methodologies via a Controlled Experiment](https://scholarspace.manoa.hawaii.edu/server/api/core/bitstreams/07ccfe0d-2ab8-44ce-945a-6a02da486468/content) (2017)

Step-by-step view on how to do data science has not materially evolved in the past 20 years. For example, they are similar to the KDD (Knowledge Discovery in Databases) process described  nearly twenty years ago [9]. In another example, the CRISP-DM (Cross Industry Standard Process for Data Mining) might also be viewed as a possible first step towards defining a data science methodology. CRISP-DM was established in the 1990s, and is a data mining process model for data mining experts [10]. The model mentions six high-level phases: business understanding, data understanding, data preparation, modeling, evaluation, and deployment. SEMMA [11] is the second most popular methodology, and consist of tasks such as: sampling, exploring, modifying,
modeling, assessing. While these process models differ in details, at a high level they are broadly similar. We note though that no model seems to have achieved wide acceptance. For example, there has been a reported decrease within the KDD community of people using CRISP-DM and SEMMA, and an increase in people using their own methodology [12].

![](img/131-project-results.png)

![](img/131-student-perceptions.png)

![](img/131-what-worked-well.png)

Perhaps a bit surprisingly, the Agile Scrum methodology was actually worse than the Baseline condition. Why not Agile Scrum? First, it was a difficult process for a team to fully utilize. In addition, task estimation was very difficult. Why was Agile Kanban effective? Perhaps it was due to its’ culture of continuous improvement. Why was the CRISP model effective? It was a very natural way of conducting the projects: understanding, analysis, etc. and making loops/iterations if necessary. It is also interesting to note that the students’ without an assigned methodology started to converge into a CRISP-like methodology.

## [[1.4] Big data team process methodologies: A literature review and the identification of key factors for a project's success](https://ieeexplore.ieee.org/abstract/document/7840936) (2017)

> paywall


## [[1.5] Predicting data science sociotechnical execution challenges by categorizing data science projects](https://asistdl.onlinelibrary.wiley.com/doi/abs/10.1002/asi.23873) (2017)

> paywall


## [[2] What is the CRISP-DM methodology?](https://www.sv-europe.com/crisp-dm-methodology/#one)

This model is an idealised sequence of events. In practice many of the tasks can be performed in a different order and it will often be necessary to backtrack to previous tasks and repeat certain actions. The model does not try to capture all possible routes through the data mining process.

1) Business understanding:

    - What are the desired outputs of the project?
        - Set objectives: This means describing your primary objective from a business perspective. There may also be other related questions that you would like to address. For example, your primary goal might be to keep current customers by predicting when they are prone to move to a competitor. Related business questions might be “Does the channel used affect whether customers stay or go?” or “Will lower ATM fees significantly reduce the number of high-value customers who leave?”
        - Produce project plan: Here you’ll describe the plan for achieving the data mining and business goals. The plan should specify the steps to be performed during the rest of the project, including the initial selection of tools and techniques.
        - Business success criteria: Here you’ll lay out the criteria that you’ll use to determine whether the project has been successful from the business point of view. These should ideally be specific and measurable, for example reduction of customer churn to a certain level, however sometimes it might be necessary to have more subjective criteria such as “give useful insights into the relationships.” If this is the case then it needs to be clear who it is that makes the subjective judgment.
    - Assess the current situation:
        - Inventory of resources: List the resources available to the project including:
        Personnel (business experts, data experts, technical support, data mining experts)
        Data (fixed extracts, access to live, warehoused, or operational data)
        Computing resources (hardware platforms)
        Software (data mining tools, other relevant software)
        - Requirements, assumptions and constraints: List all requirements of the project including the schedule of completion, the required comprehensibility and quality of results, and any data security concerns as well as any legal issues. Make sure that you are allowed to use the data. List the assumptions made by the project. These may be assumptions about the data that can be verified during data mining, but may also include non-verifiable assumptions about the business related to the project. It is particularly important to list the latter if they will affect the validity of the results. List the constraints on the project. These may be constraints on the availability of resources, but may also include technological constraints such as the size of data set that it is practical to use for modelling.
        - Risks and contingencies: List the risks or events that might delay the project or cause it to fail. List the corresponding contingency plans – what action will you take if these risks or events take place?
        - Terminology: Compile a glossary of terminology relevant to the project. This will generally have two components:
            - A glossary of relevant business terminology, which forms part of the business understanding available to the project. Constructing this glossary is a useful “knowledge elicitation” and education exercise.
            - A glossary of data mining terminology, illustrated with examples relevant to the business problem in question.
        - Costs and benefits: Construct a cost-benefit analysis for the project which compares the costs of the project with the potential benefits to the business if it is successful. This comparison should be as specific as possible. For example, you should use financial measures in a commercial situation.
    - Determine data mining goals:
        - Business success criteria: Describe the intended outputs of the project that enable the achievement of the business objectives.
        - Data mining success criteria: Define the criteria for a successful outcome to the project in technical terms—for example, a certain level of predictive accuracy or a propensity-to-purchase profile with a given degree of “lift.” As with business success criteria, it may be necessary to describe these in subjective terms, in which case the person or persons making the subjective judgment should be identified. 
    - Produce project plan:
        - Project plan: List the stages to be executed in the project, together with their duration, resources required, inputs, outputs, and dependencies. Where possible, try and make explicit the large-scale iterations in the data mining process, for example, repetitions of the modelling and evaluation phases. As part of the project plan, it is also important to analyze dependencies between time schedule and risks. Mark results of these analyses explicitly in the project plan, ideally with actions and recommendations if the risks are manifested. Decide at this point which evaluation strategy will be used in the evaluation phase. Your project plan will be a dynamic document. At the end of each phase you’ll review progress and achievements and update the project plan accordingly. Specific review points for these updates should be part of the project plan.
        - Initial assessment of tools and techniques: At the end of the first phase you should undertake an initial assessment of tools and techniques. Here, for example, you select a data mining tool that supports various methods for different stages of the process. It is important to assess tools and techniques early in the process since the selection of tools and techniques may influence the entire project.

2) Data understanding

    - Initial data collection report: List the data sources acquired together with their locations, the methods used to acquire them and any problems encountered. Record problems you encountered and any resolutions achieved. This will help both with future replication of this project and with the execution of similar future projects.
    - Data description report: Describe the data that has been acquired including its format, its quantity (for example, the number of records and fields in each table), the identities of the fields and any other surface features which have been discovered. Evaluate whether the data acquired satisfies your requirements.
        - Distribution of key attributes (for example, the target attribute of a prediction task)
        - Relationships between pairs or small numbers of attributes
        - Results of simple aggregations
        - Properties of significant sub-populations
        - Simple statistical analyses
        - Is the data complete (does it cover all the cases required)?
        - Is it correct, or does it contain errors and, if there are errors, how common are they?
        - Are there missing values in the data? If so, how are they represented, where do they occur, and how common are they?

3) Data preparation

    - Rationale for inclusion/exclusion: List the data to be included/excluded and the reasons for these decisions.
    - Data cleaning report: Describe what decisions and actions you took to address data quality problems. Consider any transformations of the data made for cleaning purposes and their possible impact on the analysis results.
    - Derived attributes: These are new attributes that are constructed from one or more existing attributes in the same record, for example you might use the variables of length and width to calculate a new variable of area.
    - Generated records: Here you describe the creation of any completely new records. For example you might need to create records for customers who made no purchase during the past year. There was no reason to have such records in the raw data, but for modelling purposes it might make sense to explicitly represent the fact that particular customers made zero purchases.
    - Merged data: Merging tables refers to joining together two or more tables that have different information about the same objects. For example a retail chain might have one table with information about each store’s general characteristics (e.g., floor space, type of mall), another table with summarised sales data (e.g., profit, percent change in sales from previous year), and another with information about the demographics of the surrounding area. Each of these tables contains one record for each store. These tables can be merged together into a new table with one record for each store, combining fields from the source tables.
    - Aggregations: Aggregations refers to operations in which new values are computed by summarising information from multiple records and/or tables. For example, converting a table of customer purchases where there is one record for each purchase into a new table where there is one record for each customer, with fields such as number of purchases, average purchase amount, percent of orders charged to credit card, percent of items under promotion etc.

4) Modeling

    - Modelling technique: Document the actual modelling technique that is to be used.
    Modelling assumptions: Many modelling techniques make specific assumptions about the data, for example that all attributes have uniform distributions, no missing values allowed, class attribute must be symbolic etc. Record any assumptions made.
    - Test design: Describe the intended plan for training, testing, and evaluating the models. A primary component of the plan is determining how to divide the available dataset into training, test and validation datasets.
    - Parameter settings: With any modelling tool there are often a large number of parameters that can be adjusted. List the parameters and their chosen values, along with the rationale for the choice of parameter settings.
    - Models: These are the actual models produced by the modelling tool, not a report on the models.
    - Model descriptions: Describe the resulting models, report on the interpretation of the models and document any difficulties encountered with their meanings.
    Model assessment: Summarise the results of this task, list the qualities of your generated models (e.g.in terms of accuracy) and rank their quality in relation to each other.
    - Revised parameter settings: According to the model assessment, revise parameter settings and tune them for the next modelling run. Iterate model building and assessment until you strongly believe that you have found the best model(s). Document all such revisions and assessments.

5) Evaluation
    - Assessment of data mining results: Summarise assessment results in terms of business success criteria, including a final statement regarding whether the project already meets the initial business objectives.
    - Approved models: After assessing models with respect to business success criteria, the generated models that meet the selected criteria become the approved models.
    - List of possible actions: List the potential further actions, along with the reasons for and against each option.
    - Decision: Describe the decision as to how to proceed, along with the rationale.

6) Deployment

    - Deployment plan: Summarise your deployment strategy including the necessary steps and how to perform them.
    - Monitoring and maintenance plan: Summarise the monitoring and maintenance strategy, including the necessary steps and how to perform them.
    - Final report: This is the final written report of the data mining engagement. It includes all of the previous deliverables, summarising and organising the results.
    - Final presentation: There will also often be a meeting at the conclusion of the project at which the results are presented to the customer.


## [[3] Project Management in Data Science using CRISP-DM](https://medium.com/international-school-of-ai-data-science/project-management-in-data-science-using-crisp-dm-54ee35a5f4f3)

> n/a

## [[4] CRISP-DM for Data Science Teams: 5 Actions to Consider](https://www.datascience-pm.com/crisp-dm-for-data-science-teams-5-actions-to-consider/)

With this in mind, when using CRISP-DM for data science projects, teams should consider the following items to help ensure a successful project:

1) Define a team process: The team process should define how the team communicates, prioritizes tasks and “loops back” to previous project phases. Some argue that CRISP-DM suffers from the same weaknesses of waterfall frameworks, and encumbers rapid iteration (since CRISP-DM has a heavy on documentation; for example, CRISP-DM calls for 12 reports prior to data collection). This is a good example of why a data science project should not be thought of as a waterfall effort. Some teams ignore the document aspect of CRISP-DM, but if this is done, there needs to be other mechanisms for the team to communicate and prioritize work. Hence, perhaps the largest drawback when using CRISP-DM is that it doesn’t really focus on how should the team collaborate, communicate, and effectively prioritize potential tasks? Teams can leverage the CRISP-DM phases, and then use a framework such as Scrum, Kanban or Data Driven Scrum to prioritize potential tasks.

2) Ensure multiple experiments: When using the CRISP-DM framework, it should also be clear how the team will repeat / iterate through the life cycle multiple times within a project. For example, after exploring some data and deploying an analysis, additional data might be added to the analysis. While it’s important to do multiple iterations, each team needs to determine how this would actually work for their project. So, the team needs to think through how iterations are defined and then evaluated (such as Scrum’s time boxed sprints, Data Driven Scrum’s functional iterations or Kanban’s focus on minimizing flow but not specific iterations).  For example, here is one way to merge CRSIP-DM and Scrum.

3) Define team roles: CRISP-DM does not include the concept of roles (nor a team). Roles can include stakeholders / product owners (to ensure the insight is actionable). See 10 reasons why you might need a product owner / product manager for some reasons why this is so important. In addition, there might need to be a team member more focused on process (in other words, a process master) or on an aspect of the analysis (such as data engineering). See the discussion on 8 roles in a data science team for more on the need for roles in a data science project.

4) Ensure actionable insight: How does the team ensure actionable insight? If the team does not focus in the stakeholders / product owners (which is possible within the CRISP-DM construct), there is the risk that there will be interesting insights, but that those insights will not be actionable.

5) Define the subitems within each phase: Finally, the six phases of a project are fairly high level. There are many potential subtasks within each phase of the project. The team needs to be clear how those tasks (within a phase) are defined, and how to ensure tasks will not be forgotten. Many have defined lists of tasks for each phase. Others have addressed these concerns by also defining additional high level phases (e.g., Microsoft’s TDSP). For example, some tasks that should be explicitly discussed include:
    - How/where does the team talk about potential bias (in the data or the machine learning algorithm) or if model transparency is required
    - How should missing data been handled
    - How to determine the appropriate level of accuracy for the business problem (sometimes, data scientists love to improve a model by 0.5% – without knowing the business value of that improvement)
    - How does the team know the results are valid (i.e., there was no error during the analysis)
    - If the model will be deployed in a production environment, how often will it need to be updated 


## [[5] Scaling Data Science: How We Use CRISP-DM and Agile](https://agilethought.com/blogs/scaling-data-science-use-crisp-dm-agile/)

How We Use it: At AgileThought, we blend the ideas of CRISP-DM with those of agile.  Our data science team members participate in the usual Scrum ceremonies (grooming, refinement, sprint planning, etc.).  While the original user story may look familiar, the backlog items for data science end up looking significantly different from those of traditional software.  For example, a user story for customer attrition might be “As a customer service representative, I want a monthly list of customers to contact with an incentive.”  Like we explained earlier using the Mega Subscription Co. example—which narrowed down its data science objectives to predicting likelihood of leaving and customer value—each one of these would need to be further broken down into testable experiments.  For example, we may refine ‘predicting likelihood’ to ‘predict likelihood using logistic regression, random forest, or gradient-boosted tree algorithms, with an F1 score of 0.75.’  To mark this story as done, the data scientist must evaluate these algorithms and record which algorithm produces the best performance score, or F1.  Then, the outcome is binarized to one of two outcomes: success or failure.  Assuming the best F1 from the experiment was 0.56 using logistic regression, we may decide to prioritize a story during the next Sprint to work on feature engineering so that we can improve our performance.


## [[6] How to apply CRISP-DM to AI and big data projects](https://www.cognilytica.com/how-to-apply-crisp-dm-to-ai-and-big-data-projects/)

> [6.1](#61-what-is-the-cognitive-project-management-for-ai-cpmai-methodology)

## [[6.1] What is the Cognitive Project Management for AI (CPMAI) Methodology?](https://www.cognilytica.com/what-is-the-cognitive-project-management-for-ai-cpmai-methodology/)

The Cognitive Project Management for AI (CPMAI) methodology is a vendor-neutral, data-centric, AI-specific, Agile methodology for running and managing AI, ML, and cognitive technology projects. Learn how this methodology is changing and improving the way AI & ML projects are run.

With the experience of thousands of AI projects, Cognilytica identifies 10 major reasons for why AI Projects fail:

1) Applying application development approaches to data-centric AI
2) Lack of sufficient quantity of data
3) Lack of sufficient quality of data
4) ROI Misalignment of AI solution to problem
5) Lack of planning for continued AI, model, data iteration and lifecycle
6) Misalignment of real world data and interaction against training data and models
7) Applying proof of concept thinking to real-world pilots
8) Underestimating time and cost of the data component of AI projects
9) Vendor misalignment on promise vs. reality
10) Overpromising AI capabilities and underdelivering projects

There are six primary CPMAI phases, all of which are iterative and data-centric:

1) CPMAI Phase I: Business Understanding – “Mapping the business problem to the AI solution.”
2) CPMAI Phase II: Data Understanding – “Getting a hold of the right data to address the problem.”
3) CPMAI Phase III: Data Preparation – “Getting the data ready for use in a data-centric AI - Project.”
4) CPMAI Phase IV: Model Development – “Producing an AI solution that addresses the business problem.”
5) CPMAI Phase V: Model Evaluation – “Determining whether the AI solution meets the real-world and business needs.”
6) CPMAI Phase VI: Model Operationalization – “Putting the AI solution to use in the real-world, and iterating to continue its delivery of value:”

![Alt text](img/61-cpmai.png)

1) Phase I: CPMAI uses Cognilytica’s Seven Patterns of AI as a way to shortcut and speed up cognitive projects (Hyper-Personalization, Patterns & Anomalities, Autonomous Systems, Goal-Driven Systems, Predictive Analysis, Conversations & Human Interaction, and Recognition).
    - What data-centric problem are we attempting to solve?
    - Should we solve this problem with AI / Cognitive Technology?
    - What portions of the project require / do not require AI?
    - What AI pattern(s) are we implementing?
    - What are the criteria for project success?
    - What requirements are needed to complete the project iteration?
    - What are the specific performance or KPI requirements for success for this project iteration?
    - What other important security, governance, cultural, ethical, and environmental considerations are there for the AI project?
    - Which of those considerations would be deal-stoppers if they were to have a negative impact?
    - What skills are necessary for successful project completion?


2) Phase II: Aims to address three key data requirements for AI projects: the availability and sources of data to meet business needs, the quality of that data and need for enhancement or augmentation, and the environments in which data is needed for training and real-world inference.
    - What data are necessary to achieve the objectives?
    - What is the quantity and quality of our data?
    - What internal and external data is necessary?
    - What are the requirements to augment existing data?
    - What are the requirements for ongoing data gathering and preparation?
    - What are the requirements for technology for data manipulation and transformation?
    - What other important data-relevant considerations are there for the AI project, including aspects of data governance, data security, data privacy, data access, data sharing, data storage and other key considerations?


3) Phase III: Wrangling data from the sources and transforming it to its required state, data cleansing to eliminate critical data flaws, and data augmentation and enhancement including data labeling to add necessary meaning and context to the data so that AI systems can properly learn from the data.
    - How must data be transformed to meet requirements?
    - Implementation of data cleansing, transformation, and manipulation
    - Iterations of the data engineering pipeline
    - Means by which data quality can continuously be monitored and evaluated
    - Use, extension, and modification of third-party data
    - Human-involved data annotation and manipulation (“labeling”)
    - Performance of additional data augmentation steps
    - Creation of data engineering pipelines

4) Phase IV: Focused on selecting the right approaches and algorithms for the model, based on the business requirements, data availability, and performance needs, and we also perform the actions of tuning and configuring the model for optimal performance with hyperparameter tuning, as well as perform necessary model training activities.
    - Appropriate algorithm selection
    - Performance of model training activities
    - Performance of model optimization activities
    - Determination of appropriate algorithm settings, and hyperparameters
    - Creation of ensemble models
    - Use of third-party models or extensions of models
    - Model development as appropriate for selected machine learning technique
    - Matching model performance against business requirements
    - The selection of appropriate infrastructure for model training

5) Phase V: Testing, model performance measurement and improvement, and determining needs for ongoing model iteration, a necessary part of any machine learning project plan.
    - Does the model meet requirements for accuracy, precision, and other metrics?
    - Determining and evaluating concerns on overfit and underfit of models
    - Evaluation of training, validation, and test curves for overall acceptability
    - Evaluation of models against business Key Performance Indicators (KPIs)
    - Determination of model suitability with regards to operationalization approach
    - Determination of means for model monitoring
    - Determination of means for model iteration and versioning

6) Phase VI: Model deployment, model management, and model governance.
    - How will this model be used in production / operational environments?
    - What are the requirements for data flow for a model to be useful?
    - What are the requirements for performance?
    - Operationalization of model in different environments
    - Implementation of model monitoring
    - Implementation of model versioning and governance
    - Evaluation of business performance
    - Determination of ongoing iteration requirements


## [[6.2] Why Can’t I use Agile or CRISP-DM to manage AI and Data Projects?](https://www.cognilytica.com/why-cant-i-use-agile-or-crisp-dm-to-manage-ai-and-data-projects/)

> vendendo sua própria metodologia [6.1](#61-what-is-the-cognitive-project-management-for-ai-cpmai-methodology)

## [[7] PMBOK: o que é e como é utilizado para gestão de projetos?](https://www.sydle.com/br/blog/pmbok-61e80383f41fbf069eb3ef2b)

O PMBOK norteia a gestão, fornecendo dados importantes para que empresas ao redor do mundo sigam direções uniformizadas, para reduzir falhas, melhorar o desempenho e ter uma previsão mais acertada sobre os resultados. Na 7a edição PMBOK: o PMBOK 7 é de 2021 e contempla abordagens ágeis, adaptativas e híbridas, e enfatiza a gestão de projetos orientada a mudanças.

É importante destacar que, embora muitas vezes seja citado assim, o PMBOK não é uma metodologia. O material é, na verdade, um guia de orientação de gerenciamento, mas que deve ser seguido de acordo com as necessidades e aspectos específicos do projeto.

De acordo com as definições do PMBOK, um projeto é um esforço temporário empreendido para criar um produto, serviço ou resultado exclusivo.

O gerenciamento de projetos PMBOK são conduzidos a partir de 5 subgrupos de processos: iniciação, planejamento, execução, monitoramento e controle, e encerramento.

1) Iniciação: Inclui a autorização para dar início ou não, além de definir um escopo inicial, que abrange as primeiras estimativas de custos. É neste processo que o gestor deve identificar as partes interessadas no projeto e começar os passos que antecedem a realização em si. Neste ponto, deve ser desenvolvido um documento que “oficializa a abertura do projeto” e contém informações importantes, que serão utilizadas também nos outros processos.

2) Planejamento: No planejamento, as atividades aumentam e ficam mais específicas. É neste subgrupo que se realizam tarefas como:
    - Plano de gerenciamento
    - Definição de escopo
    - Coleta de requisitos
    - Desenvolvimento de Estrutura Análitica do Projeto
    - Definição de cronograma e as atividades de cada etapa
    - Estimativa do tempo de duração de cada atividade
    - Estimativa de custos e definição de orçamento
    - Planejamento da gestão da qualidade e dos recursos disponíveis
    - Planejamento de comunicações
    - Identificação de riscos

3) Execução: Esse é grupo de processos em que o gestor de projetos define o que fazer, coordenando recursos humanos e materiais, além de motivar as partes envolvidas no projeto. As informações devem ser distribuídas para a equipe e o gerente deve conduzir todas as aquisições.

4) Monitoramento e Controle: Neste grupo de processos estão as atividades essenciais para avaliar o desempenho do projeto. É o momento de mostrar de onde se partiu e o quanto ainda falta para alcançar o objetivo traçado. esta etapa, ainda é possível fazer mudanças e estabelecer protocolos de alterações, mas sempre garantindo que não haja grandes variações. Esse grupo inclui processos como:
    - Monitoramento das etapas de trabalho
    - Controle sobre as mudanças
    - Validação e controle de escopo
    - Supervisão de cronograma
    - Monitoramento dos riscos
    - Acompanhamento das comunicações
    - Monitoramento das aquisições
    - Controle de custos
    - Reportes de desempenho.

5) Encerramento: O encerramento prevê que os resultados finais estejam alinhados aos parâmetros e critérios definidos anteriormente, com alcance dos objetivos e dos benefícios previstos. Nesse momento, espera-se que os seguintes resultados tenham sido obtidos:
    - Aceitação do cliente/usuário final
    - Objetivos do negócio e benefícios previstos atingidos
    - Objetivos do projeto alcançados
    - Validação e organização dos materiais usados no projeto


## [[8] Ser gerente de projetos: 6 dicas para se tornar um](https://blog.ipog.edu.br/engenharia-e-arquitetura/ser-gerente-de-projetos-6-dicas-para-se-tornar-um/)

1) Entender as necessidades do momento: Um gerente de projetos deve sempre perguntar “por que” e “para quê” realizar uma determinada atividade. Dessa forma, ele procura entender o que a empresa e a equipe precisam e como atender a demanda de forma satisfatória. Ao realizar este exercício estará realizando o gerenciamento de pessoas (stakeholders) e terá mais possibilidades de crescimento na carreira.

2) Ter capacidade de realização: O gerente de projetos é o líder da equipe e deve sempre pensar as decisões de forma positiva, com flexibilidade e tenacidade na hora de resolver os problemas. Portanto, deve estar sempre preparado para trabalhar no impasse, seja ele qual for, até que se encontre a solução ideal.

3) Ser um gerente de projetos exigente: Um bom gerente de projetos é exigente e detalhista, acompanha todo o trabalho do início ao fim, para garantir que ele realmente seja bem-feito, pois será cobrado pelo resultado de toda equipe.

4) Ter respeito com a equipe: O respeito deve prevalecer em quaisquer situações, portanto, deve-se evitar o conflito entre a equipe, evitando assim a perda de eficiência e produtividade. É importante que o gerente de projetos mantenha sempre a seriedade e serenidade, pois, caso haja excesso de companheirismo e amizade, sua equipe pode não te respeitar e, sem isso, não consegue atingir as suas metas propostas.

5) Valorizar a equipe: O gerente de projetos ao perceber que alguém da sua equipe se superou ou chamou a atenção de forma positiva, deve elogias, um elogio faz com que uma pessoa ou a equipe, trabalhe mais motivada e que produza resultados acima dos esperados.

6) Conhecer cursos e certificações de gerenciamento de projetos: ...


## [[9] Saiba tudo sobre PMBOK](https://blog.aevo.com.br/pmbok/)

Um dos pontos mais importantes do PMBoK para os projetos é que ele facilita a padronização. Assim, as atividades conseguem seguir uma lógica, melhorando todo o fluxo de dados e diminuindo os riscos. O que acaba gerando um aumento nos lucros e um maior controle em todo o resto da organização.

Os conhecimentos trazidos pelo PMBoK possibilitam os gestores a terem uma visão mais clara sobre todo o processo como um todo . Conseguindo assim padronizar processos e tornar a empresa mais eficiente, que gera um ganho de valor e uma melhor percepção do cliente.

Quais são os fatores:

    - Ambiental (e.g.: Fauna e flora)
    - Físicos e Infraestrutura (e.g.: Acomodação, distância, custos logísticos, etc.)
    - Humanos e Sociais (e.g.: Cultura da empresa, metodologias existentes)
    - Tecnológicos (e.g.: Softwares, hardware, etc)
    - Externos (e.g.: Legislação vigente, normativos)

Os processos trabalhados pelo PMBoK são complexos. Eles trazem uma verdadeira revolução quando implementados. São eles: 

    - Escopo
    - Tempo
    - Custos
    - Qualidade
    - Aquisições
    - Recursos humanos
    - Comunicação
    - Riscos
    - Partes stakeholders
    - Integração

PMBOK consiste de um macroprocesso.

