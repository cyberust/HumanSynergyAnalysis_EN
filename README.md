# Human Synergy Analysis System

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cyberust/HumanSynergyAnalysis_EN/blob/main/HumanSynergyAnalysis_en.ipynb)

## Overview

This repository contains a system designed to analyze, predict, and visualize the synergy of a team based on the profiles of its members. The analysis leverages natural language processing to understand the semantics of each member's background, skills, and areas of expertise.

The analysis includes the following components:
- Semantic profile analysis using sentence embeddings.
- Synergy calculation based on skill complementarity, experience, network effects, and cultural diversity.
- Dynamic systems modeling to predict future team growth.
- Game theory analysis (Shapley value) to measure individual value contribution.
- Forecasting key business metrics.
- On-demand, interactive visualization of all results.

## How to Use

1.  Click the "Open in Colab" badge above to open the notebook in Google Colab.

2.  **(Recommended)** Prepare the following text files describing the profiles of the individuals for analysis. Place them in the root of your Google Drive ("My Drive").
    - `arale_cohen_profile.txt`
    - `yanay_geva_profile.txt`
    - `yasuyuki_sakane_profile.txt`
    
    *Note: If these files are not found, the script will still run, but the analysis will be based on placeholder data and will not produce meaningful results.*

3.  From the Google Colab menu, select "Runtime" > "Run all".

4.  If a pop-up appears asking for permission to access Google Drive, please grant it.

5.  The entire analysis pipeline will run. This will not display graphs automatically but will save all deliverables to a new folder in your Google Drive.

6.  A new folder named `synergy_semantic_analysis_[timestamp]` will be created in your "My Drive". Inside this folder, you will find:
    - `synergy_dashboard_V3.html`: An HTML file containing all interactive graphs.
    - `analysis_report_V3.md`: A Markdown file with the summary report.

7.  To view the graphs, you can either open the generated HTML file or run the final cells of the notebook to display them on-demand within Colab.

8. Visualizing the Results

    After the pipeline finishes, no graphs will be displayed automatically in the output. This is by design to prevent browser freezing issues with multiple complex plots.

    All graph objects are generated and stored in the `results` variable. To view any specific graph, **add a new code cell** at the end of the notebook and use one of the following commands:

    *To display the synergy heatmap:*
    ```python
    results['figures']['synergy_heatmap'].show()
    ```

    *To display the dynamic growth trajectory:*
    ```python
    results['figures']['growth_trajectory'].show()
    ```

    You can display any of the generated graphs using their keys: `synergy_heatmap`, `growth_trajectory`, `business_dashboard`, `shapley_values`, `network_graph`.

## License

This project is released under the MIT License.
