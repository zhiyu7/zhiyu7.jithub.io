---
title: "Publications"
layout: gridlay
sitemap: false
permalink: /publications/
years: [2016, 2017, 2018, 2019, 2020, 2021]
---

<style>
.jumbotron{
    padding:3%;
    padding-bottom:10px;
    padding-top:10px;
    margin-top:10px;
    margin-bottom:30px;
}
</style>

*equal contribution; [full list of publications](https://scholar.google.com/citations?hl=en&user=gd04NQ8AAAAJ&view_op=list_works&sortby=pubdate)

## Preprints
<div class="jumbotron">
{% bibliography --file ref_preprint --no-bibtex %}
</div>

## Publications

<!-- Display the total count of publications -->
<p>Total number of publications: {{ site.data.references.ref_pub.size }}</p>

<div class="jumbotron">
  <!-- Display all publications without grouping by year -->
  {% bibliography --file ref_pub --no-bibtex %}
</div>
