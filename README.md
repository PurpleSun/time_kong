# TimeKong

Time converter between timestamp, string and datetime.

## Usages

### TimeKong
```python
from datetime import datetime

from time_kong import TimeKong

TimeKong.timestamp2string(1558883766.864879, formatter="%Y-%m-%d %H:%M:%S.%f")
# '2019-05-26 23:16:06.864879'
TimeKong.timestamp2datetime(1558883766.864879)
# datetime.datetime(2019, 5, 26, 23, 16, 6, 864879)

TimeKong.string2timestamp('2019-05-26 23:16:06.864879', formatter="%Y-%m-%d %H:%M:%S.%f")
# 1558883766.864879
TimeKong.string2datetime('2019-05-26 23:16:06.864879', formatter="%Y-%m-%d %H:%M:%S.%f")
# datetime.datetime(2019, 5, 26, 23, 16, 6, 864879)

d = datetime(year=2019, month=5, day=26, hour=22, minute=42, second=26, microsecond=864879)
TimeKong.datetime2timestamp(d)
# 1558881746.864879
TimeKong.datetime2string(d, formatter="%Y-%m-%d %H:%M:%S.%f")
# '2019-05-26 22:42:26.864879'
```

### TimeGen
```python
from time_kong import TimeGen

print TimeGen.n_milliseconds(42)
print TimeGen.n_seconds(42)
print TimeGen.n_minutes(42)
print TimeGen.n_hours(42)
print TimeGen.n_days(42)
print TimeGen.n_months(42)
print TimeGen.n_years(42)
# 0.042
# 42
# 2520
# 151200
# 3628800
# 108864000
# 39735360000
```

Constants

1. `TimeGen.ONE_MILLISECOND`
2. `TimeGen.ONE_SECOND`
3. `TimeGen.ONE_MINUTE_SECONDS`
4. `TimeGen.ONE_HOUR_SECONDS`
5. `TimeGen.ONE_DAY_SECONDS`
6. `TimeGen.ONE_MONTH_SECONDS`
7. `TimeGen.ONE_YEAR_SECONDS`