# Same Score, Different Mistakes

### Interactive Comparison of Where Two Classifiers Fail

A course project for **DS-GA 3001: Visualization for Machine Learning**.

**Team:** Xiang Chen, Chengzhi He, and Ruoyan Xiong

## Project Status

This project is currently in the planning stage. Implementation has not started, and no trained models, working interface, or experimental results are available yet. We are refining the visual design and evaluation plan in response to proposal feedback.

## Overview

Two classifiers can achieve similar overall accuracy while making mistakes on different examples. Our project explores an interactive visualization that connects model comparisons to individual test instances, allowing analysts to examine shared errors, model-specific errors, and prediction confidence.

The project builds on ideas from **Squares** and **Boxer**, with a focus on comparing both models' predictions for the same instance.

## Research Focus

Our proposed revised research question is:

> What differences in two classifiers' errors can analysts discover through a joint, instance-level view of correctness and prediction confidence?

This revision is intended to guide a qualitative evaluation of the observations supported by the interface.

## Planned Visualization

Both classifiers will be evaluated on the same test dataset. Instances will be grouped into four categories:

| Category | Model A | Model B |
| --- | --- | --- |
| Both correct | Correct | Correct |
| Both wrong | Incorrect | Incorrect |
| Only A correct | Correct | Incorrect |
| Only B correct | Incorrect | Correct |

Planned interactions include:

- Filtering by class, correctness category, and prediction confidence.
- Inspecting individual images, recorded labels, and both models' predictions.
- Comparing confidence scores for the same instance.
- Connecting category summaries with detailed instance views.

The visual encoding of both models' confidence scores remains a design decision. We will explore alternatives through sketches and prototypes.

## Planned Implementation

- **Models:** a small CNN in PyTorch and an MLP in scikit-learn.
- **Datasets:** MNIST for examining known weaknesses and Fashion-MNIST for natural classification errors.
- **Interface:** D3.js.
- **Prediction data:** instance ID, recorded label, predicted labels, and confidence scores from both models.

These choices are planned and may change during development.

## Evaluation Direction

Following proposal feedback, we plan to replace the original controlled user study with qualitative case studies and formative feedback.

The evaluation will examine concrete discoveries and limitations, using confusion matrices and Boxer as comparison references. Any mislabeled-example retrieval metrics will serve as supporting analysis of the ranking method.

## Next Steps

- [ ] Finalize the research question and evaluation scope.
- [ ] Sketch alternatives for displaying both models' confidence.
- [ ] Train classifiers and export predictions.
- [ ] Build the interactive prototype.
- [ ] Document comparison cases and formative feedback.
- [ ] Prepare the final presentation and report.

## References

- Ren et al. (2016). *Squares: Supporting Interactive Performance Analysis for Multiclass Classifiers.*
- Gleicher et al. (2020). *Boxer: Interactive Comparison of Classifier Results.*
- Xiao et al. (2017). *Fashion-MNIST: A Novel Image Dataset for Benchmarking Machine Learning Algorithms.*
