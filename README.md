# Fast RSA Engine for jruby-openssl gem

[![Build Status](https://travis-ci.org/lookout/fast-rsa-engine.svg?branch=master)](https://travis-ci.org/lookout/fast-rsa-engine)

This gem replaces the RSA signature and RSA ciphers from jruby-openssl by the much faster implementation of them. See [corner.squareup.com/2014/02/faster-rsa-jnagmp.html](https://corner.squareup.com/2014/02/faster-rsa-jnagmp.html)

but this works only for **darwin** and **linux-x84_64** platforms due to the library used from squareup.

The improvement in performance brings JRuby verify and decrypy using RSA close to MRI.

## installation

via rubygems
```
gem install fast-rsa-engine
```
or add to your Gemfile
```
gem 'fast-rsa-engine'
```

installing the gem also takes care of the jar dependencies with jruby-1.7.16+

## usage

with bundler its auto-require magic will be sufficient. otherwise just

    require 'fast-rsa-engine'

## running the benchmark

    ruby benchmark/benchmark-with-fast-rsa.rb

or
    ruby benchmark/benchmark-with-builtin-rsa.rb

## developement

Get all the gems and jars in place.
    
    
    bundle install

Build jar and run all specs.

    bundle exec rake

## meta-fu

enjoy :)
