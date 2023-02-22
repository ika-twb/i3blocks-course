# i3blocks-course
An `i3block' script to display your current class status in i3bar.

More features to come.

## How does it read data of my courses?
Write down your course metadata in a yaml file like this:

``` yaml
compstr:
  fullname: 计算机组成与体系结构
  abbrev: 计组
  time: [[Mon, 8:00, 10:40], [Fri, 16:20, 18:00]]
  path: /path/to/your/course1/folder

crypto:
  fullname: 密码学基础
  abbrev: 密码
  time: [[Wed, 8:00, 10:40], [Thu, 16:20, 18:00]]
  path: /path/to/your/course/folder
```

and it's path is specified using the `fmetadata` variable.

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

## How do I contribute?
Issues and pull requests always welcome.

## What license does it use?
This program is free software, it uses GPLv3+.
