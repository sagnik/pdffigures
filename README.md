pdffigures
==========
pdffigures is a command line tool that can be used to extract figures, tables, and captions from scholarly documents. See the [project website](http://pdffigures.allenai.org).

### Usage
1. Compile the command line tools:

```make DEBUG=0```

2. Run on a new PDF document and display the results:

```pdffigures -f /path/to/pdf```

See ```pdffigures -help``` for a list of additional command line arguements.

### Dependencies
pdffigures requires [leptonica](http://www.leptonica.com/) and [poppler](http://poppler.freedesktop.org/) to be installed. On MAC both of these dependencies can be installed through homebrew:

```brew install leptonica poppler```

On Ubuntu 14.04 these dependencies can be installed through apt-get:

```sudo apt-get install libpoppler-dev libleptonica-dev```

On Ubuntu 15.04:

```sudo apt-get install libpoppler-private-dev libleptonica-dev```

pdffigures has been tested with poppler 3.0,3.4,3.7, although I expect most other versions to be compatible, and leptonica 1.72

pdffigures uses std::regex, therefore compiling on Ubuntu requires g++ >= 4.9

You might have multiple poppler.pc in your computer. On my `Ubuntu 15.10`, one was in `/usr/lib/x86_64-linux-gnu/pkgconfig/` and one was in `/usr/local/lib/pkgconfig/`. Make sure to choose the appropriate one (by adding the appropriate path to the `PKG_CONFIG_PATH` variable in your `bahrc`. ) 

### Support
pdffigures has been tested on MAC OS X 10.9 and 10.10, Ubuntu 14.04, 15.04 and 15.10 (64 bit), Windows is not supported.
