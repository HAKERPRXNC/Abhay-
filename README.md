export default function PizonWebsite() {
  const menu = [
    { name: 'Margherita', price: '₹299', desc: 'Classic mozzarella, tomato & basil' },
    { name: 'Pepperoni Blast', price: '₹399', desc: 'Loaded with pepperoni & extra cheese' },
    { name: 'Veggie Supreme', price: '₹349', desc: 'Fresh veggies with signature sauce' },
  ];

  return (
    <div className="min-h-screen bg-orange-50 text-gray-900">
      {/* Hero Section */}
      <section className="bg-gradient-to-r from-red-600 to-orange-500 text-white p-10 md:p-20">
        <div className="max-w-6xl mx-auto grid md:grid-cols-2 gap-8 items-center">
          <div>
            <h1 className="text-5xl md:text-7xl font-bold mb-4">PIZON</h1>
            <p className="text-xl mb-6">Hot. Fresh. Delicious. Your favorite pizza delivered fast.</p>
            <button className="bg-white text-red-600 px-6 py-3 rounded-2xl font-semibold shadow-lg hover:scale-105 transition">
              Order Now
            </button>
          </div>
          <div>
            <img
              src="https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&w=1200&q=80"
              alt="Pizza"
              className="rounded-3xl shadow-2xl"
            />
          </div>
        </div>
      </section>

      {/* About */}
      <section className="max-w-6xl mx-auto p-10 text-center">
        <h2 className="text-4xl font-bold mb-4">Why Choose PIZON?</h2>
        <p className="text-lg text-gray-700 max-w-3xl mx-auto">
          At PIZON, we craft every pizza with premium ingredients, hand-tossed dough, and bold flavors that keep you coming back for more.
        </p>
      </section>

      {/* Menu */}
      <section className="max-w-6xl mx-auto p-10">
        <h2 className="text-4xl font-bold text-center mb-8">Popular Menu</h2>
        <div className="grid md:grid-cols-3 gap-6">
          {menu.map((item) => (
            <div key={item.name} className="bg-white rounded-3xl shadow-lg p-6 hover:shadow-xl transition">
              <h3 className="text-2xl font-bold mb-2">{item.name}</h3>
              <p className="text-gray-600 mb-3">{item.desc}</p>
              <span className="text-red-600 text-xl font-bold">{item.price}</span>
            </div>
          ))}
        </div>
      </section>

      {/* Contact */}
      <section className="bg-gray-900 text-white p-10 text-center">
        <h2 className="text-3xl font-bold mb-3">Visit or Call Us</h2>
        <p>📍 Your Address Here, Pune</p>
        <p>📞 +91 98765 43210</p>
        <p>✉️ hello@pizonpizza.com</p>
      </section>
    </div>
  );
}
