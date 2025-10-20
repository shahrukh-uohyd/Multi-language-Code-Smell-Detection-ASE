This repository provides the replication package for the study “Reevaluation and Refinement of Multi-Language Design Smell Detection and Impact Analysis.”
The study reexamines the detection accuracy, prevalence, and quality impact (fault- and change-proneness) of multi-language design smells in Java Native Interface (JNI)-based systems.

The package contains all datasets, ground truth, refined detection implementation, and empirical results needed to fully reproduce the study.
1. Dataset/

Contains the metadata and retrieval scripts for the dataset of 60 open-source multi-language projects.

fetch_projects.sh – Script to fetch all projects automatically.

projects_list.csv – Lists project names, repository URLs, and commit SHAs.

2. Detection Approach Revised/

Contains the refined implementation of the multi-language design smell detector.

Main file: mlssdd/DetectCodeSmellsAndAntiPatterns.java

To detect a specific smell, comment out other detectors and uncomment the target smell.

Run as a standard Java program; outputs are saved under the Results/Performance Evaluation/ folder.

3. Ground Truth/

Provides the manually validated dataset used to evaluate detector performance.

labeling_guidelines.txt – Describes labeling criteria and process.

15 subfolders – Each folder corresponds to one design smell and contains the verified smelly files for all 60 projects.

4. Results/

Contains two main subdirectories reflecting the analyses conducted in the study:

a. Performance Evaluation/

Compares the baseline and refined detectors on the new dataset.

results_of_baseline_detector_on_new_data/

results_of_revised_detector_on_new_data/

precision_and_recall_of_baseline_detector.csv

precision_and_recall_of_revised_detector.csv

These results quantify the improvement achieved by the refined detection implementation.

b. Prevalence/

Provides the updated empirical distributions of multi-language design smells.

general_smelly/ – Files affected by at least one smell per release.

prevalence_of_code_smells_on_old_data/ – Smell prevalence on dataset from Abidi et al.

prevalence_of_code_smells_on_new_data/ – Smell prevalence on the new dataset.

percentage_of_general_smelly_files_releaseWise.csv

percentage_of_smelly_files_affected_by_each_smell_old_data.csv

percentage_of_smelly_files_affected_by_each_smell_new_data.csv

5. Documentation

A detailed description of all folders, codes, and instructions for reproducing the study is provided in:

ReplicationUtilities.pdf

This document includes the complete replication procedure, setup steps, and execution instructions.
