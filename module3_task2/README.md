# Awesome Inc. website Docs

* Welcome to our site, please follow the next information
  in order to have a working website.

## how to install hugo

* sudo apt update -> upgrade
* wget `https://github.com/gohugoio/hugo/releases/download/v0.109.0/hugo_extended_0.109.0_linux-amd64.deb`
* sudo `dpkg -i hugo_extended_0.109.0_linux-amd64.deb`
* hugo version
* hugo v0.109.0-47b12b83e636224e5e601813ff3e6790c191e371+extended
  linux/amd64 BuildDate=2022-12-23T10:38:11Z VendorInfo=gohugoio

## Prerequisites

* A Valid Go-Hugo website is provided
* There are no Git Submodules
* The theme ananke is installed
* No directory dist/ committed
* Makefile present

## Lifecycle

* build
* clean
* post
* help

## Build Workflow

* The workflow is executed into Ubuntu 18.04 environment
* Required tools are installed prior to any make target,
  by executing the script setup.sh
