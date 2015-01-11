## Symfony Translation Twig Collection Bundle
Symfony Translation Bundle for Twig Extension to handle collection

### Usage

Translation file (eg. `messages.en.yml`)

```
termsAndConditions:
  title: Terms and Conditions
  paragraph:
    - Terms Information 1
    - Terms Information 2
    - Terms Information 3
    - Terms Information 4
    ...
```

Twig template (eg. `index.html.twig`)

```
{% for i in range(0,'termsAndConditions.paragraph'|translength) -%}
    <p>{{('termsAndConditions.paragraph.'~i)|trans}}</p>
{%- endfor %}
```

### Credits

Inspired by **acontell** http://stackoverflow.com/questions/27868921/symfony2-translation-yaml-array-and-twig-loop