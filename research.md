---
layout: page
permalink: /research/
title: Research
pubs:
    - title:   "SQL-Encoder: Improving NL2SQL In-Context Learning Through a Context-Aware Encoder"
      author:  "Mohammadreza Pourreza, Davood Rafiei, Yuxi Feng, Raymond Li, Zhenan Fan, Weiwei Zhang"
      journal: "Preprint"
      year:    "2024"
      url:     "https://arxiv.org/abs/2403.16204"
      Media:
      - name: "Official Video"
        url: "https://aclanthology.org/2023.acl-long.488.mp4"



    - title:   "DuNST: Dual Noisy Self Training for Semi-Supervised Controllable Text Generation"
      author:  "Yuxi Feng, Xiaoyuan Yi, Xiting Wang, Laks V.S. Lakshmanan, Xing Xie"
      journal: "ACL"
      year:    "2023"
      url:     "https://aclanthology.org/2023.acl-long.488/"
      Media:
      - name: "Official Video"
        url: "https://aclanthology.org/2023.acl-long.488.mp4"

    - title:   "KEST: Kernel Distance Based Efficient Self-Training for Improving Controllable Text Generation"
      author:  "Yuxi Feng, Xiaoyuan Yi, Laks V.S. Lakshmanan, Xing Xie"
      journal: "IJCAI"
      year:    "2023"
      url:     "[https://aclanthology.org/2023.acl-long.488/](https://www.ijcai.org/proceedings/2023/0561.pdf)"
      doi:     "https://doi.org/10.24963/ijcai.2023/561"


---

## Publications

{% assign thumbnail="left" %}

{% for pub in page.pubs %}
{% if pub.image %}
{% include image.html url=pub.image caption="" height="100px" align=thumbnail %}
{% endif %}
[**{{pub.title}}**]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %})<br />
{{pub.author}}<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})*
{% endif %} *{{pub.year}}* {% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}
{% if pub.media %}<br />Media: {% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}

{% endfor %}
