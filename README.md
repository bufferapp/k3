# Firehoser

[![license](https://img.shields.io/github/license/mashape/apistatus.svg)]()
[![PyPI version](https://badge.fury.io/py/firehoser.svg)](https://badge.fury.io/py/firehoser)

Command line tool that automates the setup of a lambda function that fowards records from Kinesis to Firehose.

## Installation

To install Firehoser, simply:

```
pip install firehoser
```

## Usage

Firehoser relies in [`boto3` credentials configuration][credentials] so you should have AWS credentials and a region properly configured.

### Link

Create a new Lambda function that forwards events from `[kinesis-stream-name]` to `[firehose-stream-name]`. It will also creates the required roles and policies.

```bash
firehoser link [kinesis-stream-name] [firehose-stream-name]
```

### Unlink

Destroy function created with `firehoser link`.

```bash
firehoser unlink [kinesis-stream-name] [firehose-stream-name]
```

[credentials]: https://boto3.readthedocs.io/en/latest/guide/configuration.html

## Contributing

Feel free to open issues or submit pull requests with bug fixes or changes. All kind of contributions welcome!
