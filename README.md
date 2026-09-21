# Soil Course: Exercises & Custom Helper Package

Welcome to the **Soil Course** repository! This project contains a collection of practical exercises and data analysis workflows developed for a university course on Soil Science and Geotechnical Engineering.

To keep the exercise notebooks and scripts clean, readable, and focused on learning concepts, all repetitive data processing, plotting, and analytical routines have been encapsulated into a custom helper Python package (`soil_course`).

---

## 📁 Repository Structure

```text
soil-course-repo/
├── pyproject.toml         # Build configuration & dependency manager
├── README.md              # Project overview and usage guide
├── soil_course/           # Custom helper package source code
│   ├── __init__.py        # Package initialization
│   └── ...                # Core module utilities & helper functions
└── exercises/             # University lab assignments & exercise scripts
    ├── exercise_01.ipynb
    ├── exercise_02.py
    └── ...
```

* **`soil_course/`**: The core package containing simplified wrapper functions for mathematical calculations, statistical models, soil mechanics equations, and data visualization.
* **`exercises/`**: Jupyter Notebooks and Python scripts where exercise prompts are solved by invoking high-level functions from `soil_course`.
* **`pyproject.toml`**: Modern Python build file defining dependencies (`numpy`, `scipy`, `pandas`, `matplotlib`, `statsmodels`, `openpyxl`) and installation parameters.

---

## ⚙️ Installation & Setup

### Prerequisites
* **Python 3.8+**
* `pip` and `git` installed on your machine.

### Quick Start

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/soil-course.git
   cd soil-course
   ```

2. **Install the package and dependencies:**
   Run the following command in the root folder of the repository:
   ```bash
   pip install -e .
   ```
   > **Note:** The `-e` flag installs the package in **editable mode**. Any changes you make to functions inside the `soil_course/` folder will be immediately available in your exercise scripts without needing to re-install.

---

## 🚀 Usage Example

With the `soil_course` package installed, your exercise scripts remain concise and easy to read. 

```python
import pandas as pd
import soil_course as soil

# Load exercise dataset
data = pd.read_csv("exercises/data/sample_soil_test.csv")

# Execute simplified helper functions from the package
soil.plot_particle_size_distribution(data)
results = soil.calculate_atlerberg_limits(data)

print(results)
```

---

## 📦 Dependencies

The project relies on standard scientific Python packages managed via `pyproject.toml`:

* **`numpy`**: Numerical computations and array operations.
* **`pandas` & `openpyxl`**: Data structures, data handling, and Excel I/O.
* **`scipy`**: Advanced scientific and engineering routines.
* **`matplotlib`**: Plotting and graphical visualization.
* **`statsmodels`**: Statistical modeling and analysis.

---

## 📝 License & Acknowledgments

* **Course**: University Soil Science / Geotechnical Module
* **Author**: [Your Name]