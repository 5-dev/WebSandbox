# Useful Bug Reports for WebSandbox issues

In general, we always prefer a **minimal, reproducible example** when looking at a bug report. Here are a few things you can do to write the perfect example when you encounter an issue with WebSandbox.

## Try Locally

If a project is not working as expected, it might be due to an incompatibility with WebSandbox. However, please do check that the project runs as expected in your local machine, with your Node installation. If it does run without issue locally, we are much more certain that we might be after a WebSandbox compat issue.

## Read the Error

This is always good advice! But seriously, sometimes the error message will give you strong hints of what's going on. For instance, it might report that it did not find an executable file that it's usually available on local environments, or that it attempted to run a shell script with features we don't support yet.
