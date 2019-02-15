SOP and reference for [Travis CI](https://travis-ci.com/) setup.

* [x] Enable Travis from https://github.com/marketplace/travis-ci
* [x] Go https://travis-ci.com/yakshaveinc/travis and hit the badge to steal it
* [x] Insert the badge [![Build Status](https://travis-ci.com/yakshaveinc/travis.svg?branch=master)](https://travis-ci.com/yakshaveinc/travis)

![No builds](no_travis.png)

### Create .travis.yml

* [x] [Empty .travis.yml](https://travis-ci.com/yakshaveinc/travis/builds/101078477)
starts **default job** in Ruby environment.

![Empty No builds](empty_travis.png)

* [x] `script: skip` stops Ruby environment from failing ([build #4](https://travis-ci.com/yakshaveinc/travis/builds/101115865))
```yaml
script: skip
```

* [ ] `language: minimal` switches from Ruby to [alternative environment](https://docs.travis-ci.com/user/languages/minimal-and-generic/) without default scripts
```yaml
language: minimal
```

Using invalid language like [`language: none`](https://travis-ci.com/yakshaveinc/travis/jobs/178150572) or
[misspelled](https://travis-ci.com/yakshaveinc/travis/jobs/178155333) will default to Ruby without any errors.
