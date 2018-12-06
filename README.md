# For users

To install the conda packages maintained in this repository do
`conda install -c astropy package_name`

If you use this channel frequently it may be convenient to add the conda
channel for this repository to your list of default channels:

```
conda config --add channels astropy
```

# For maintainers/contributors

## Dependencies

This packages uses `extruder`, available on GitHub at
[astropy/conda-build-tools](https://github.com/astropy/conda-build-tools) or installable
with: `conda install -c astropy extruder`.

## Updating an existing package to a new version

Edit the version number in `requirements.yml`: by far the easiest way is to
open [`requirements.yml`](requirements.yml) in GitHub, click the pencil icon
to edit it, and create a pull request to make the change.

## Adding a new package

First try adding the new package to `requirements.yml`. If the build based on
that fails you will need to write a recipe for it, then do some minor editing
to convert it to a template.

Check out the
[home page for the builder](https://github.com/astropy/conda-build-tools)
for a description of the permitted fields in `requirements.yml` and a sample recipe template.

## In case of emergency, copy manually

First install `anaconda-client`. Once you have done that, use it to log in to anaconda at
the command line:

```
$ anaconda login
```

Once you are logged in you can do the copy from the command line:

```
$ anaconda copy --to-owner astropy conda-forge/astroquery/0.3.9
```

If you want to copy just one specific file from conda-forge add its name after
the version number. See `anaconda copy --help` for details.
