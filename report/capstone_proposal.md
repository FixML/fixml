# Checklists and LLM prompts for efficient and effective test creation in data analysis - Initial Proposal
- Authored By John Shiu, Orix Au Yeung, Tony Shum, Yingzi Jin

# 1.0 EXECUTIVE SUMMARY

The rapid growth of global artificial intelligence (AI) market presents both opportunities and challenges. While AI systems have the potential to impact various aspects of human life, ensuring their software quality remains a significant concern. Current testing strategies for machine learning (ML) systems lack standardization and comprehensiveness, which poses risks to stakeholders such as financial losses and safety hazards.

Our proposal addresses this challenge by developing an end-to-end application that provides comprehensive test evaluation, tailored test recommendations, and automated test specifications generation. Through these features, users can systematically assess, improve, and include tests tailored to their ML systems. By leveraging human expertise and prompt engineering, we build our product to deliver actionable insights for improving users' test strategies and overall ML system reliability.

With an iterative development approach, we aim to develop our minimum viable product (MVP) in the first two weeks. We will further iterate and refine our product over the next 3 weeks. During the last 2 weeks, we will carry out rigorous system testing, finalize our final product and report, and deliver to our partners. Ultimately, our goal is to mitigate potential negative societal impacts associated with unreliable ML systems and promote trustworthiness.

# 2.0 INTRODUCTION

## 2.1 Problem Statement
Global artificial intelligence (AI) market is growing exponentially (Ref: https://www.grandviewresearch.com/industry-analysis/artificial-intelligence-ai-market), which is driven by its ability to autonomously make complex decisions impacting various aspects of human life, including financial transactions, autonomous transportation, and medical diagnosis, etc. 

However, ensuring the software quality of these systems is yet an open challenge (Ref: https://arxiv.org/pdf/2312.12604). A lack of a standardized and comprehensive approach to testing machine learning (ML) systems is observed, which might pose potential risks to stakeholders. Inadequate quality assurance in ML systems could possibly link to severe consequences such as financial losses (Ref: https://www.firstpost.com/business/sebis-circular-the-black-box-conundrum-and-misrepresentation-in-ai-based-mutual-funds-6625161.html) and safety hazards, which raises our concerns about the need for robust testing methodologies.

## 2.2 Our Objectives
Quality assurance in software engineering is dependent on testing suites. Our proposal aims to enhance the trustworthiness and robustness of applied ML software through the development of comprehensive ML system testing suites. We seek to improve the quality and reproducibility of ML systems (Ref: https://arxiv.org/abs/2207.07048) in both industry and academia via the systematic testing approach. Ultimately, our goal is to mitigate the potential negative societal impacts associated with unreliable ML systems.

# 3.0 OUR PRODUCT
Our solution offers an end-to-end application for evaluating and enhancing the robustness of users' machine learning (ML) systems. Key features include:
1. Comprehensive Test Evaluation
2. Tailored Test Recommendations
3. Automated Test Specification Generation

## 3.1 Description
Basically, our product can be utilized into 3 stages.

- Stage 1: Comprehensive Test Evaluation

    Users input the source code of their ML systems along with our suggested prompts into the application, which utilizes Large Language Model (LLM) to identify existing test suites within the code. A comprehensive report is generated and provides qualitative (e.g., test categories/strategies covered) and quantitative (e.g., test coverage/score) evaluations of the ML system's test quality.

- Stage 2: Tailored Test Recommendations

    Based on the robust checklist created by our team for testing applied ML code, the application assesses the adequacy of existing tests. Recommendations on additional test categories/strategies are provided based on the ML system's nature and test evaluation for improvement.

- Stage 3: Automated Test Specification Generation

    Users specify desired test categories/strategies and utilize our suggested LLM prompts within the application. The application autonomously engineers reproducible test data and software tests for reference, which serve as reliable starting points for users to utilize and improve their test suites within the ML systems.

## 3.2 Success Metrics

The success of our product will be dependent on the mutation testing result of the reference test cases generated by the application. A set of perturbations would be made to the ML project code and the success rate of detecting these perturbations by the implemented test cases will be recorded as the evaluation metric.

Our partner and stakeholders would expect to see a significant improvement in testing strategies of their ML systems post-application usage. Moreover, the application would demonstrate high accuracy in detecting faults, which ensure consistent and high quality ML projects upon updates. 

## 3.3 Data Science Approach

### 3.3.1 Data 

We will collect data from the 377 GitHub repositories identified in the study by Wattanakriengkrai et al. (2022) (Ref: https://www.sciencedirect.com/science/article/pii/S0164121221002144). The data will include repository metadata and source code sourced using GitHub API and custom scripts. To ensure relevance to our study, we will apply these criteria for filtering the data: 1) projects that are related to ML systems; 2) projects that contain test cases; 3) test cases are written in Python programming language.

{screencap/copy-and-paste of the code}

### 3.3.2 Methodologies
Our data science methodology incorporates both human expert evaluation and prompt engineering to assess and enhance the test quality of ML systems.

- Human Expert Evaluation

    We will begin by formulating a comprehensive checklist for evaluating the data and ML pipeline based on established testing strategies outlined in Openja et al. (2023) (Ref: https://arxiv.org/pdf/2312.12604) as the foundational framework. for assessing test quality within selected repositories. Our team will manually evaluate the test quality within the repository data based on the formulated checklist. The checklist will be refined during the process to ensure its applicability and robustness testing general ML systems.

- Prompt Engineering

    We will engineer prompts for LLM to serve various purposes across three stages:
    1. Prompts to examine test cases within ML system source codes and deliver qualitative and quantitative test scores.
    2. Prompts incorporated with the completed checklist to suggest potential testing strategies by comparing with ML system source codes.
    3. Prompts to generate test cases based on suggested testing strategies and ML system task types (Ref: https://ieeexplore.ieee.org/abstract/document/10329992)

### 3.3.3 Iterative Development Approach
As we leverage data from selected GitHub repositories and references research on testing strategies, it's important to acknowledge that this may not include all ML systems or testing methodologies. To address these considerations, we adopt an iterative development approach by setting up an open and scalable framework for this project. Our application could then undergo continuous updates based on users' feedback and contributors' insights.

We encourage users to interpret the artifacts generated by the application with a grain of salt and recognize the evolving nature of ML system testing practices.

# 4.0 DELIVERY TIMELINE
Our team follow a timeline for our product delivery. We also aim at close communication with our partner to align our product development with their expectation.

| Timeline | Milestones |
|---|---|
| Week 1 (Apr 29) | Initial Proposal and Presentation, Scrape repository data |
| Week 2 - 3 (May 6 - 17) | Deliver Initial Proposal, Initial Draft of Pipeline Test Checklist, Develop MVP (Evaluation Function, Recommendation Function, Test Specs Generation Function) |
| Week 4 - 6 (May 20 - Jun 7) | Iterations and Refinement on Test Checklist and Product Functions |
| Week 7 (Jun 10) | Final Product Presentation, Draft Final Product Report, Perform Product System Test|
| Week 8 (Jun 17) | Deliver Final Product and Final Product Report |

# References
> Reference to be done with Jupyter notebook