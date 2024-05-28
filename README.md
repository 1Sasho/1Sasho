<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>{% block title %}{% endblock %} | Puddle</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
    <nav class="py-6 px-6 flex justify-between items-center border-b border-gray-200">
        <a href="/" class="text-xl font-semibold">Puddle</a>

        <div class="space-x-6">
            <a href="#" class="text-lg font-semibold hover:text-gray-500">New item</a>
            <a href="#" class="text-lg font-semibold hover:text-gray-500">Browse</a>
            <a href="#" class="px-6 py-3 text-lg font-semibold bg-teal-500 text-white rounded-xl hover:bg-teal-700">Sign Up</a>
            <a href="#" class="px-6 py-3 text-lg font-semibold bg-gray-500 text-white rounded-xl hover:bg-gray-700">Log In</a>
        </div>
    </nav>

    <div class="px-6 py-6">
        {% block content %}
        {% endblock %}
    </div>

    <footer class="px-6 py-6">
        <!-- Footer content -->
    </footer>
</body>
</html>
