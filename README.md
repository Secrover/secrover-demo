# Secrover Daily Scan

This repository runs a **daily security scan** using [Secrover](https://github.com/secrover/secrover) via Docker, managed automatically by [GitHub Actions](https://docs.github.com/en/actions).

## What It Does

- Pulls and runs the `secrover/secrover` Docker container every day at 03:00 UTC.
- Uses the local `config.yaml` and Github env vars for configuration.
- Outputs scan results into the [`output/`](output/) folder.
- Commits any updated results automatically to the repository.

## Output

You can view the latest scan result here:

👉 [output/index](output/index)

> Note: The `output/` folder is committed to the repository daily, so you can track changes and view historical reports via Git history.

## Configuration

- `Github env vars`: Environment variables passed to the Docker container.
- `config.yaml`: The main configuration file for Secrover.

## GitHub Actions Workflow

The workflow is defined in [`.github/workflows/secrover.yml`](.github/workflows/secrover.yml) and is triggered:
- **Automatically** every day.
- **Manually** via the GitHub UI ("Run workflow").

---

Feel free to fork this repository or customize it for your own security automation needs.
