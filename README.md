# DVC 1.0 no-auto-commit examlpe

Usage:
1. Change code or params, commit all the changes localy.
2. Kick off the CI/CD action job: `git push`.
3. Wait until CI/CD action is done.
4. (if training result is not good go back to 1) Bring the result to a local machine: `dvc pull --run-cache` and `dvc repro`
5. Add and commit all the new changes
6. Got to step 1 until the model is not good enough.

Note, you need to use `--run-cache` option for `dvc pull` and `dvc push` to manage the run-cache. The same way you need to pull\push on the CI/CD workflow.
