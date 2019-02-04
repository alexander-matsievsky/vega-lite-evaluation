# vega-lite-evaluation

Vega-Lite implementation of https://demo.baremetrics.com/forecast chart.

## Run locally

```bash
git clone https://github.com/alexander-matsievsky/vega-lite-evaluation.git /tmp/vega-lite-evaluation
cd /tmp/vega-lite-evaluation

python -m SimpleHTTPServer 8080 # python2
python -m http.server 8080      # python3

browse http://localhost:8080
```

## Motivation

Since datavis lies at the heart of https://demo.baremetrics.com app
streamlining charts' production is highly desirable for rapid development and ease of maintenance.

> [Vega-Lite](https://vega.github.io/vega-lite/) is a high-level grammar of interactive graphics.
> It provides a concise JSON syntax for rapidly generating visualizations to support analysis.

It would be nice to have a library of plug-n-play declarative visualization specifications backed by a
trusted platform and ecosystem. 

## Conclusion

Implementing a static version of the chart was enjoyable. D3 skills felt right at home.
Overall Vega-Lite seems to be very well thought through and the enthusiasm of the community is encouraging.
There are several quite intriguing dataviz solutions supporting Vega, e.g.
[Altair](https://altair-viz.github.io/) or [Observable](https://beta.observablehq.com/@mbostock/exploring-data-with-vega-lite)
to name some of my favorites. 

Nonetheless the current state of Vega-Lite is not well suited for custom interactivity.
A more low-level [Vega](https://vega.github.io/vega/) grammar supporting
[Signals](https://vega.github.io/vega/docs/signals/) must be employed leading to prohibitive
development and maintenance costs.

Vega project is obviously a thing to keep a close eye on. Right now I'd pick it for quick throw-away
visualizations during exploration or in cases where granular interactivity is not needed.
For a customized interactivity of baremetrics.com good ol' D3 wrapped into Vue components library would serve.

P.S.: the repo contains the static version of the chart only. I tried to go for the Vega implementation
but quickly realized that the output would be cryptic and horrifying+)
 