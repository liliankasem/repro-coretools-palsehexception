# repro-coretools-palsehexception

- [GH issue](https://github.com/Azure/azure-functions-core-tools/issues/4158)

Issue occurs on MacOS M1/M3 (arm) devices on version `v4.0.6594` of core tools.

Exception:

`terminate called after throwing an instance of 'PAL_SEHException'`

## Steps to reproduce

1. Clone the repo
1. Run `docker-compose up`
1. Double check the core tools version being used in the container

#### Last working version

The issue did not occur on `v4.0.6280`. Update line 24 in the docker-compose file to see the last working version:

`npm install -g azure-functions-core-tools@4.0.6280`
