make apache run on startup (centos):
  chkconfig --level 2345 httpd on

check what user apache runs as:
  ps aux | egrep '(apache|httpd)'