{% extends 'core/base.html' %}

{% block title %}Sign up{% endblock %}

{% block content %}
<div class"w-1/2 my-6 mx-auto p-6 bg-gray-200 rounded-xl">
    <h1 class="mb-6 text-3x1">Sign up</h1>

    <form method="post" action=".">
        {% csrf_token %}
