---
permalink: /assignments/pop-model/
layout: single
title: Population Modeling Assignment Overview
author_profile: false
classes: wide
excerpt: This assignment will introduce you to the wonderful world of population modeling. 
sidebar:
  nav: "Course Materials"
header:
  overlay_filter: 0.5
  overlay_image: /assets/images/matrix.png
  actions:
    - label: "Download"
      url: "https://colebrookson.github.io/marine-pop-ecol/assignments/pop-model.pdf"
  caption: "Photo credit: Jono Tonkin"
---

Population models can take many forms, but with populations we classify as age/stage-structured, building models to explicitly account for those stages is helpful. The purpose of this assignment is to introduce you to modeling stage-structured populations in the form of matrix models. This assignment has two parts. Part 1 is a brief proposal of research so that we can make sure you are on the right track. Part 2 requires you to do research on your own and build a matrix model with accompanying write up. 

## Assignment Overview

You will: 

1. Select a species to analyse their population growth
2. Report the life history of the species including stage structure 
3. Draw a life-cycle graph of species demography
4. Write a set of equations for population growth of the species
5. Using the published literature, parameterize your model
6. Assess the population growth rate for your species
7. Perform an elasticity analysis of the growth rate
8. Contextualize your results in the relevant literature

This project will be done in **groups of two students.** You are both expected to contribute equally to the project. You will both be required to turn in *identical* reports. 

*Note: Much of this content has been informed and borrowed from iterations of population ecology courses run by Drs. Stephanie Green & Martin Krkošek.*

## Submitted Content

### Proposal (7 points)

For this project, each group must submit a brief, 500 word proposal covering points 1-5 above. The purpose of this proposal is for the instructors to ensure you are on the right path, and to give you feedback on the model before you analyse it. The proposal should have:

1. A brief paragraph on the species you selected, and it's life history. In this section, explicitly discuss the foundational papers on the species that you are using to describe the population and stage structure (2 points)
2. The life cycle-graph denoting all relevant parameters symbolically (2 points)
3. All equations for your model, and a corresponding table with parameter values and citations of where they are coming from. In cases where numerical values for parameters cannot be found, values can be chosen from closely related species or a rationale could be provided for the range of values that will be considered in your analysis (3 points)

See the grading rubric regarding how the proposal will be graded. 

### Final Report

The final report will cover all the objectives listed above. It will be a maximum of 3000 words not including code. Information from your proposal can be copied directly into the final report. The report will have the basic sections of an academic manuscript: 
1. **Introduction** (3 points)
  - Introduce the species, life history, why you chose this species, and outline the objectives of your analysis. This section should follow the logical flow of any academic introduction, following an inverted funnel. Start broad, discuss why your species/question is of interest, provide relevant background, then then with a paragraph summarizing what you will be doing in the paper from then on. This paragraph should include any hypotheses you may have, and some form of stated objectives.
2. **Model** (6 points)
  - Present your life-cycle graph with discussion, present your equations and define all parameters and state variables, present the population projection matrix, and provide all parameter values, citing the appropriate sources. Assume that I have never seen a matrix model before, and be very clear with the various explanations you might provide.
3. **Results**(5 points)
  - The meat of your report: present your analysis results including the population growth rate, the stable stage distribution, the elasticity analysis, any simulations you might have performed, and any sensitivity of the results to parameters you may not be certain about. That is, if there is quite a bit of uncertainty in a particular parameter (i.e. it is hard to estimate from data), discuss this. You could even show how, if you change that parameter, your results might change. **Note:** this is NOT the same as a sensitivity/elasticity analysis, but more of a comment on which parameters are hardest to get from data, and what that may mean for your results. 
4. **Discussion** (3 points)
  - Contextualize your results in the broader literature. Discuss how these results may inform conservation and management of the species in question, comment on whether or not the species is of interest broadly to conservation and mangement. In this section also include assumptions and caveats to your analysis, how your conclusions may be affected by them, and why you made them. You may also include some possible follow-up questions/analyses that you could include in some future project.
5. **References** (1 point)
- All references for your report including sources for parameterization are listed here. Format the citations in any consistent style. If you're looking for one, you may use APA or Ecology, as examples.

## Assessment

