---
layout: post
title:  "To the races!"
date:   2016-07-30
categories: python refactoring rewrite
---

One customer contacted us to refactor code they had written previously.
Data was being pulled of a website and processed in various ways to deliver certains view of the data.
The initial code base was developed by the customer. Further enhancements were made by a third party developer.

After initially working with the code the provide the customer what he looked for, it turned out that he
wanted to add more data filters. The existing code base made it difficult to enhance the functionality without the
entire code breaking on minor changes to the data source.

We re-developed the code that decoupled data-capture from data-processing.
This achieved multiple things:

1. Changes to the data source now only require changes to the data extractor library.
2. Data extractors become unit testable.
3. Data filters remain stable on data source changes.
4. Data filters become unit testable.
5. Data filters can easily be combined.

Overall the code become significantly more testable and maintainable.

---

Do you have a similar need? Contact our fearless Ninja at [{{ site.email }}](mailto:{{ site.email }})