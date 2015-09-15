---
layout: default
group: config-guide
subgroup: Caching
title: Caching
menu_title: Caching
menu_order: 1
menu_node: parent
github_link: config-guide/config/caching.md
redirect_from: /guides/v1.0/config-guide/config/caching.html
---

#### Contents 

*	<a href="#m2devgde-cache-explore">Overview of caching</a>
*	<a href="#m2devgde-cache-type">Create a cache type</a>
* <a href="#m2devgde-cache-more">More information about caching</a>

<h2 id="m2devgde-cache-explore">Overview of caching</h2>
Magento uses <a href="http://framework.zend.com/manual/1.12/en/zend.cache.html" target="_blank">Zend_Cache</a> component for interaction with the cache storage. However, Magento also has <a href="{{ site.mage2000url }}lib/internal/Magento/Framework/Cache" target="_blank">Magento\Cache</a> library component for implementing Magento-specific caching.

<div class="bs-callout bs-callout-info" id="info">
  <p>By default, file system caching is enabled; no configuration is necessary to use it. This means the cache is located under <code>&lt;your Magento install dir>/var</code>.</p>
</div> 

To change the cache configuration, edit `<your Magento install dir>/app/etc/env.php`.

The cache configuration is an associative array similar to the following:

{% highlight PHP %}
<? php
'cache_types' =>
  array (
    'config' => 1,
    'layout' => 1,
    'block_html' => 1,
    'collections' => 1,
    'db_ddl' => 1,
    'eav' => 1,
    'full_page' => 1,
    'translate' => 1,
    'config_integration' => 1,
    'config_webservice' => 1,
    'config_integration_api' => 1,
  ),
); ?>
{% endhighlight %}

#### Related topics
TBD