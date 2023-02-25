# i3blocks-course
An `i3blocks' script to display your current class status in i3 bar.

More features to come.

## How does it get information about my courses?
Write down your course metadata in a yaml file in a structure like this:

``` yaml
compstr:
  fullname: 计算机组成与体系结构
  abbrev: 计组
  time: [[Wed, 8:00, 10:40, H3108], [Thu, 16:20, 18:00, H2101]]
  path: /path/to/your/course1/folder

crypto:
  fullname: 密码学基础
  abbrev: 密码
  time: [[Wed, 8:00, 10:40, H3108]]
  path: /path/to/your/course2/folder
```

and its path is specified using the `fmetadata` variable.

The `time` field should be an array of one or multiple four element array,
which includes the day of the week, start time, end time,
and classroom number, in that order.

## How do I use it?
You may symlink or copy the `course` file under your `$SCRIPT_DIR`, which is specified in
your i3blocks config.

then add a segment in your i3blocks config:

``` ini
[course]
command=$SCRIPT_DIR/course
label=
interval=60
```

`label` is a string that displays before the program output.

`interval` is a number of seconds between each running of the script.

If you have Emacs and Emacs client installed AND you are currently in
a class, you could right-click on the botton and an `emacsclient`
frame will popup with a Dired buffer of the directory for your current
class (the `path`), then you could navigate in it to open your notes,
slides etc. that was stored in that directory.

## How do I contribute?
Issues and pull requests always welcome.

## Why is your code so ugly and has wierd spaces?
I write Lisps from time to time and that's just my aesthetic of clear code.

## What license does it use?
This program is free software, it uses GPLv3+.
