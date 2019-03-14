---
layout: null
---

<?xml version="1.0" encoding="utf-8"?>
<feed xmlns="http://www.w3.org/2005/Atom">

 <title>{{ site.title }}</title>
 <link href="https://knolleary.net/feed/atom/" rel="self"/>
 <link href="https://knolleary.net"/>
 <updated>{{ site.time | date_to_xmlschema }}</updated>
 <id>https://knolleary.net</id>
 <author>
   <name>{{ site.author.name }}</name>
 </author>

 {% for post in site.posts %}
 <entry>
   <title>{{ post.title }}</title>
   <link href="{{ site.url }}{{ post.url }}"/>
   <updated>{{ post.date | date_to_xmlschema }}</updated>
   <id>{{ site.url }}{{ post.id }}</id>
   <content type="html">{{ post.content | xml_escape }}</content>
 </entry>
 {% endfor %}

</feed>