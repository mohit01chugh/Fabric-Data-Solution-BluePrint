                                                    # 🌟 Microsoft Fabric Data Solution Blueprint 🌟

[![Project Status](https://img.shields.io/badge/Status-Complete-green.svg)](https://github.com/YourRepoLinkHere)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## 🎯 Overview

**End-to-End (E2E) Reference Architecture** for building robust data analytics solutions entirely within **Microsoft Fabric**.

The solution demonstrates best practices across the entire data lifecycle: ingestion, transformation, storage in a **Lakehouse**, and presentation via **Power BI**. It is fully governed using **Application Lifecycle Management (ALM)** principles via Fabric's native Deployment Pipelines (CI/CD).

---

## ✨ Key Features

This blueprint showcases the seamless integration and workflow of core Fabric components:

* **Lakehouse Architecture:** Utilizing the Lakehouse as the unified central data hub, with data organized using the **Medallion Architecture** (Bronze → Silver → Gold layers).
* **Data Transformation:** Spark-based data processing and cleansing using **Notebooks** (PySpark/Scala) for scale and performance.
* **Analytics Layer:** Creation of **Semantic Models** (Datasets) directly from the Gold layer for high-performance Power BI reporting.
* **CI/CD Pipeline:** Demonstrates automated content promotion across **Development, Test, and Production** stages using **Fabric Deployment Pipelines**.
* **Environment Separation:** Use of **Deployment Rules** to automatically swap data sources and parameters between environments, eliminating manual configuration changes.

---

## 🛠️ Prerequisites

To deploy and run this solution, you will need:

1.  **Microsoft Fabric Capacity:** An active Fabric license (F64 or above recommended) to host the workspaces.
2.  **Git Repository:** Access to this repository via **Azure DevOps** or **GitHub** for Fabric's Git Integration feature.
3.  **Fabric Workspaces:** Three separate, dedicated workspaces (e.g., `fabric-dev`, `fabric-test`, `fabric-prod`) to map to the Pipeline stages.

---

## 📁 Repository Structure

The project assets are organized following industry-standard conventions:

| Folder | Description | Key Contents |
| :--- | :--- | :--- |
| **`src`** | **Source Code.** Contains all executable logic and core Fabric item definitions. | `.ipynb` Notebooks, Data Pipeline JSONs, ML model definitions. |
| **`config`** | **Configuration Files.** Contains non-sensitive environment settings and parameters. | JSON or YAML files for data source parameters. |
| **`data`** | **Sample Data.** Small, anonymous sample files needed to run and test the solution. | Sample `.csv` and `.json` files. |
| **`docs`** | **Documentation.** Detailed guides and architecture diagrams. | Setup guide, architecture overview. |
| **`assets`** | **Media.** Images and screenshots used within this README and documentation. | Pipeline screenshots, Dashboard visuals. |
| **`_temp`** | **Local Cache.** Folder for temporary files, excluded from Git tracking via `.gitignore`. | Local logs or temporary artifacts. |

---

## 🚀 Getting Started: Deployment Guide

Follow these steps to deploy the entire blueprint into your environment:

1.  **Clone the Repo:** Clone this repository to your local machine.
    ```bash
    git clone [https://github.com/YourRepoLinkHere/Fabric-Data-Solution-BluePrint.git](https://github.com/YourRepoLinkHere/Fabric-Data-Solution-BluePrint.git)
    ```
2.  **Setup Git Integration (Dev):** In your **Development** Fabric workspace, enable **Git Integration** and connect it to this GitHub repository's main branch. This will automatically populate the workspace with all items from the **`src`** folder.
3.  **Create Pipeline:** Follow the detailed steps provided in the comprehensive guide: **`docs/SETUP_GUIDE.md`** to create the Deployment Pipeline and map your three workspaces (Dev, Test, Prod) to the stages.
4.  **Deploy:** Once setup is complete, use the **Deployment Pipeline** interface to push the content from Development to Test, and finally to Production.

## 🖼️ Solution Walkthrough

* [View the Full Pipeline Architecture](assets/pipeline_architecture.png)
* [View the Final Power BI Dashboard](assets/final_dashboard.png)
