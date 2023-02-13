# Go2 Error Handling Feedback

ref https://github.com/golang/go/wiki/Go2ErrorHandlingFeedback

# Suggestions for the `handle` section of the new Go2 error handling proposal

1. Provide access to the __line number__ of the `check` statement (i.e. the equivalent of the old C \_\_LINE\_\_ directive)
2. Provide access to the source code __filename__ (i.e. "my_code.go")
3. Provide access to a __tag__ value associated with the build (e.g. 'go build' could accept a "tag" option, which could be used to version the build)


## Context of the above suggestion

There are many proposals that address the error handling issue of Go2 at the "function level".

The above suggestion is more focused on the "high level" issue of error handling -- the problem of how to "scale to large code bases and large developer efforts."

Many reported errors are easy to diagnose and remedy __IF__ the developer can locate the correct line of code, in the correct source file, of the correct version __AND__ (sometimes important) within the timeframe that the problem condition still exists.

For illustration, if given a stark choice between: __(#1)__ the line number, source filename, and code version, but NO error code or message, versus __(#2)__ an error code and message, but no precise location, it may be preferred by many developers to have #1, rather than #2!

**.**
