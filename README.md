# shreecomputersnashik
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Shree Computers — Sales & Service</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 text-gray-800 font-sans">
  <!-- Header -->
  <header class="sticky top-0 z-50 backdrop-blur bg-white/80 border-b shadow-sm">
    <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
      <div class="flex items-center gap-3">
        <div class="h-12 w-12 rounded-2xl bg-gradient-to-br from-blue-800 to-blue-900 grid place-items-center text-white shadow-md">
          💻
        </div>
        <div>
          <h1 class="text-xl font-bold">Shree Computers</h1>
          <p class="text-sm text-gray-600">Trusted IT Solutions, Sales & Expert Repairs</p>
        </div>
      </div>
      <nav class="hidden md:flex items-center gap-8 text-sm font-medium">
        <a href="#products" class="hover:text-blue-900">Shop</a>
        <a href="#services" class="hover:text-blue-900">Services</a>
        <a href="#contact" class="hover:text-blue-900">Contact</a>
      </nav>
      <a href="tel:+919850902158" class="px-4 py-2 rounded-xl border border-blue-900 text-blue-900 hover:bg-blue-50 shadow-sm">📞 Call</a>
    </div>
  </header>

  <!-- Hero -->
  <section class="bg-gradient-to-br from-white via-gray-50 to-blue-50 border-b">
    <div class="max-w-7xl mx-auto px-6 py-16 grid md:grid-cols-2 gap-10 items-center">
      <div>
        <h2 class="text-4xl md:text-5xl font-extrabold leading-tight">
          Your Trusted <span class="bg-clip-text text-transparent bg-gradient-to-r from-blue-800 to-blue-900">Computer Partner</span>
        </h2>
        <p class="mt-4 text-gray-600 text-lg">Laptops, PCs, Accessories & IT services with AMC plans in Nashik.</p>
        <div class="mt-6 flex gap-4">
          <a href="#products" class="px-6 py-3 rounded-xl bg-gradient-to-r from-blue-800 to-blue-900 text-white shadow-md">🛒 Start Shopping</a>
          <a href="#services" class="px-6 py-3 rounded-xl border border-blue-900 text-blue-900 hover:bg-blue-50 shadow-sm">🔧 Book a Repair</a>
        </div>
      </div>
      <div>
        <img src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=1600&auto=format&fit=crop" class="rounded-3xl shadow-2xl border" alt="Computer shop"/>
      </div>
    </div>
  </section>

  <!-- Products -->
  <section id="products" class="max-w-7xl mx-auto px-6 py-16">
    <h2 class="text-3xl font-bold mb-8 text-center">Featured Products</h2>
    <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-6">
      <div class="p-4 bg-white rounded-xl shadow-md border">
        <h3 class="font-semibold">Dell Laptop i5</h3>
        <p class="text-gray-600">Powerful laptop for office & study</p>
        <p class="mt-2 font-bold text-blue-900">₹45,000</p>
      </div>
      <div class="p-4 bg-white rounded-xl shadow-md border">
        <h3 class="font-semibold">HP Laser Printer</h3>
        <p class="text-gray-600">High-speed printing for home & office</p>
        <p class="mt-2 font-bold text-blue-900">₹12,000</p>
      </div>
      <div class="p-4 bg-white rounded-xl shadow-md border">
        <h3 class="font-semibold">Lenovo Desktop</h3>
        <p class="text-gray-600">Reliable desktop PC with warranty</p>
        <p class="mt-2 font-bold text-blue-900">₹28,000</p>
      </div>
    </div>
  </section>

  <!-- Services -->
  <section id="services" class="bg-gray-100 border-t border-b py-16">
    <div class="max-w-7xl mx-auto px-6">
      <h2 class="text-3xl font-bold mb-8 text-center">Our Services</h2>
      <div class="grid sm:grid-cols-2 md:grid-cols-3 gap-6">
        <div class="p-6 bg-white rounded-xl shadow-md border">🔧 Laptop/Desktop Repair</div>
        <div class="p-6 bg-white rounded-xl shadow-md border">📦 AMC IT Solutions</div>
        <div class="p-6 bg-white rounded-xl shadow-md border">🌐 Accessories & Networking</div>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="max-w-7xl mx-auto px-6 py-16">
    <h2 class="text-3xl font-bold mb-8 text-center">Contact Us</h2>
    <div class="grid md:grid-cols-2 gap-10">
      <div>
        <p class="mb-2">📍 Kamgar Nagar, Satpur, Nashik 422007</p>
        <p class="mb-2">📞 +91 98509 02158</p>
        <a href="https://wa.me/919850902158" class="px-4 py-2 rounded-xl bg-green-600 text-white shadow-md">💬 WhatsApp</a>
      </div>
      <form class="bg-white p-6 rounded-xl shadow-md border">
        <label class="block mb-2 font-medium">Your Name</label>
        <input type="text" class="w-full border rounded-lg p-2 mb-4"/>
        <label class="block mb-2 font-medium">Message</label>
        <textarea class="w-full border rounded-lg p-2 mb-4"></textarea>
        <button type="submit" class="px-6 py-2 rounded-xl bg-gradient-to-r from-blue-800 to-blue-900 text-white">Send</button>
      </form>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gradient-to-r from-blue-800 to-blue-900 text-white py-6 text-center">
    © 2025 Shree Computers. All rights reserved.
  </footer>
</body>
</html>
