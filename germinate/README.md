germinate
=========
Process template files (aka seeds) to create files.

Originally developed so that a quick default file for a variety of
programming languages could be created.

Seeds are searched for in /usr/share/germinate/seeds and
$HOME/.config/germinate/seeds (or XDG_CONFIG_HOME if set). Seeds found
under the HOME directory will be preferred over seeds found in /usr/share.

The seeds are written in the Template Toolkit templating language.
http://template-toolkit.org/
For the seed templates, the "star" tag style is used. This allows other
styles to be embedded so that you can create a template of a template.

You can customize the values that populate a seed when germinated in two
ways. You can put constants in a configuration file or you can supply
key=value pairs on the commandline. The file for constants is at
$XDG_CONFIG_HOME/germinate/config.yaml. A sample configuration file is
provided. Key-value pairs can also be supplied on the command line. Pass as
many KEY=VALUE parameters as needed and they will be available in the
seeds.

Requires the following Perl modules:
* YAML
* Template Toolkit
* Date::Format
* Getopt::Std


Usage
-----

	Usage:	germinate [ -l | -y ] | -s seed [ KEY=VALUE ]* [ -o output-file ] [ -c config-file ]
		-l: list available seeds 
		-y: list available seeds as YAML
		-s: seed to germinate
		-o: output file (Default: STDOUT)
		-c: configuration file (Default: $HOME/.germinate/config.yaml)
		KEY=VALUE: Used while processing a seed
		         : These overwrite keys listed in config file
		         : The date of germination is always available in the DATE key.

