# yii-grc-conf

[`grc`](https://github.com/garabik/grc) config to colorize Yii application.log 

## Installation

1. Install grc running `sudo apt-get install grc`

2. Copy `conf.yii` file to `~/.grc` directory (create if not exists)

3. Add to your `~/.grc/grc.conf` file (create if not exists) following lines:

```
# Yii log file
\btail\b.*\/(consoleapp|application)\.log\b
conf.yii
```

## Usage

Run `tail` using grc startup script:

```Shell
grc tail -F protected/runtime/application.log
```

or pipe `tail` output to `grcat` specifying path to `conf.yii`

```Shell
tail -F protected/runtime/application.log | grcat ~/.grc/conf.yii
```

## Links

* Generic Colourizer Home Page - http://kassiopeia.juls.savba.sk/~garabik/software/grc/README.txt
* Generic Colourize on Github - https://github.com/garabik/grc
* Yii Framework - http://www.yiiframework.com/