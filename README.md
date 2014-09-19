# Emscripten

## Description

Provide a working [Emscripten]() environment including all dependencies.

## Usage

```yaml
- role: Emscripten
```

## Explicit Dependencies

- Nodejs Binary (`node`)
    - Using the [nvm]() role it is easy to ensure a nodejs environment is
      present.

## Configuration

*optional* `path`: Path to install the Emscripten environment is installed to.
(Default: `{{ ansible_env.HOME }}/Emscripten`).

*optional* `user`: username the install path belongs to (Default: 
`{{ ansible_env.USER }}`).

## Implicit Dependencies

- BuildEnvironment
- CMake
- Git
- Java

## Further Remarks

The Emscripten installation process needs to intially compile the Clang
compiler and afterwards compile the emscripten module with it. This takes
A LONG time. On my current macbook it takes about an hour. So be patient and
grab or coffee or something, while Emscripten is installing.
