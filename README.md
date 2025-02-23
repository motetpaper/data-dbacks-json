# Arizona Diamondbacks Schedule in JSON format

# DATA SOURCE
This JSON data feed is based on the [downloadable schedule](https://www.mlb.com/dbacks/schedule/downloadable-schedule) from the official Arizona Diamondbacks web site. You can link directly to this JSON feed on GitHub:

```bash
https://raw.githubusercontent.com/motetpaper/data-dbacks-json/refs/heads/main/outputs/dbacks.json
```


# PURPOSE

Converting the CSV into a JSON document creates oppotunities to query the Arizona Diamondbacks regular season schedule. For example, you can use the `jq` command line program to perform such queries:

### EXAMPLE: Diamondbacks vs. Yankees

We can filter the JSON feed to only show Yankees games.
```bash
 cat dbacks.json | jq '.[] | select(.teamcode == "NYY")'
```

[Learn more about jq](https://jqlang.org/).

### RESULT

We see that there are 3 away games in April.

```javascript
{
  "date": "2025-04-01",
  "datets": 1743490800000,
  "dateiso": "2025-04-01T07:00:00.000Z",
  "firstpitch": "4:05 PM",
  "firstpitchts": 1743548700000,
  "firstpitchiso": "2025-04-01T23:05:00.000Z",
  "team": "Yankees",
  "teamcode": "NYY",
  "homegame": false,
  "openingdayts": 1743058800000,
  "openingdayiso": "2025-03-27T07:00:00.000Z",
  "openingday": "2025-03-27"
}
{
  "date": "2025-04-02",
  "datets": 1743577200000,
  "dateiso": "2025-04-02T07:00:00.000Z",
  "firstpitch": "4:05 PM",
  "firstpitchts": 1743635100000,
  "firstpitchiso": "2025-04-02T23:05:00.000Z",
  "team": "Yankees",
  "teamcode": "NYY",
  "homegame": false,
  "openingdayts": 1743058800000,
  "openingdayiso": "2025-03-27T07:00:00.000Z",
  "openingday": "2025-03-27"
}
{
  "date": "2025-04-03",
  "datets": 1743663600000,
  "dateiso": "2025-04-03T07:00:00.000Z",
  "firstpitch": "4:05 PM",
  "firstpitchts": 1743721500000,
  "firstpitchiso": "2025-04-03T23:05:00.000Z",
  "team": "Yankees",
  "teamcode": "NYY",
  "homegame": false,
  "openingdayts": 1743058800000,
  "openingdayiso": "2025-03-27T07:00:00.000Z",
  "openingday": "2025-03-27"
}
```

# FIELDS

More fields will be added to the JSON feed. For now, here is the starting lineup.

## SAMPLE ENTRY
```javascript
  {
    "date": "2025-03-27",
    "datets": 1743058800000,
    "dateiso": "2025-03-27T07:00:00.000Z",
    "firstpitch": "7:10 PM",
    "firstpitchts": 1743127800000,
    "firstpitchiso": "2025-03-28T02:10:00.000Z",
    "team": "Cubs",
    "teamcode": "CHC",
    "homegame": true,
    "openingdayts": 1743058800000,
    "openingdayiso": "2025-03-27T07:00:00.000Z",
    "openingday": "2025-03-27"
  },
```


