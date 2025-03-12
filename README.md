<img src=https://raw.githubusercontent.com/databricks-industry-solutions/.github/main/profile/solacc_logo.png width="600px">

[![DBR](https://img.shields.io/badge/DBR-CHANGE_ME-red?logo=databricks&style=for-the-badge)](https://docs.databricks.com/release-notes/runtime/CHANGE_ME.html)
[![CLOUD](https://img.shields.io/badge/CLOUD-CHANGE_ME-blue?logo=googlecloud&style=for-the-badge)](https://databricks.com/try-databricks)

# LEGO Assortment Optimization

This project demonstrates mathematical optimization techniques for solving product assortment problems using LEGO datasets as an example. It leverages Databricks, PySpark, and Gurobi to optimize which LEGO sets can be built from available parts.

## Architecture

```mermaid
graph LR
    A[LEGO Dataset] --> B[Data Prep]
    B --> C[Optimization Model]
    C --> D[Results]
    
    subgraph Databricks
        B
        C
        D
    end

    subgraph External
        A
        E[Gurobi]
    end
    
    C <--> E
```

## Notebooks

1. `01_Prepare_Data.ipynb` - Processes raw LEGO dataset into optimization-ready format
2. `02_Optimization_Model.ipynb` - Introduces optimization concepts with a small example
3. `03_Optimization_Model_Large.ipynb` - Demonstrates large-scale optimization

## Prerequisites

- Databricks Runtime 15.4 LTS or later
- Python 3.10+
- Gurobi License (commercial license needed for large model)

## Usage

1. Set up a Databricks workspace
2. Import notebooks
3. Configure catalog and schema names
4. Run notebooks in sequence

## Key Dependencies

| Component | License | Purpose |
|-----------|---------|---------|
| Gurobi | Commercial | Optimization solver |
| PySpark | Apache 2.0 | Data processing |
| MLflow | Apache 2.0 | Experiment tracking |
| Pandas | BSD 3-Clause | Data manipulation |

## Contributors

- Juan Morinelli (Aimpoint Digital)
- Linlin Yang (Aimpoint Digital) 
- Peyman Mohajerian (Databricks)
- Bryan Smith (Databricks)

## License

This project is licensed under the Apache 2.0 License - see the LICENSE file for details.

Data sourced from [Rebrickable](https://rebrickable.com/downloads/) under their [terms of use](https://rebrickable.com/terms-of-service/).
