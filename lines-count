#!/usr/bin/env python

import os, sys

def main(excludes):
	lines = 0
	for root, dirs, files in os.walk(os.getcwd()):
		for exclude in excludes:
			if exclude in dirs:
				dirs.remove(exclude)
		
		for name in files:
			if name[0] != ".":
				f = open(os.path.join(root, name), "r")
				for line in f:
					lines = lines + 1

	return lines

if __name__ == "__main__":
	print "start counting"
	print main(sys.argv[1:])