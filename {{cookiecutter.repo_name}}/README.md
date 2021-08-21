# {{ cookiecutter.project_name }}


{{ cookiecutter.project_short_description }}
{% if cookiecutter.license != "no" %}
* Free software: {{cookiecutter.license }}
{% endif %}

# Installation

    pip install {{ cookiecutter.distribution_name }}

You can also install the in-development version with:

```
{% if cookiecutter.repo_hosting_domain == "github.com" %}
    pip install https://github.com/{{ cookiecutter.repo_username }}/{{ cookiecutter.repo_name }}/archive/master.zip
{% elif cookiecutter.repo_hosting_domain == "gitlab.com" %}
    pip install https://gitlab.com/{{ cookiecutter.repo_username }}/{{ cookiecutter.repo_name }}/-/archive/master/{{ cookiecutter.repo_name }}-master.zip
{% else %}
    pip install git+ssh://git@{{ cookiecutter.repo_hosting_domain }}/{{ cookiecutter.repo_username }}/{{ cookiecutter.repo_name }}.git@master
{%- endif %}
```
