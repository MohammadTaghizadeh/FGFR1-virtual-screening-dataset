# Ensemble-Based Virtual Screening and Ligand Selection for FGFR1

This repository contains the dataset and metadata for the virtual screening of potential FGFR1 inhibitors. The project utilizes an ensemble-based docking approach to enhance the reliability of ligand selection for drug repurposing.

## Data Structure

### `FGFR1_Dataset.csv` / `FGFR1_Dataset.xlsx`
The main dataset consists of the following columns:

*   **`DrugBank_ID`**: Unique identifier for each compound from the DrugBank database.
*   **`Drug_Name`**: Generic or market name of the compound.
*   **`Formula`**: Molecular chemical formula of the ligand.
*   **`Frequency`**: The total count of appearances of the ligand in top-ranking results across all docking simulations.
*   **`Mean_Energy`**: The average binding affinity score (kcal/mol) calculated across the ensemble.
*   **`Best_Energy`**: The strongest (lowest) binding energy recorded for the ligand.
*   **`Mean_Rank`**: The average ranking position of the ligand across the library.
*   **`Files_Found`**: Lists the specific screening runs or ensemble batches where the ligand was identified (indicating consistency across different screening scenarios).
*   **`references`**: Citations, DOIs, or literature references for compounds previously identified and validated in experimental studies as known FGFR1 inhibitors (used as positive controls and for validation).

---

## Methodology
1.  **Ensemble Docking**: Multiple conformations of the FGFR1 receptor were used to account for structural flexibility during virtual screening.
2.  **Scoring & Selection**: Ligands were prioritized using a multi-parametric function incorporating **Binding Energy**, **Mean Rank**, and **Frequency**.
3.  **Cross-Validation**: Identified leads were cross-referenced with experimental literature (recorded in the `references` column) to benchmark the performance of the selection function.

## Software & Tools
*   **Virtual Screening**: AutoDock Vina / PyRx
*   **Data Processing**: R (dplyr), SPSS, and Microsoft Excel
*   **Phylogenetic Analysis**: MEGA11

## Citation
If you use this dataset, please cite:
> [Mohammad Taghizadeh], et al. "Ensemble-Based Virtual Screening and Ligand Selection for FGFR1." (2026).

## License
Licensed under the **MIT License)**.
