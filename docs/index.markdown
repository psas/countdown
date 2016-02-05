---
layout: page
title: Countdown API
description: "How to use the PSAS launch countdown API"
---


## JSON Endpoint:

<div class="code" markdown="1">
  <http://psas.pdx.edu/countdown/countdown.json>
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

**Example request:**

{% highlight HTTP %}
GET /countdown/countdown.json HTTP/1.1
Host: psas.pdx.edu
Accept: application/json, text/javascript
{% endhighlight %}

**Example response:**

{% highlight HTTP %}
HTTP/1.1 200 OK
Access-Control-Allow-Origin:*
Content-Type:application/json

{
    "launch": 1464800400,
    "certainty": "TBD",
    "name": "Launch-13",
    "link": "https://github.com/psas/Launch-13",
    "patch": ""
}
{% endhighlight %}


[1]: https://en.wikipedia.org/wiki/Unix_time
