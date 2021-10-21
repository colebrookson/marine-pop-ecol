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
  - Introduce the species, life history, why you chose this species, and outline the objectives of your analysis 
2. **Model** (6 points)
  - Present your life-cycle graph with discussion, present your equations and define all parameters and state variables, present the population projection matrix, and provide all parameter values, citing the appropriate sources
3. **Results** (6 points)
  - The meat of your report: present your analysis results including the population growth rate, the stable stage distribution, the elasticity analysis, any simulations you might have performed, and any sensitivity of the results to parameters you may not be certain about 
4. **Discussion** (3 points)
  - Contextualize your results in the broader literature. Discuss how these results may inform conservation and management of the species in question, comment on whether or not the species is of interest broadly to conservation and mangement. In this section also include assumptions and caveats to your analysis, how your conclusions may be affected by them, and why you made them. 
5. **References** (1 point)
- All references for your report including sources for parameterization are listed here. Format the citations in the style of the journal *Ecology* 

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
            <td>26 October @09:00</td>
            <td>18</td>
        </tr>
    </tbody>
</table>

### Grading 

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
            <td>There were >2 incorrect components to the diagram.</td>
        </tr>
    </tbody>
</table>

An excellent assignment will:
- Contain all the required information in each section, presented clearly and concisely without errors - All figures and tables will have appropriate captions.
- Be carefully researched - It will include appropriate references to available literature, which are not just cited but *interpreted*.
- Be written clearly and concisely – each paragraph will have a topic sentence that summarizes the main point of the paragraph, followed by sentences that present and analyze the evidence supporting each main point. The tone will be appropriate for a formal scientific report. 

#### Rubric



## Submission Details

Use the GitHub classroom link here: [https://classroom.github.com/a/rZDwW2zV](https://classroom.github.com/a/rZDwW2zV) to accept the assignment and view submission instructions. 


