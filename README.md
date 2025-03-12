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
- Gurobi License - You have two options:
  - [Commercial License](https://www.gurobi.com/solutions/licensing/)
  - [Databricks-specific Licensing](https://support.gurobi.com/hc/en-us/articles/20659745842961-Databricks-Architecture-and-licensing)

## Usage

1. Set up a Databricks workspace
2. Import notebooks
3. Configure catalog and schema names
4. Run notebooks in sequence

## Key Dependencies

| Library | Description | License | Source |
|---------|-------------|---------|---------|
| Gurobi | Commercial optimization solver for large-scale mathematical programming | Commercial | https://www.gurobi.com/ |
| PySpark | Distributed computing framework for large-scale data processing | Apache 2.0 | https://pypi.org/project/pyspark/ |
| MLflow | Platform for ML lifecycle management including tracking experiments and models | Apache 2.0 | https://pypi.org/project/mlflow/ |
| Pandas | Data manipulation and analysis library | BSD 3-Clause | https://pypi.org/project/pandas/ |
| NumPy | Fundamental package for scientific computing | BSD 3-Clause | https://pypi.org/project/numpy/ |

## Contributors

- Linlin Yang (Aimpoint Digital)
- Juan Morinelli (Aimpoint Digital) 
- Peyman Mohajerian (Databricks)
- Bryan Smith (Databricks)

## License

This project is licensed under the Apache 2.0 License - see the LICENSE file for details.

Data sourced from [Rebrickable](https://rebrickable.com) under their [terms of use](https://rebrickable.com/terms/).


## Project support
Please note the code in this project is provided for your exploration only, and are not formally supported by Databricks with Service Level Agreements (SLAs). They are provided AS-IS and we do not make any guarantees of any kind. Please do not submit a support ticket relating to any issues arising from the use of these projects. The source in this project is provided subject to the Databricks License. All included or referenced third party libraries are subject to the licenses set forth below.

Any issues discovered through the use of this project should be filed as GitHub Issues on the Repo. They will be reviewed as time permits, but there are no formal SLAs for support.