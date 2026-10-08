# Archery Performance Analytics

Data-driven platform for archers to record, analyze and track their performance, competitions, equipment and rankings.

## Overview

Archery Performance Analytics is a project focused on developing a data-driven platform for archers and coaches.

The platform aims to bring together competition results, training data and equipment information in a single environment, providing tools for performance tracking, historical analysis and ranking visualization.

The project is being developed as a Master's Final Project for the Master's Degree in Data Science & Artificial Intelligence.

## Main objectives

The platform will progressively incorporate functionalities such as:

* Recording training sessions and scores.
* Entering detailed score sheets, including arrow-by-arrow data.
* Importing and processing official competition results.
* Providing a competition calendar with filters.
* Tracking an archer's historical performance.
* Visualizing rankings by different geographical and sporting scopes.
* Managing multiple archer profiles and equipment configurations.
* Recording technical equipment information such as bow type, limbs, riser, draw weight and other relevant components.
* Storing sight marks for different shooting distances.
* Comparing performance across competitions, modalities and equipment configurations.

## Data sources

The project will use different types of sources depending on their purpose:

* **Official competition results:** RFETA and Ianseo.
* **Sporting regulations and definitions:** World Archery and RFETA.
* **Complementary sources:** publicly available competition classifications and other archery-related sources.
* **User-generated data:** training sessions, detailed score sheets and equipment information.

Official sources will be prioritized whenever the same information is available from multiple sources.

## Data processing

The project follows a layered data-processing approach:

```text
Raw → Silver → Gold
```

* **Raw:** original data collected from the source.
* **Silver:** cleaned, standardized and validated data.
* **Gold:** processed data prepared for analysis and application features.

The exact data model will be refined as real competition sources are explored.

## Planned functionality

### Competition calendar

A calendar will provide access to available competitions and progressively incorporate filters such as:

* Country
* Autonomous community
* City
* Date
* Modality
* Category
* Competition type

### Archer profiles

A user may manage more than one archer profile. This is intended to support situations such as:

* Managing profiles for family members or friends.
* Shooting with different bow configurations.
* Participating in different modalities.

Performance data will remain separated according to the relevant archer, modality and equipment configuration.

### Equipment

Profiles may contain technical information about the equipment used, including:

* Bow type
* Riser
* Limbs
* Draw weight
* Arrows
* Sight
* Stabilization
* Other relevant components

Sight marks may also be recorded for different distances.

### Competition results and rankings

The platform will distinguish between official rankings and rankings calculated by the application.

Whenever a ranking or classification is displayed, its source and/or calculation method will be identified to make its meaning and origin clear.

Rankings may eventually be available at different scopes, depending on data availability and the methodology used:

* World
* National
* Autonomous community
* Other defined scopes

## Project structure

```text
archery-performance-analytics/
│
├── data/
│   ├── raw/          # Original data
│   ├── silver/       # Clean data
│   ├── gold/         # Processed data
│   └── reference/    # Regulations and reference data
│
├── docs/
│   └── ...
│
├── notebooks/
│   └── ...
│
├── src/
│   ├── data/
│   ├── processing/
│   ├── analysis/
│   └── ...
│
├── tests/
│   └── ...
│
├── app.py
├── main.py
├── requirements.txt
└── README.md
```

During development, notebooks are used for exploration, testing and documentation. Stable functionality will progressively be moved into Python modules so that the final system can be executed independently of the notebooks.

## Development approach

The project is developed incrementally.

The initial stage focuses on:

1. Identifying and validating real data sources.
2. Extracting a small representative set of competition data.
3. Building the Raw → Silver → Gold data pipeline.
4. Defining the data model.
5. Developing the first analysis and visualization components.
6. Building the application layer.
7. Expanding the platform with additional sources and functionality.

The system will prioritize real and traceable data over fabricated or static datasets.

## Status

🚧 **In development**

The project is currently in the data exploration and preparation stage.
