a way to give variables into a running process


example:
nginx
setup cookbook
in each file bunch of default settings
makes one big document with a key: nginx, values are the settings in file
these can all be overwritten , it's all just values in a json file
anything we write in the UI will overwrite whatever it is in the file.
( * )


( * ) aside: node = the big json document



Our setup file is going to be just a bunch of other peoples cookbooks
downloading the required files is most of the work and its already been done

intit.d
runs process for you, if it fails run it again
service that on boot runs process for you
if you need it google "intit.d service template"



deploy.rb
