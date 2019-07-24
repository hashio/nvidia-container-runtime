# Copyright (c) 2017-2018, NVIDIA CORPORATION. All rights reserved.

DOCKER ?= docker

GOLANG_VERSION := 1.10.3

.NOTPARALLEL:
.PHONY: all

all: ubuntu18.04 ubuntu16.04 ubuntu14.04 debian9 debian8 centos7 amzn2 amzn1 opensuse_leap15.0 sles12sp3

ubuntu%: $(CURDIR)/Dockerfile.ubuntu
	$(DOCKER) build --build-arg VERSION_ID="$*" \
	                --build-arg GOLANG_VERSION="$(GOLANG_VERSION)" \
	                -t "nvidia/base/ubuntu:$*" -f Dockerfile.ubuntu .

debian%: $(CURDIR)/Dockerfile.debian
	$(DOCKER) build --build-arg VERSION_ID="$*" \
	                --build-arg GOLANG_VERSION="$(GOLANG_VERSION)" \
	                -t "nvidia/base/debian:$*" -f Dockerfile.debian .

centos%: $(CURDIR)/Dockerfile.centos
	$(DOCKER) build --build-arg VERSION_ID="$*" \
	                --build-arg GOLANG_VERSION="$(GOLANG_VERSION)" \
	                -t "nvidia/base/centos:$*" -f Dockerfile.centos .

amzn%: $(CURDIR)/Dockerfile.amzn
	$(DOCKER) build --build-arg VERSION_ID="$*" \
	                --build-arg GOLANG_VERSION="$(GOLANG_VERSION)" \
	                -t "nvidia/base/amzn:$*" -f Dockerfile.amzn .

opensuse_leap%: $(CURDIR)/Dockerfile.opensuse_leap
	$(DOCKER) build --build-arg VERSION_ID="$*" \
	                --build-arg GOLANG_VERSION="$(GOLANG_VERSION)" \
	                -t "nvidia/base/opensuse/leap:$*" -f Dockerfile.opensuse_leap .

sles%: $(CURDIR)/Dockerfile.sles
	$(DOCKER) build --build-arg VERSION_ID="$*" \
	                --build-arg GOLANG_VERSION="$(GOLANG_VERSION)" \
	                -t "nvidia/base/suse/sles:$*" -f Dockerfile.sles .
