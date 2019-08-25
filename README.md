## Golinter

Golinter is a *fork* of golint (github.com/golang/lint). 
The only difference is that you can specify which linting mistakes to report.


## Installation

Golinter will install side-by-side with the official linter.
However, since they share the same codebase (Golinter being a fork of the linter) the default functionality
should be the same.

### go get
Golinter requires a
[supported release of Go](https://golang.org/doc/devel/release.html#policy).

    go get -u github.com/DylanMeeus/golinter

### from source

```
git clone github.com/DylanMeeus/golinter
cd golinter
go build && go install
```


## Usage

*If you're not familiar with go lint read the [documentation of
golint](https://github.com/golang/lint) first.*

Golinter let's you specify which linting mistakes to report back.
For a list of all flags, you can run `golinter -h`.

By default, all possible linting mistakes will be reported back. Thus, by default golinter will act
the same as golint.

But if we'd want to ignore blank imports and variable declaration errors we could tweak it:

> golinter -lint_vardecls=false -lint_blank_imports=false ./...


## Available flags

With the following flags you can control which errors to report back:

```
- lint_blank_imports
- lint_context_args
- lint_context_key_types,
- lint_elses
- lint_error_returns
- lint_error_strings
- lint_errorf
- lint_errors
- lint_exported
- lint_inc_dec
- lint_names
- lint_ranges
- lint_package_comments
- lint_receiver_names
- lint_time_names
- lint_unexported_return
- lint_vardecls
```

