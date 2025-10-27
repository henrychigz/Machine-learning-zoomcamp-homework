# Machine Learning Zoomcamp Homework

This repository contains homework assignments and exercises for the Machine Learning Zoomcamp course.

## Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

## Setup Instructions

### 1. Install Dependencies

First, install the required Python packages using pip:

```bash
pip install -r requirements.txt
```

Or install Jupyter Notebook and pandas individually:

```bash
pip install jupyter pandas numpy matplotlib scikit-learn
```

### 2. Starting Jupyter Notebook

#### Default Port (8888)

To start Jupyter Notebook on the default port (8888):

```bash
jupyter notebook
```

#### Custom Port

To start Jupyter Notebook on a specific port, use the `--port` option:

```bash
jupyter notebook --port 8889
```

Replace `8889` with your desired port number.

#### Additional Options

You can combine multiple options:

```bash
# Start on a specific port with a specific directory
jupyter notebook --port 8889 --notebook-dir /path/to/notebooks

# Start without opening the browser automatically
jupyter notebook --port 8889 --no-browser

# Allow access from any IP address (useful for remote access)
jupyter notebook --port 8889 --ip 0.0.0.0
```

### 3. Accessing Jupyter Notebook

After starting Jupyter Notebook, you'll see output similar to:

```
[I 12:34:56.789 NotebookApp] Serving notebooks from local directory: /home/user/Machine-learning-zoomcamp-homework
[I 12:34:56.789 NotebookApp] Jupyter Notebook is running at:
[I 12:34:56.789 NotebookApp] http://localhost:8889/?token=abc123...
```

Copy the URL with the token and paste it into your web browser to access Jupyter Notebook.

## Troubleshooting

### Port Already in Use

If you see an error like `OSError: [Errno 98] Address already in use`, the port is already occupied. Try:

1. **Use a different port:**
   ```bash
   jupyter notebook --port 8890
   ```

2. **Find and stop the process using the port:**
   ```bash
   # On Linux/Mac
   lsof -ti:8888 | xargs kill -9
   
   # On Windows (PowerShell)
   Get-Process -Id (Get-NetTCPConnection -LocalPort 8888).OwningProcess | Stop-Process
   ```

### Jupyter Not Found

If the `jupyter` command is not found:

1. Ensure you've installed Jupyter: `pip install jupyter`
2. Check if pip's bin directory is in your PATH
3. Try using: `python -m jupyter notebook --port 8889`

## Repository Structure

```
.
├── 01-intro/
│   └── lesson1.ipynb    # Introduction lesson notebooks
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

## Working with Notebooks

1. Navigate to the notebook you want to work with in the Jupyter interface
2. Click on the `.ipynb` file to open it
3. Run cells using `Shift + Enter` or the Run button
4. Save your work regularly using `Ctrl + S` or `Cmd + S`

## Additional Resources

- [Jupyter Notebook Documentation](https://jupyter-notebook.readthedocs.io/)
- [Machine Learning Zoomcamp Course](https://github.com/alexeygrigorev/mlbookcamp-code)
- [Pandas Documentation](https://pandas.pydata.org/docs/)