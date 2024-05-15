# duqtalk

*Disclaimer: this program is in an early stage of development, so it has many assertions and rough edges.*

A CLI application to chat with DuckDuckGo AI (using Python and Selenium).

## Installation

Set up dependencies:

- `firefox` utility available in `PATH`
- `geckodriver` utility available in `PATH`
- `selenium` Python package

Then, simply fetch the `duqtalk` executable from this repo and run it (`duqtalk`).
If you're on Windows, `py -x path\to\duqtalk` should hopefully do the trick.

## Usage

Below invocation accepts raw textual lines and outputs responses as blocks of
raw text. If the terminal is a TTY, prints a simple `> ` prompt.

```bash
duqtalk
```

Below invocation is JSON mode. It accepts a line-by-line stream of JSON strings
and outputs also a stream of JSON string responses.

```bash
duqtalk --json
```

NOTE: Current implementation *cleans up the chat after each response* on the
browser side, so in practice there's no chat history context to drive a
conversation - each query & response pair is completely standalone. This may
change in future implementations.
