One would think that choosing some file specific offset instead of the unix epoch offset i.e. the begining of the year 1970 for storing millisecond precision timestamps would save storage space.

Only the offset from the earliest timestamp in the file would have to be stored for each timestamp.

Millisecond precision unix epoch takes currently 41 bits which fits in six bytes. One year timespan in milliseconds is a number that takes 35 bits to store.

Because usually we have to reserve full bytes for encoding data, we have to use five bytes to store that millisecond timestamp for one year time span. Thus we only save one byte for each time stamp and loose in added complexity.

Five bytes can express millisecond precision timestamp accross 34 years:

```
(/ (Math/pow 2 (* 8 5))
   (* 365 24 60 60 1000))
;; => 34.865285000507356
```

Six bytes can express millisecond precision timestamp accross 8925 years:

```
(/ (Math/pow 2 (* 8 6))
   (* 365 24 60 60 1000))
;; => 8925.512960129883
```

Using the current six byte millisecond precision unix epoch can take us to the year `1970 + 8925 = 10 895` until we have to take a seventh byte into use.

See [[identifier number size does not matter for storage space]].