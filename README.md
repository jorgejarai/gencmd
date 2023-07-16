# `gencmd`

A command line tool that leverages the OpenAI API to generate shell commands based on a prompt.

## Installation and usage

This tool requires Python 3.x and an OpenAI API key. You can get one [here](https://platform.openai.com/). The key should be stored in an environment variable called `OPENAI_API_KEY`. You can set this variable in your shell's configuration file (e.g. `.bashrc` or `.zshrc`).

Before you can use the tool, you must install the dependencies. You can do this by running the following command:

```console
$ pip install -r requirements.txt
```

You can install this script by copying it to a directory in your `$PATH` and making it executable. For example:

```console
$ cp gencmd.py ~/.local/bin/gencmd
$ chmod +x ~/.local/bin/gencmd
```

Once the API key is set, you can run the program like so (quotes are optional):

```console
$ gencmd 'List all files in the current directory and sort them by size.'
```

The program will then generate a command based on the prompt and ask for confirmation. If you confirm, the command will be copied to your clipboard. You can then paste it into your terminal.

```console
$ gencmd 'List all files in the current directory and sort them by size.'
Command: ls -S
Do you want to copy the command to the clipboard? [Y/n]: y
$
```

# API costs

Generating commands with this tool costs money, since it uses the OpenAI API (specifically the `gpt-3.5-turbo` model). The cost depends on the length of the prompt. The longer the prompt, the more it costs. You can find the current prices [here](https://openai.com/pricing).
