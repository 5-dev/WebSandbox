<div align="center">
  <img width="60" src="logo.png" alt="WebSandbox Logo" />
  <h1>Minimal Reproducible Examples</h1>
</div>

---

In general, we always prefer a **minimal, reproducible example** when looking at a bug report. A clear, reproducible bug report helps our maintainers pinpoint the issue quickly and deliver a fix. 

Here are a few things you can do to write the perfect example when you encounter an issue with WebSandbox.

### 1. Try Locally

If a project is not working as expected, it might be due to an incompatibility with WebSandbox or an environment issue. However, please do check that the project runs as expected on your local machine, with your Node installation. 

If it does run without issue locally, we are much more certain that it's a WebSandbox compatibility issue. For some types of issues (e.g., editor UI bugs), this verification might not make sense.

### 2. Isolate Faulty API Calls

WebSandbox does not cover the entire Node.js API perfectly yet. Most of the time, the underlying issue is a single API call that is not behaving properly. You might find the issue when trying some script or workflow in your favorite framework, but ideally, the reproduction example would be a **simple script with few or zero dependencies** that triggers the faulty API call immediately.

Remember that WebSandbox allows you to debug your code! If you open the DevTools panel, all your code plus your dependencies are there. You can also edit individual files and add `debugger` statements at will.

### 3. Read the Error

This is always good advice! But seriously, sometimes the error message will give you strong hints of what's going on. For instance, it might report that it did not find an executable file that is usually available on local environments, or that it attempted to run a shell script with features we don't support yet.
