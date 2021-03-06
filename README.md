## AWS CloudFormation Resource Provider Java Plugin

The CloudFormation CLI (cfn) allows you to author your own resource providers that can be used by CloudFormation.

This plugin library helps to provide Java runtime bindings for the execution of your providers by CloudFormation.

Usage
-----

If you are using this package to build resource providers for CloudFormation, install the [CloudFormation CLI Java Plugin](https://github.com/aws-cloudformation/cloudformation-cli-java-plugin) - this will automatically install the the [CloudFormation CLI](https://github.com/aws-cloudformation/cloudformation-cli)! A Python virtual environment is recommended.

```shell
pip3 install cloudformation-cli-java-plugin
```

Refer to the documentation for the [CloudFormation CLI](https://github.com/aws-cloudformation/cloudformation-cli) for usage instructions.

Development
-----------

For changes to the plugin, a Python virtual environment is recommended. Check out and install the plugin in editable mode:

```shell
python3 -m venv env
source env/bin/activate
pip3 install -e /path/to/cloudformation-cli-java-plugin
```

You may also want to check out the [CloudFormation CLI](https://github.com/aws-cloudformation/cloudformation-cli) if you wish to make edits to that. In this case, installing them in one operation works well:

```shell
pip3 install \
  -e /path/to/cloudformation-cli \
  -e /path/to/cloudformation-cli-java-plugin
```

That ensures neither is accidentally installed from PyPI.

Linting and running unit tests is done via [pre-commit](https://pre-commit.com/), and so is performed automatically on commit after being installed (`pre-commit install`). The continuous integration also runs these checks. Manual options are available so you don't have to commit:

```shell
# run all hooks on all files, mirrors what the CI runs
pre-commit run --all-files
# run unit tests only. can also be used for other hooks, e.g. black, flake8, pylint-local
pre-commit run pytest-local
```

License
-------

This library is licensed under the Apache 2.0 License.
