# Change Log

## [1.0.9] 2025-04-01
### Changes

- Update RM (minor)

## [1.0.8] 2023-10-07
### Changes

- Update Dependencies
- Silent fallback to SQLite
- CI/CD for Render

## [1.0.7] 2022-06-01
### Improvements

- Built with [CoreUI Generator](https://appseed.us/generator/coreui/)
  - Timestamp: `2022-06-01 09:08`

## [1.0.6] 2022-01-16
### Improvements

- Bump Flask Codebase to [v2stable.0.1](https://github.com/app-generator/boilerplate-code-flask-dashboard/releases)
- Dependencies update (all packages) 
  - Flask==2.0.2 (latest stable version)
  - flask_wtf==1.0.0
  - jinja2==3.0.3
  - flask-restx==0.5.1
- Forms Update:
  - Replace `TextField` (deprecated) with `StringField`

## [1.0.5] 2021-12-03
### Improvements

- Bump UI: CoreUI v4.1.0

## [1.0.4] 2021-11-09
### Improvements

- Bump Codebase: [Flask Dashboard](https://github.com/app-generator/boilerplate-code-flask-dashboard) v2.0.0
  - Dependencies update (all packages) 
    - Flask==2.0.1 (latest stable version)
- Better Code formatting
- Improved Files organization
- Optimize imports
- Docker Scripts Update
- Gulp Tooling  (SASS Compilation)
- Fix **ImportError: cannot import name 'TextField' from 'wtforms'**
  - Problem caused by `WTForms-3.0.0`
  - Fix: use **WTForms==2.3.3**

## [1.0.3] 2021-05-16
### Dependencies Update

- Bump Codebase: [Flask Dashboard](https://github.com/app-generator/boilerplate-code-flask-dashboard) v1.0.6
- Freeze used versions in `requirements.txt`
    - jinja2 = 2.11.3

## [1.0.2] 2021-03-18
### Improvements

- Freeze used versions in `requirements.txt`
    - flask_sqlalchemy = 2.4.4
    - sqlalchemy = 1.3.23

## [1.0.1] 2020-06-08 
### Improvements

- Bump the Core UI Kit to v3.2.0
- Update the code-base to use latest [Flask Boilerplate](https://github.com/app-generator/boilerplate-code-flask-dashboard)
- Update Licensing information
- Add CHANGELOG.md to track all changes

## [1.0.0] 2020-01-01
### Initial Release
