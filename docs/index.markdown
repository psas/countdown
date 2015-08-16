---
layout: base
title: Countdown API Docs
---

# Countdown API

## JSON Endpoint:

<div style="background:#eee;padding:10px;font-size:1.2em;" markdown="1">
  <https://psas.github.io/countdown/countdown.json>
</div>

## Fields:

   Field     | Description
 ----------- | --------------------------------------------
 `launch`    | [Unix timestamp][1] of upcoming launch time. 
 `certainty` | Values: **TBD** (To Be Decided), **NET** (No Earlier Than), **Date** (launch day scheduled), **Time** (Most likely date and time)
 `name`      | Name of this launch
 `link`      | URL of page for more information about this launch
 `patch`     | URL for svg or png image of the "mission patch" for this launch

## Example:

    {
        "launch": 1464800400,
        "certainty": "TBD",
        "name": "Launch-13",
        "link": "https://github.com/psas/Launch-13",
        "patch": ""
    }




[1]: https://en.wikipedia.org/wiki/Unix_time
