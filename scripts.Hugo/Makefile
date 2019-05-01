all:

include Makefile.env

up:
	nice -n 19 git push -u origin master
e:
	vim Makefile.env
m:
	vim Makefile
gs:
	nice -n 19 git status
gc:
	nice -n 19 git commit -a
	

gd :
	nice -n 19 git diff

ga :
	nice -n 19 git add .

rg:regen
regen:
	[ -f config.toml ] && make regenX || make regenX -C scripts.Hugo 
regenX:
	rm -fr public/*
	cp ../CNAME public/
	[ -f public/CNAME ] || ( echo ; echo "why no CNAME ? exit" ; echo ; exit 32 )
	nice -n 19 hugo

s : server
server:
	[ -f config.toml ] && make serverX || make serverX -C scripts.Hugo 
serverX:
	nice -n 19 hugo server

# hddps://themes.gohugo.io/
# hddps://gohugo.io/themes/

