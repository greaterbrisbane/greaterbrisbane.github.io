---
layout: splash
hero_image: 
  src: "assets/images/splash_header.svg"
  alt: "Brisbane River logo motif"
affiliations:
  - 
    url: https://abundanthousing.org.au
    image: https://abundanthousing.org.au/AHNA_favicon.png
  - 
    url: https://parkingreform.org
    image: https://i0.wp.com/parkingreform.org/wp-content/uploads/2020/03/B39E997E-DD3C-4C12-B9B6-86D20080CD69.jpeg

---

Greater Brisbane is an all-volunteer grassroots urbanism collective trying to build a better city for everyone. We want a Brisbane where everyone is welcome and has the opportunity to live a good life wherever they want. 

We believe housing abundance — building more homes where people want to live — is the key to solving the housing crisis and building the kind of cities people love. 

We were started by young people who felt locked out of conversations about their city. We represent thousands of people across Brisbane who want to see their city grow and mature, who want secure and affordable homes near their friends, families and communities and who want to see real action on housing. 

We advocate for better land use, transport and streetscapes to make our city more connected, more sustainable and more accessible. We know that building that city means sacrifices, compromises and trade-offs — but for too long those compromises have been made in favour of millionaire homeowners and real estate agents who are fundamentally opposed to a growing, changing city. 

As long as people want to live in our city, we need to make sure we have enough modern, affordable homes for all of them. To do this we need to build abundant housing of all types and tenures where people want to live — public, private and commons, townhouses to skyscrapers.

---

{% for post in site.posts limit:1 %}
  {% include card.html 
    url=post.url 
    title=post.title 
    description=post.description 
    img_src=post.image %}
{% endfor %}

--- 

<div class="ml-embedded" data-form="SZhH3D"></div>

---

### Proudly part of

<div class="card-holder">
{% for affil in page.affiliations %}
  {% include preview.html url=affil.url image=affil.image title=affil.title description=false %}
{% endfor %}
</div>
