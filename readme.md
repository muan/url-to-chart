# URL to chart

Using `chart.js` and `chartjs-node`.

## Usage

With [`qs`](https://github.com/ljharb/qs):

```js
require('qs').stringify({
  w: 1000,
  h: 500,
  type: 'line',
  data: {
    labels: ['Jan', 'Feb', 'Mar', 'Apr', 'Aug', 'Sept', 'Oct', 'Nov', 'Dec'],
    datasets: [
      {
        label: 'hello world',
        data: [25, 21, 23, 24, 22, 24, 24, 30, 29, 28, 31, 32]
      }
    ]
  }
})
> w=1000&h=500&type=line&data%5Blabels%5D%5B0%5D=Jan&data%5Blabels%5D%5B1%5D=Feb&data%5Blabels%5D%5B2%5D=Mar&data%5Blabels%5D%5B3%5D=Apr&data%5Blabels%5D%5B4%5D=Aug&data%5Blabels%5D%5B5%5D=Sept&data%5Blabels%5D%5B6%5D=Oct&data%5Blabels%5D%5B7%5D=Nov&data%5Blabels%5D%5B8%5D=Dec&data%5Bdatasets%5D%5B0%5D%5Blabel%5D=hello%20world&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=25&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=21&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=23&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B3%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B4%5D=22&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B5%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B6%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B7%5D=30&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B8%5D=29&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B9%5D=28&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B10%5D=31&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B11%5D=32
```

![`https://url-to-chart.herokuapp.com?w=1000&h=500&type=line&data%5Blabels%5D%5B0%5D=Jan&data%5Blabels%5D%5B1%5D=Feb&data%5Blabels%5D%5B2%5D=Mar&data%5Blabels%5D%5B3%5D=Apr&data%5Blabels%5D%5B4%5D=Aug&data%5Blabels%5D%5B5%5D=Sept&data%5Blabels%5D%5B6%5D=Oct&data%5Blabels%5D%5B7%5D=Nov&data%5Blabels%5D%5B8%5D=Dec&data%5Bdatasets%5D%5B0%5D%5Blabel%5D=hello%20world&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=25&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=21&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=23&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B3%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B4%5D=22&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B5%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B6%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B7%5D=30&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B8%5D=29&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B9%5D=28&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B10%5D=31&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B11%5D=32`](https://url-to-chart.herokuapp.com?w=1000&h=500&type=line&data%5Blabels%5D%5B0%5D=Jan&data%5Blabels%5D%5B1%5D=Feb&data%5Blabels%5D%5B2%5D=Mar&data%5Blabels%5D%5B3%5D=Apr&data%5Blabels%5D%5B4%5D=Aug&data%5Blabels%5D%5B5%5D=Sept&data%5Blabels%5D%5B6%5D=Oct&data%5Blabels%5D%5B7%5D=Nov&data%5Blabels%5D%5B8%5D=Dec&data%5Bdatasets%5D%5B0%5D%5Blabel%5D=hello%20world&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=25&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=21&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=23&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B3%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B4%5D=22&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B5%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B6%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B7%5D=30&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B8%5D=29&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B9%5D=28&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B10%5D=31&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B11%5D=32)
