# Craft Parts

Craft-parts provides a mechanism to obtain data from different sources,
process it in various ways, and prepare a filesystem subtree suitable for
deployment. The components used in its project specification are called
*parts*, which can be independently downloaded, built and installed, and
also depend on each other in order to assemble the subtree containing the
final artifacts.


# License

Free software: GNU Lesser General Public License v3


# Documentation

https://canonical-craft-parts.readthedocs-hosted.com/en/latest/

# Contributing

A `Makefile` is provided for easy interaction with the project. To see
all available options run:

```
make help
```

## Development Environment

In order to develop any `apt` related items, the `python-apt` package is needed.
The `apt` extra will require this package in general. For development on an
Ubuntu system, the `focal-dev`, `jammy-dev`, and `lunar-dev` extras are available
instead, which will build a local `python-apt` package that matches the
declared Ubuntu version.

Apt package prerequisites for this development environment on an Ubuntu system can be installed with:

```bash
sudo apt install libapt-pkg-dev intltool fuse-overlayfs
```

## Running tests

To run all tests in the suite run:

```
make tests
```

## Adding new requirements

If a new dependency is added to the project run:

```
make freeze-requirements
```

## Verifying documentation changes

To locally verify documentation changes run:

```
make docs
```

After running, newly generated documentation shall be available at
`./docs/_build/html/`.


## Committing code

Please follow these guidelines when committing code for this project:

- Use a topic with a colon to start the subject
- Separate subject from body with a blank line
- Limit the subject line to 50 characters
- Do not capitalize the subject line
- Do not end the subject line with a period
- Use the imperative mood in the subject line
- Wrap the body at 72 characters
- Use the body to explain what and why (instead of how)
