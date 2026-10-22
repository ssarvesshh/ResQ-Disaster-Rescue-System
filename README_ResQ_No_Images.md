# ResQ: Disaster Rescue Coordination and Emergency Prioritization System

## Overview

ResQ is a browser-based academic project that demonstrates how data
structures can support disaster-response coordination. It helps organize
reported incidents, prioritize emergencies, and track the assignment of
rescue teams through a simple command-center interface.

> **Disclaimer:** ResQ is an educational simulation only. It is not
> connected to emergency services, live GPS, or real rescue teams and
> must not be used to coordinate real emergencies.

## Objectives

-   Register and manage emergency incidents.
-   Prioritize incidents according to their urgency.
-   Assign available rescue teams to incidents.
-   Search for and review incident information.
-   Track incident status and view activity history.
-   Store project data locally in the browser and export data when
    supported.

## Data Structures Used

-   **Max-Heap / Priority Queue:** helps select the highest-priority
    incident.
-   **Circular Queue:** demonstrates orderly handling of available
    rescue teams.
-   **Hash Map:** supports quick lookup of incidents by ID.
-   **Stack:** supports an undo-style operation where implemented.
-   **Array / ArrayList-style collections:** keep track of incident
    records and activity.

These structures are used for learning and demonstration; exact
behaviour depends on the implementation in `index.html`.

## Features

-   Dashboard for viewing incidents and response activity.
-   Incident registration and priority-based handling.
-   Rescue-team assignment workflow.
-   Incident search and status tracking.
-   Activity log and sample map-style visualization.
-   Browser local storage for retaining data on the same browser.
-   Data export where supported by the application.

## How to Run

1.  Download or clone this repository.
2.  Open `index.html` in a modern web browser.
3.  Use the dashboard to explore the sample data and available controls.

No separate server is required for the basic single-file version.

## Project Structure

``` text
ResQ-Disaster-Rescue-System/
├── index.html
└── README.md
```

If you later add screenshots, place them in an `assets/` folder and
update this README with their paths.

## Technologies Used

-   HTML
-   CSS
-   JavaScript
-   Browser Local Storage

## Academic Purpose

This project demonstrates practical applications of data structures in
an emergency-coordination scenario. It is intended for academic
learning, demonstration, and discussion---not real-world emergency
response.

## Future Improvements

-   Connect to a backend database.
-   Add authentication and role-based access.
-   Add validated geographic data and map integration.
-   Improve reporting and analytics.
-   Add automated tests and more robust error handling.

## License

Add a license if you intend to specify how others may reuse this
project.
