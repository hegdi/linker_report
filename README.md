# Binary Size Analysis
This repository is used to generate interactive linker statistics and revive the former repo. Please have a look at our [interactive example](https://hegdi.github.io/linker_report/).

## Installation

Then clone the tool to a local directory
```bash
git clone https://github.com/hegdi/linker_report
```
This will use GNU `nm` from your selected toolchain. The toolchain can be selected by setting `nm` accordingly in `config.py`.
To customise your target further you can change the color mappings in `sequences.js`.

## Running the Analysis

### Symbol level analysis - gcc compiler

Now run the ELF linker statistics tool:
```bash
# Process Data: provide one or more elf files for analysis
> elfsize.py -i <your file>.elf -b
```
This will open up a browser page automatically with the visualisation.

## Advanced usage
### More Options
```
> elfsize.py -h
usage: elfsize.py [-h] -i [BINARY [BINARY ...]] [-o OUTPUT] [-b]

Analyse binary built by gcc and generate json containing binary size
information

optional arguments:
  -h, --help            show this help message and exit
  -i [BINARY [BINARY ...]], --binary [BINARY [BINARY ...]]
                        path to the binary. You can also specify multiple
                        binaries: -i <path1> <path2>
  -o OUTPUT, --output OUTPUT
                        path of output json, defaults to
                        /Users/leozhou/projects/mbed-os-linker-report/html
                        /data-flare.js, default filename to data-flare.js if a
                        folder is specified
  -b, --browser         launch the pie chart visualisation in a browser
```

## Example Output
Below you can find an example screenshot of our tool. Please have a look at our [interactive example](https://hegdi.github.io/linker_report/), too.
![d3.js based ELF Linker Statistics](docs/example.png)
