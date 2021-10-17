Each file could define a custom timestamp column type by specifying a starting year and unit: year, month, day, hour, second, millisecond. A timestamp would then be a number of such units from the beginning of a given year.

A [[Variable length quantity]] should be used as the offset to avoid running out of available range at any point in the future.

A date for example would then be in most applications only two bytes because that would cover a  2^14/365=44 year time span.

A default year would be prefered to make the timestamps in different data segments be comparable without adding an offset. Choosing 1970 as the default would make the timestamps compatible with the unix epoch. That would make dates two bytes long until the year `1970+2^16/365 = 2 149`

For high precision timestamps this may not be worth it because storage space size is logarithmic to the value size. See [[using custom offset for millisecond precision unix epoch is not worth it]] and [[identifier number size does not matter for storage space]]

Some Clojure repl experiments:

```cloure
  (for \[i (range 20)\]
    \[i (Math/pow 2 i)\])

  (/ (Math/log (\* 24 60 60 1000))
     (Math/log 2)
     8)

  (/ (Math/log (\* 365 24 60 60 1000))
     (Math/log 2)
     8)

  (/ (Math/pow 2 (- (\* 5 8) 2))
     (\* 365 24 60 60 #\_1000))

  (/ (Math/pow 2 (- (\* 3 8) 1))
     (\* 365 24 60 #\_60 #\_1000))

  (+ 1970
     (/ (Math/pow 2 (- (\* 8 3) 3))
        365))
```