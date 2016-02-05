# Edit The Launch Date & Time

There is a single definition of the next launch in the file `_data/launch.yml`
which looks like this:

```yaml
launch: 2016-07-31T17:00:00
certainty: TBD
name: Launch-13
link: https://github.com/psas/Launch-13
patch: http://psas.pdx.edu/Launch-12/patch/L12_patch.svg
```

Simply edit the values appropriately (from right in github if you want) and the
site will auto do everything.

 - `launch` ISO 8601 format **In UTC** date string for the exact time of launch
 - `certainty` Launch date certaintiy. Valid values for certainty:
    - `TBD` (To Be Decided) We're not sure
    - `NET` (No Earlier Than). Soft-pick a day for the launch. Might change
    - `Date` Launch day scheduled firmly
    - `Time` We have a target time picked out too
 - `name` What we're calling the launch
 - `link` URL to the launch info page, usually github repo
 - `patch` URL to patch artwork
