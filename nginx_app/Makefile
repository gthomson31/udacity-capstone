## The Makefile includes instructions on environment setup and lint tests
# Dockerfile should pass hadolint
# app.py should pass pylint
# (Optional) Build a simple integration test

install:
	apt-get update
	apt-get install tidy -y
	apt-get install wget -y
	wget -O ./hadolint https://github.com/hadolint/hadolint/releases/download/v1.16.3/hadolint-Linux-x86_64 &&\
	chmod +x ./hadolint


lint:
	# See local hadolint install instructions:   https://github.com/hadolint/hadolint
	# This is linter for Dockerfiles
	hadolint -v
	hadolint --ignore DL3006 Dockerfile
	tidy -q -e *.html



all: install lint 
