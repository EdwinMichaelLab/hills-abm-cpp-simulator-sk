# hillsborough_fl_simulator-skim

# Modified City-Scale epidemic simulator (for Hillsborough County Florida USA)

There are three(3) main components:
* [Synthetic Population Generation](staticInst/)
* [C++ simulator](cpp-simulator/)
* [Web / Javascript simulator](simulator/)

## `StaticInst/` - Generates static files to instantiate a city based on Demographics data
The first stage of the simulator workflow is to generate static information required to instantiate a city.  To get the necessary options to instantiate the city:

```
> python CityGen.py -h
usage: CityGen.py [-h] [-n N] [-i I] [-o O] [--validate] [-s S]

Create mini-city for COVID-19 simulation

optional arguments:
  -h, --help  show this help message and exit
  -n N        target population
  -i I        input folder
  -o O        output folder
  --validate  script for validation plots on
  -s S        [for debug] restore random seed from folder
```

An example run, to generate a version of Hillsborough County(FL, USA), would be the following:
```
> python CityGen.py -n 1459762 -i data/base/hillsborough_fl -o data/hills_1.45M
```

A detailed description of the input files, the script and instructions to run are available at [`staticInst/README.md`](staticInst/README.md)


## `cpp-simulator/` - CPP simulator
This folder contains the cpp-version of the simulator. The CPP simulator evolved from the JS simulator. 
Please read the  [`cpp-simulator/README.md`](cpp-simulator/README.md) for more details.

# This is the modified for our academic research form here:
[CNI-IISC Epidemic Simulator](https://github.com/cni-iisc/epidemic-simulator)
