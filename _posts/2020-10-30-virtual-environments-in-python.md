---
layout: post
title: Virtual environments in Python
date: 2020-10-30 
categories: python
---


## What's a virtual environment?

A virtual environment is an isolated python environment where you can install packages that are separated from other environments or globally installed packages. 

## Why use a virtual environment?

Most Python applications will likely have several packages and dependencies outside the standard package.

Imagine you have project A that uses package 1 with version 1.4. And you have another project B that uses the same package 1 but with version 2.0. It will become difficult to maintain these two projects since they have conflicting dependencies.  

This is were virtual environments come it handy.

A virtual environment allows us to have an environment where packages are isolated in a project and are unaffected by any other projects even if they use the same packages/dependencies.

## Using virtualenv

We will be using a tool called `virtualenv` to create our virtual environment.

To install virtualenv, run the following command: 

```bash
pip3 install virtualenv
```

To create a new virtual environment, go to your project's directory and run the following command.

```bash
virtualenv venv
```

This will create a new virtual environment in your current directory with the name `venv`.

You can also specify the python version using the `-p` tag.

```bash
 virtualenv venv -p python3.8
```

To activate our new virtual environment, run the following command.

If you're on linux or macOS:

```bash
source venv/bin/activate
```

On windows: 

```bash
\venv\Scripts\activate
```

After activating the environment, your shell will show the name of the environment on the left.

Now any packages you install using pip will be available only inside this virtual environment.

To view all installed packages in our virtual environment, run `pip list`.

### To deactivate a virtual environment:

On Linux and macOS:

```bash
source venv/bin/deactivate
```

On Windows:

```bash
\venv\Scripts\deactivate
```

  

Thats it. Thanks for reading! 

If you find any mistakes in is article, please let me know.
