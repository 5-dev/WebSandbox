# Useful Bug Reports for WebSandbox issues

In general, we always prefer a [minimal, reproducible example](https://stackoverflow.com/help/minimal-reproducible-example) when looking at a bug report. Here are a few things you can do to write the perfect example when you encounter an issue with WebSandbox.

## Try Locally

If a project is not working as expected, it might be due to an incompatibility with WebSandbox. However, please do check that the project runs as expected in your local machine, with your Node installation. If it does run without issue locally, we are much more certain that we might be after a WebSandbox compat issue.

For some types of issues, it might not make sense to perform this verification, e.g. if you have an issue with the editor.

## Auto-execute Erroneous Command

We always ask you to include a link to a sandbox that shows the erroneous behavior. You can make things even easier to reproduce if you configure it so the command that triggers the error is run automatically on start. You can do that by including a custom `websandbox.json` configuration file.

## Isolate Faulty API Calls

WebSandbox does not cover the whole Node.js API perfectly yet, so most of the times the underlying issue is a single API call that is not behaving properly. You might find the issue when trying some script or workflow in your favorite framework, but ideally the reproduction example would be a simple Node.js script, with few or even no dependencies at all, that triggers the faulty API call immediately.

Remember that WebSandbox allows you to debug your code! If you open the DevTools panel, all your code plus all your dependencies are there. You can also edit individual files and add `debugger` statements at will. It's almost magical!

## Read the Error

This is always good advice! But seriously, sometimes the error message will give you strong hints of what's going on. For instance, it might report that it did not find an executable file that it's usually available on local environments, or that it attempted to run a shell script with features we don't support yet.
