# Change Log

All notable changes to this project will be documented in this
file. This file is structured according to http://keepachangelog.com/

- - -

Unreleased
----------
- Add `category` field to `Person.age`

## [1.7.0] - 2015-02-10
### Added
- Add `sl` country code to validation pattern for Person.address


## [1.6.0] - 2015-01-29
### Added
- `EbolaCallCentreUser` schema
- Person schema
  - `phone` property in sources
  - `interviewer` moved to `connectedPerson` to be re-usable
  - `relative` of source case, is a `connectedPerson`
  - `red_eyes` and `other_symptoms` as accepted symptoms
### Changed
- Person schema
  - `interviewer` is of type `connectedPerson`
  - `leader` is of type `connectedPerson`

## [1.5.0] - 2015-01-15
### Added
- `leader` property in a case management `Person` schema
- `city` property in a case management `Person` schema
- `exposure` property in sources within a `Person` schema

## [1.4.0] - 2015-01-08
### Changed
- specify the possible values for `case.contact.callNature`
- `case.contact.callNature` is now required

I am not marking this as a breaking change, in the belief that our
data is already compliant to the new schema

## [1.3.2] - 2015-01-05
### Changed
- removed the `call` model, now merged with the `case` model, which
  represented the same type of documents. technically a breaking
  change, but the `call` model is not used anywhere
- `contact` is now mandatory in a case. all known components are
  already writing it

## [1.3.1] - 2015-01-05
### Fixed
- updated the distribution files

## [1.3.0] - 2015-01-05
### Added
- `call` schema

## [1.2.3] - 2014-12-23
### Added
- Add 'mg' as allowed contry code

## [1.2.2] - 2014-12-19
### Added
- Product storage attribute

## [1.2.1] - 2014-12-19
### Fixed
- distribution files *actually* exposing the model as a global variable

## [1.2.0] - 2014-12-19
### Added
- distribution files exposing the validator as a global variable

## [1.1.0] - 2014-12-18
### Added
- id and name properties in Person.contact.sourceCases. This would be
  a breaking change but that software is not in production yet
