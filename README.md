# First CI Demo — Student Result Prediction

## Project Overview

This project demonstrates Continuous Integration (CI) using Python and GitHub Actions. It uses a simple rule-based function to predict whether a student passes or fails based on internal marks and attendance.

## Objectives

- Implement student result prediction using Python.
- Write automated unit tests using Python's `unittest` framework.
- Configure GitHub Actions to run tests automatically.
- Understand successful and failed CI workflow runs.

## Technologies Used

- Python
- Python `unittest`
- GitHub Actions
- YAML

## Project Structure

```text
first-ci-demo/
├── .github/
│   └── workflows/
│       └── ci.yml
├── result_logic.py
├── test_result_logic.py
└── README.md
```

## Result Prediction Logic

The `predict_result(internal_marks, attendance)` function returns:

- **PASS:** Internal marks are at least 40 and attendance is at least 75%.
- **FAIL:** Either condition is not satisfied.

```python
def predict_result(internal_marks, attendance):
    if internal_marks >= 40 and attendance >= 75:
        return "PASS"
    else:
        return "FAIL"
```

## Automated Testing

The `test_result_logic.py` file contains unit tests for the prediction logic.

Run the tests locally using:

```bash
python -m unittest -v
```

## GitHub Actions CI

The workflow is configured in `.github/workflows/ci.yml`. It runs automatically when code is pushed to `main` or when a pull request targets `main`.

The workflow checks out the repository, sets up Python, and runs the automated tests.

- **Green check:** Workflow completed successfully.
- **Red cross:** A workflow step failed; inspect its logs to identify the problem.

## Practical Steps

1. Created the Python prediction function.
2. Added unit tests.
3. Configured GitHub Actions.
4. Pushed code and verified a successful workflow run.
5. Observed a failed run during debugging, corrected the issue, and verified the successful run again.

## Conclusion

This practical demonstrates the basic CI process: write code, push changes to GitHub, run automated tests, troubleshoot failures, and verify the final successful workflow.

