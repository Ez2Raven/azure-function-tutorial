# Coding Guidelines and Emphasis

* Don't use console.log to write trace outputs. Use context.log

> Because output from console.log is captured at the function app level, it's not tied to a specific function invocation and isn't displayed in a specific function's logs. Also, version 1.x of the Functions runtime doesn't support using console.log to write to the console.

* Trace logs should always include invocationId for log filtering

> Logs entries are usually written to a centralized log file, sequence to log entries are not guaranteed.

* Consider defining a package.json in the folder of a specific function if a version conflict arises

> You should define a package.json file at the root of your Function App. Defining the file lets all functions in the app share the same cached packages, which gives the best performance. If a version conflict arises, you can resolve it by adding a package.json file in the folder of a specific function.

* There is coupling between Azure Functions Core version and Node version for local development.

## Additional tools and plugins

* <https://github.com/Azure/azure-functions-core-tools#linux>

## Reference

* <https://learn.microsoft.com/en-us/azure/azure-functions/functions-reference-node>
* Configure vscode to use azure function core - <https://learn.microsoft.com/en-us/azure/azure-functions/functions-versions?tabs=v4&pivots=programming-language-csharp>
* Install azure function core - <https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=v4%2Clinux%2Ccsharp%2Cportal%2Cbash>
* NodeJs unit testing - <https://github.com/Azure-Samples/azure-functions-unit-testing-mocha/blob/master/walkthrough.md>
