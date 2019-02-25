# URL to chart

Using [`chart.js`](https://github.com/chartjs/Chart.js) and [`chartjs-node`](https://github.com/vmpowerio/chartjs-node).

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Usage

With [`qs`](https://github.com/ljharb/qs):

### Doughnut chart

```js
require('qs').stringify({
  w: 400,
  h: 400,
  type: 'doughnut',
  data: {
    labels: ['VE RY', 'USEFUL', 'CHART'],
    datasets: [
      {
        borderWidth: 5,
        borderColor: '#ffffff',
        backgroundColor: ['#ff8a8a', '#fbeb76', '#ffc08a'],
        data: [10, 20, 30]
      }
    ]
  }
})
> w=400&h=400&type=doughnut&data%5Blabels%5D%5B0%5D=VERY&data%5Blabels%5D%5B1%5D=USEFUL&data%5Blabels%5D%5B2%5D=CHART&data%5Bdatasets%5D%5B0%5D%5BborderWidth%5D=5&data%5Bdatasets%5D%5B0%5D%5BborderColor%5D=%23ffffff&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B0%5D=%23ff8a8a&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B1%5D=%23fbeb76&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B2%5D=%23ffc08a&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=10&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=20&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=30
```

URL: https://url-to-chart.herokuapp.com/?w=400&h=400&type=doughnut&data%5Blabels%5D%5B0%5D=VERY&data%5Blabels%5D%5B1%5D=USEFUL&data%5Blabels%5D%5B2%5D=CHART&data%5Bdatasets%5D%5B0%5D%5BborderWidth%5D=5&data%5Bdatasets%5D%5B0%5D%5BborderColor%5D=%23ffffff&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B0%5D=%23ff8a8a&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B1%5D=%23fbeb76&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B2%5D=%23ffc08a&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=10&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=20&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=30

Image:

<img src="https://url-to-chart.herokuapp.com/?w=400&h=400&type=doughnut&data%5Blabels%5D%5B0%5D=VERY&data%5Blabels%5D%5B1%5D=USEFUL&data%5Blabels%5D%5B2%5D=CHART&data%5Bdatasets%5D%5B0%5D%5BborderWidth%5D=5&data%5Bdatasets%5D%5B0%5D%5BborderColor%5D=%23ffffff&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B0%5D=%23ff8a8a&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B1%5D=%23fbeb76&data%5Bdatasets%5D%5B0%5D%5BbackgroundColor%5D%5B2%5D=%23ffc08a&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=10&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=20&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=30" width="300">

### Line chart

```js
require('qs').stringify({
  w: 1000,
  h: 400,
  type: 'line',
  data: {
    labels: ['JAN', 'FEB', 'MAR', 'APR', 'AUG', 'SEPT', 'OCT', 'NOV', 'DEC'],
    datasets: [
      {
        label: 'HELLO WORLD',
        data: [25, 21, 23, 24, 22, 24, 24, 30, 29, 28, 31, 30]
      }
    ]
  }
})
> w=1000&h=400&type=line&data%5Blabels%5D%5B0%5D=Jan&data%5Blabels%5D%5B1%5D=Feb&data%5Blabels%5D%5B2%5D=Mar&data%5Blabels%5D%5B3%5D=Apr&data%5Blabels%5D%5B4%5D=Aug&data%5Blabels%5D%5B5%5D=Sept&data%5Blabels%5D%5B6%5D=Oct&data%5Blabels%5D%5B7%5D=Nov&data%5Blabels%5D%5B8%5D=Dec&data%5Bdatasets%5D%5B0%5D%5Blabel%5D=hello%20world&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=25&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=21&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=23&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B3%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B4%5D=22&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B5%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B6%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B7%5D=30&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B8%5D=29&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B9%5D=28&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B10%5D=31&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B11%5D=30
```

URL: https://url-to-chart.herokuapp.com?w=1000&h=400&type=line&data%5Blabels%5D%5B0%5D=Jan&data%5Blabels%5D%5B1%5D=Feb&data%5Blabels%5D%5B2%5D=Mar&data%5Blabels%5D%5B3%5D=Apr&data%5Blabels%5D%5B4%5D=Aug&data%5Blabels%5D%5B5%5D=Sept&data%5Blabels%5D%5B6%5D=Oct&data%5Blabels%5D%5B7%5D=Nov&data%5Blabels%5D%5B8%5D=Dec&data%5Bdatasets%5D%5B0%5D%5Blabel%5D=hello%20world&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=25&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=21&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=23&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B3%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B4%5D=22&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B5%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B6%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B7%5D=30&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B8%5D=29&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B9%5D=28&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B10%5D=31&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B11%5D=30

Image:

![](https://url-to-chart.herokuapp.com?w=1000&h=400&type=line&data%5Blabels%5D%5B0%5D=Jan&data%5Blabels%5D%5B1%5D=Feb&data%5Blabels%5D%5B2%5D=Mar&data%5Blabels%5D%5B3%5D=Apr&data%5Blabels%5D%5B4%5D=Aug&data%5Blabels%5D%5B5%5D=Sept&data%5Blabels%5D%5B6%5D=Oct&data%5Blabels%5D%5B7%5D=Nov&data%5Blabels%5D%5B8%5D=Dec&data%5Bdatasets%5D%5B0%5D%5Blabel%5D=hello%20world&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B0%5D=25&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B1%5D=21&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B2%5D=23&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B3%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B4%5D=22&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B5%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B6%5D=24&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B7%5D=30&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B8%5D=29&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B9%5D=28&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B10%5D=31&data%5Bdatasets%5D%5B0%5D%5Bdata%5D%5B11%5D=30)
