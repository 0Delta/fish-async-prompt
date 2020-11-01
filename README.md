# fish-async-prompt

Make your prompt asynchronous in Fish shell.

## Description

![Demo Video](demo.png)

It runs `fish_prompt` and `fish_right_prompt` functions as another process and then, update the prompt asynchronously.

## Installation

With [fisher](https://github.com/jorgebucaran/fisher):

```
$ fisher add acomagu/fish-async-prompt
```

If your prompt doesn't work correctly, try changing the configuration.

## Configuration

### Variable: `async_prompt_inherit_variables`

Define variables inherited to prompt functions. Set `all` to pass all global variables.

**Default:** `status SHLVL CMD_DURATION`

### Variable: `async_prompt_functions`

Define functions replaced to run asynchronously. Usually one or both of `fish_prompt` and `fish_right_prompt`.

Other functions can be specified, but they must be called from `fish_prompt` or `fish_right_prompt` and arguments can't be passed.

**Default:** `fish_prompt fish_right_prompt`


**Default:** `fish_prompt fish_right_prompt`

### Function: `async_prompt_prehook`

Define a function to customize the pre-update prompt.

**Default:**

```
function async_prompt_prehook
  echo "*$argv"
end
```

## Author

[@0Delta](https://github.com/0delta)

## Special Thanks

- fish-async-prompt original creator [acomagu](https://github.com/acomagu)
