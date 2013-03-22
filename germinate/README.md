germinate
=========

Process template files (aka seeds) to create any kind of file you need.
Originally developed so that a quick default file for a variety of programming
languages could be created.

Uses the Template Toolkit template language.
http://template-toolkit.org/

Requires the following Perl modules:
* YAML
* Template Toolkit
* Date::Format
* Getopt::Std



Usage:	germinate [ -l | -y ] | -s seed [ KEY=VALUE ]\* [ -o output-file ] [ -c config-file ]
	-l: list available seeds 
	-y: list available seeds as YAML
	-s: seed to germinate
	-o: output file (Default: STDOUT)
	-c: configuration file (Default: $HOME/.germinate/config.yaml)
	KEY=VALUE: Used while processing a seed
	         : These overwrite keys listed in config file
	         : The date of germination is always available in the DATE key.

