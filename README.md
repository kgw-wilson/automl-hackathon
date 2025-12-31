# AutoML Hackathon

This repository contains a condensed version of our submission for the UW–Madison AutoML Hackathon (Fall 2022). The event was part of a multi-university AutoML competition with a $20,000 grand prize.

Our team, PureLeaf, was the only team from UW–Madison to successfully submit a working solution to the national competition (out of ~10 participating teams). We also won the Best Student Presentation award for our explanation of AutoML concepts and our project approach.

## Project Overview

The goal of the hackathon was to build an automated machine learning (AutoML) pipeline capable of training effective models with minimal prior knowledge of the dataset or task. AutoML frameworks evaluate and select from multiple model families (e.g., XGBoost, k-NN, neural networks) to identify high-performing solutions under constrained conditions.

We evaluated several AutoML frameworks—including Auto-Sklearn and PyCaret—and ultimately selected AutoGluon for its reliability and performance. Our workflow included:

•	Custom AutoML integration using AutoGluon within a constrained, containerized evaluation environment

•	Dynamic data handling, converting PyTorch datasets into tabular formats and supporting both single- and multi-label tasks

•	Time-aware training and inference, designed to operate under strict runtime budgets

•	Selective model search, limiting model families to improve stability and performance

•	Reproducible experimentation, using deterministic seeding and consistent preprocessing

We also began prototyping a custom model selection strategy inspired by multi-armed bandit algorithms, which we presented during the competition.

## Technical Challenges & Approach

A major challenge was configuring and running the provided codebase inside a Docker environment while managing dependencies, performance constraints, and limited runtime budgets. Once the environment was stabilized, we focused on improving baseline model performance.

Due to time constraints, we targeted 2 of the 10 hidden evaluation tasks hosted on the CodaLab server. Our final code successfully executed and outperformed the provided baselines on both tasks.

## Takeaways

This project strengthened my understanding of:

•	AutoML system design

•	Model benchmarking and evaluation

•	Docker-based ML workflows

•	Collaborative ML experimentation under time constraints

Overall, this was a highly rewarding experience both technically and collaboratively, and I’m very grateful to UW–Madison for hosting the event.
