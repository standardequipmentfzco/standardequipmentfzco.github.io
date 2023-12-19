---
layout: page
title: Catalog
permalink: /catalog/
---

<div class="row">
    {% assign catalog = site.pages | where_exp: "item" , "item.path contains 'catalog/'"%}
    {% for page in catalog %}
        <div class="col col-12 col-md-6 col-lg-4 mt-4">
            <div class="card rounded-0">
                <img src="{{ site.baseurl }}{{ page.img }}" class="card-img-top" alt="...">
                <div class="card-body">
                <h5 class="card-title">{{ page.title }}</h5>
                <a href="{{ site.baseurl }}{{ page.url }}" class="btn rounded-0 w-100" style="background-color: rgb(195, 54, 54);" data-bs-theme="dark">Full info</a>
                </div>
            </div>
        </div>
    {% endfor %}
</div>
