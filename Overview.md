# QGIS Development overview


## 1. Standard approach
### Setting Up QGIS Development Environment on Linux (15 minutes)
### a. Prerequisites (5 minutes)
- Install essential dependencies on Ubuntu:
    ```bash
    sudo apt-get update
    sudo apt-get install build-essential cmake git python3-dev
    ```

### b. Setting Up QGIS Development Environment (5 minutes)
- Clone QGIS repository and set up QGIS development environment:
    ```bash
    git clone https://github.com/qgis/QGIS.git
    cd QGIS
    ```
- Building QGIS from source and installing dependencies like Qt and GDAL.
- Setting up a Python virtual environment for development (if applicable).


###  Basic Concepts in QGIS Development (10 minutes)
### a. QGIS Code Structure (5 minutes)
- Overview of key directories in the QGIS repository:
    - `src/`: Core C++ code
    - `python/`: Python bindings and plugins
    - `tests/`: Unit tests
- Brief walkthrough of important files and directories.

### b. Key Development Tools (5 minutes)
- **QGIS Desktop**: Using QGIS Desktop to test development work.
- **QGIS Python API (PyQGIS)**: Introduction to scripting within QGIS using Python:
    ```python
    from qgis.core import QgsVectorLayer
    layer = QgsVectorLayer("/path/to/your/shapefile.shp", "Layer name", "ogr")
    if not layer.isValid():
        print("Layer failed to load!")
    ```

---

## 2. Using Docker (40 minutes)
### a. System Setup

- Docker and Docker Compose installation
- QGIS repository cloning
- Container setup and initialization

### b. Development Workflow

- Building QGIS in container
- Source code editing procedures
- Test execution and verification
- Changes deployment process

### c. Best Practices and Maintenance

- Container resource management
- Environment cleanup procedures
- Troubleshooting steps

---

## 3. Contributing to QGIS (5 minutes)
### a. Forking and Pull Requests (5 minutes)
- Fork the QGIS repository and create a new branch for development.
- Git workflow for making changes and submitting pull requests:
    ```bash
    git checkout -b my-feature-branch
    git add .
    git commit -m "Add feature"
    git push origin my-feature-branch
    ```
- Submitting a pull request on GitHub for review.

### b. Coding Guidelines and Reviews (2 minutes)
- QGIS coding standards (PEP8 for Python, C++ coding standards).
- Importance of writing unit tests and documentation.
- Overview of the pull request review process.

---

## 4. QGIS Documentation and Resources (15 minutes)
### a. Official QGIS Documentation (10 minutes)
- Walkthrough of the [QGIS Developer Documentation](https://qgis.org/en/docs/).
- Key sections to look for setting up development environments, coding guidelines, and API references.

### b. Other Key Resources (5 minutes)
- **QGIS StackExchange**: Troubleshooting and learning from others.
- **QGIS IRC and Mailing Lists**: Engaging with the community for support and discussion.
- **QGIS Wiki**: Contributing to the community wiki for additional documentation.

---