<style>
  .evaluation-table {
    border-collapse: collapse;
    margin: 25px 0;
    font-size: 0.9em;
    min-width: 400px;
    border-radius: 5px 5px 0 0;
    overflow: hidden;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
  }

  .evaluation-table thead tr {
    background-color: #44d7a8;
    color: #ffffff;
    text-align: left;
    font-weight: bold;
  }

  .evaluation-table th,
  .evaluation-table td {
    padding: 12px 15px;
  }

  .evaluation-table tbody tr {
    border-bottom: 1px solid #dddddd;
  }

  .evaluation-table tbody tr:last-of-type {
    border-bottom: 2px solid #44d7a8;
  }

  .evaluation-table tr:hover { background: #bebebe; }
  td a { 
      padding: 1px; 
  }

  .grading-table {
    border-collapse: collapse;
    margin: 25px 0;
    font-size: 0.9em;
    min-width: 400px;
    border-radius: 5px 5px 0 0;
    overflow: hidden;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
  }

  .grading-table thead tr {
    background-color: #44d7a8;
    color: #ffffff;
    text-align: left;
    font-weight: bold;
  }

  .grading-table th,
  .grading-table td {
    padding: 12px 15px;
  }

  .grading-table tbody tr {
    border-bottom: 1px solid #dddddd;
  }

  .grading-table tbody tr:last-of-type {
    border-bottom: 2px solid #44d7a8;
  }
</style>

<table class="evaluation-table">
    <thead>
        <tr>
            <th width=400>Component</th>
            <th width=400>Due Date</th>
            <th width=174>% of Grade</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Proposal</td>
            <td>22 October 2021 @ 18:00</td>
            <td>7</td>
        </tr>
        <tr>
            <td>Final Report</td>
            <td>27 October @23:59</td>
            <td>18</td>
        </tr>
    </tbody>
</table>

### Grading 

An excellent assignment will:
- Contain all the required information in each section, presented clearly and concisely without errors - All figures and tables will have appropriate captions.
- Be carefully researched - It will include appropriate references to available literature, which are not just cited but *interpreted*.
- Be written clearly and concisely – each paragraph will have a topic sentence that summarizes the main point of the paragraph, followed by sentences that present and analyze the evidence supporting each main point. The tone will be appropriate for a formal scientific report. 

#### Proposal Rubric


<table class="evaluation-table">
    <thead>
        <tr>
            <th width=150>Section</th>
            <th width=174>Life History Paragraph</th>
            <th width=174>Life Cycle Diagram</th>
            <th width=174>Model Equations</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Excellent (Full Marks)</td>
            <td>All relevant information included. Primary literature supporting the three essential items: a)choices of variables, b) life stages, and c) parameters, are mentioned and referenced. </td>
            <td>All stages are present, noting transitions, with transition arrows pointing the correct direction, and each arrow labeled with the corresponding parameter.The diagram is clear and easy to follow</td>
            <td>All equations are present, and follow logically and accurately from the life cycle diagram. Parameter symmbols are logical, and all subscripts are accurate. All parameter values are listed clearly in a table, and are accurate to the papers referenced in the life history paragraph.</td>
        </tr>
        <tr>
            <td>Fair (Half Marks)</td>
            <td>Most information included. One of a) the choice of variables, b) life stages, or c) the parameters were either not mentioned nor referenced.</td>
            <td>Almost all important information was included with 1-2 minor mistakes.</td>
            <td>There are 1-2 minor errors in the equations/parameter table.</td>
        </tr>
        <tr>
            <td>Poor (No Marks)</td>
            <td>>1 of a) the choice of variables, b) life stages, or c) the parameters were either not mentioned nor referenced.</td>
            <td>There were >2 incorrect components to the diagram.</td>
            <td>There were >2 incorrect components to the equations or the parameter table.</td>
        </tr>
    </tbody>
</table>

#### Final Project Rubric

<table class="evaluation-table">
    <thead>
        <tr>
            <th width=100>Section</th>
            <th width=100>Introduction</th>
            <th width=100>Model</th>
            <th width=100>Results</th>
            <th width=100>Discussion</th>
            <th width=100>References</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Excellent (Full Marks)</td>
            <td>All relevant information included. Primary literature is referenced, the structure is clear and informative, and the writing is concise and well-edited. Objectives/hypotheses are clearly stated in the concluding paragraph, and follow logically from the introduction thus far.</td>
            <td>All equations and components are present and well-described, parameters and state variables are defined. SI material is referenced appropriately. All analyses are described accurately, and the reasoning behind choosing them is outlined clearly.</td>
            <td>Essential elements are present: growth rate, stable stage distribution, elasticity analysis, and any simulations performed. Parameter values from data and their impact on the model is discussed. It is clear how the results correspond to the stated objectives. Values are stated properly, figures are neat and clear, and there are no errors. </td>
            <td>The results are contextualized effectively, citing from appropriate sources. The major limitations of the analysis are made clear, any caveats/assumptions are addressed, and logical next-steps for analysis are described. </td>
            <td>In text references are made when needed using a consistent formal style, and the reference list is complete, correctly formatted and follows consistent style. </td>
        </tr>
        <tr>
            <td>Fair (Half Marks)</td>
            <td>Most information included, with a few minor ommissions. Objectives are still present, but are perhaps confusing. Formatting is less than perfect, resulting in difficulty reading.</td>
            <td>Most information included, with a few minor ommissions. Some model information was unclear or missing, but the section was still mostly clear.</td>
            <td>Most information included, with a few minor ommissions. Some results were unclear or poorly described, but mostly present.</td>
            <td>Most information included, with a few minor ommissions. Some literature references/context were missed, or some assumptions not made explicit.</td>
            <td>Most references were correct with a few minor errors.</td>
        </tr>
        <tr>
            <td>Poor (No Marks)</td>
            <td>Serious lack of information regarding important information above. No objectives/hypotheses stated.</td>
            <td>Major lack of information or incorrect information regarding model construction and analysis.</td>
            <td>Key results were not discussed, or were incorrectly interpreted in whole.</td>
            <td>Major lack of context, assumptions and caveats not at all discussed.</td>
            <td>Serious issues with in text citations or reference list including multiple missing/miscited references.</td>
        </tr>
    </tbody>
</table>


## Submission Details

### Proposal Submission:

Use the GitHub classroom link here: [https://classroom.github.com/a/eXKmjwid](https://classroom.github.com/a/eXKmjwid) to accept the assignment and view submission instructions. 

## Final Submission:

Use the GitHub classroom link here: [https://classroom.github.com/a/RnRw17xX](https://classroom.github.com/a/RnRw17xX) to accept the assignment and view submission instructions. 


