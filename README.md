
To build a local debug version of the Hermes CLI tools the following steps should get you started on macOS/Linux:

```shell
mkdir hermes_workingdir
cd hermes_workingdir
git clone https://github.com/facebook/hermes.git
cmake -S hermes -B build -G Ninja
cmake --build ./build
```

Or if you're using Windows, the following should get you going in a Git Bash shell:

```shell
mkdir hermes_workingdir
cd hermes_workingdir
git -c core.autocrlf=false clone https://github.com/facebook/hermes.git
cmake -S hermes -B build -G 'Visual Studio 16 2019' -A x64
cmake --build ./build
```

You will now be in a directory with the output of building Hermes into CLI tools. From here you can run a piece of JavaScript as follows:

```shell
echo "'use strict'; function hello() { print('Hello World'); } hello();" | ./bin/hermes
```

## Contributing

The main purpose of this repository is to continue to evolve Hermes, making it faster and more efficient. We are grateful to the community for contributing bugfixes and improvements. Read below to learn how you can take part in improving Hermes.

### Code of Conduct

Facebook has adopted a [Code of Conduct](./CODE_OF_CONDUCT.md) that we expect project participants to adhere to. Please read [the full text](https://code.fb.com/codeofconduct) so that you can understand what actions will and will not be tolerated.

### Contributing Guide

Read our [contributing guide](CONTRIBUTING.md) to learn about our development process, how to propose bugfixes and improvements, and how to build and test your changes to Hermes.

### License

Hermes is [MIT licensed](./LICENSE).
