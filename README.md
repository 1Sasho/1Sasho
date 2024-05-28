
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">

        <scripts src="https://cdn.tailwindcss.com"></script>

            <title>{% block title %}{% endblock %} | Puddle</title>
        <head>

        <body>
            <nav class="py-6 px-6 flex justify-between items-center:"border-b -gray-200">
                <a href="/" class="text-xl font semibold">Puddle<a/>

                <div class="space-x-6">
                    <a href="#" class="text-lg font-semibold hover:text-gray-500">New item<a/>
                    <a href="#" class="text-lg font-semibold hover:text-gray-500">browse<a/>

                    <a href="#" class="px-6 py-3 text-lg font-semibold bg-teal-500 text-white rounded-xl hover:bg-teal-700">sing up</a>
                    <a href="#" class="px-6 py-3 text-lg font-semibold bg-gray-500 text-white rounded-xl hover:bg-gray-700">log in</a>
                    
                    <div class="px-6 py-6">

                        </div>
                    </nav>

            <div class="px-6 py-6">
                {% block content %}
                {% endblock %}
            </div>
            <footer class=
