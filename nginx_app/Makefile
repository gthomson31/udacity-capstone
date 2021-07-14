## The Makefile includes instructions on environment setup and lint tests
# Dockerfile should pass hadolint
# app.py should pass pylint
# (Optional) Build a simple integration test

install:
	wget -O ./hadolint https://github.com/hadolint/hadolint/releases/download/v1.16.3/hadolint-Linux-x86_64 &&\
	chmod +x ./hadolint

lint:
	# See local hadolint install instructions:   https://github.com/hadolint/hadolint
	# This is linter for Dockerfiles
	./hadolint Dockerfile

	RESULT=$?
	if [ $RESULT -eq 0 ]; then
		echo "successfully linted dockerfile - proceeding to build image"
	else
		echo "failed to lint dockerfile - please fix and try again"
	fi

all: install lint 
