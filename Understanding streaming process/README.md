# Understanding Stream Processing

## What is streaming?

- **Stream** is potentially abandoned sequence of objects.
- **Stream Processing** is the act of performing continual calculations on a potentially endless and constantly evolving source of data.
- The unbounded **input** stream is resulted in some **output** stream after the calculations applied.

<img src="https://github.com/makarovartyom/Data-streaming-ND/blob/master/assets/cloud.png" width=520, height=200 align="left"/>

- Stream is also produced at uneven rate - stream has **no start or end** (and event **might not be sent at particular time**) - see the gap between **c** and **a** in the example below.
- Moreover, objects may vary in sizes. See the difference between **y and x**.

### Important difference between data streaming and traditional data schema - data is immutable

- It means once the piece of stream is in place, it cannot be changed or replaced.
- **Example**: input stream c,b,a are not changeable (locked in pic.), same to output stream.
- However, if **a, b** or **c** are *keys* with values (dictionaries), we can create another event, e.g. with key b that points to a different value and add this to the stream. But initial event with value stays the same.

**Example**: same event sent, but values are different for keys.

> click_event: {"button_name": "learn_tab", "location": "Australia", "received_at": "2021-06-17"}, click_event: {"button_name": "learn_tab", "location": "USA", "received_at": "2021-06-19"}


