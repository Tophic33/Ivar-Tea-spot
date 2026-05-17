export default function IvarJRTeaSpotApp() {
  const teas = [
    {
      name: "Classic Milk Tea",
      price: "GHS 18",
      image:
        "https://images.unsplash.com/photo-1515823064-d6e0c04616a7?q=80&w=1200&auto=format&fit=crop",
    },
    {
      name: "Ginger Herbal Tea",
      price: "GHS 15",
      image:
        "https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?q=80&w=1200&auto=format&fit=crop",
    },
    {
      name: "Lemon Green Tea",
      price: "GHS 20",
      image:
        "https://images.unsplash.com/photo-1544145945-f90425340c7e?q=80&w=1200&auto=format&fit=crop",
    },
  ];

  return (
    <div className="min-h-screen bg-black text-white font-sans">
      {/* Hero */}
      <section className="relative overflow-hidden bg-gradient-to-br from-black via-zinc-900 to-yellow-950">
        <div className="absolute inset-0 opacity-20 bg-[radial-gradient(circle_at_top_right,_#facc15,_transparent_40%)]"></div>

        <div className="relative z-10 max-w-7xl mx-auto px-6 py-20 grid md:grid-cols-2 gap-10 items-center">
          <div>
            <p className="uppercase tracking-[0.3em] text-yellow-400 mb-4 text-sm">
              Premium Tea Experience
            </p>

            <h1 className="text-5xl md:text-7xl font-black leading-tight">
              IVAR JR
              <span className="block text-yellow-400">Tea Spot</span>
            </h1>

            <p className="mt-6 text-zinc-300 text-lg max-w-xl leading-relaxed">
              A futuristic tea ordering experience with smooth mobile payments,
              premium drinks, and fast delivery.
            </p>

            <div className="flex flex-wrap gap-4 mt-8">
              <button className="bg-yellow-400 text-black px-6 py-3 rounded-2xl font-bold hover:scale-105 transition">
                Order Now
              </button>

              <button className="border border-zinc-700 px-6 py-3 rounded-2xl hover:bg-zinc-800 transition">
                Explore Menu
              </button>
            </div>
          </div>

          <div className="relative">
            <div className="absolute -top-10 -right-10 w-40 h-40 bg-yellow-400 blur-3xl opacity-30 rounded-full"></div>

            <img
              src="https://images.unsplash.com/photo-1511920170033-f8396924c348?q=80&w=1200&auto=format&fit=crop"
              alt="Tea"
              className="rounded-[32px] shadow-2xl border border-zinc-800"
            />
          </div>
        </div>
      </section>

      {/* Menu */}
      <section className="max-w-7xl mx-auto px-6 py-20">
        <div className="flex items-center justify-between mb-10">
          <div>
            <h2 className="text-4xl font-bold">Popular Drinks</h2>
            <p className="text-zinc-400 mt-2">
              Freshly made premium tea selections.
            </p>
          </div>

          <div className="bg-zinc-900 border border-zinc-800 rounded-2xl px-5 py-3">
            <p className="text-sm text-zinc-400">Payments Supported</p>
            <p className="font-bold text-yellow-400">MTN MoMo</p>
          </div>
        </div>

        <div className="grid md:grid-cols-3 gap-8">
          {teas.map((tea, index) => (
            <div
              key={index}
              className="bg-zinc-900 border border-zinc-800 rounded-3xl overflow-hidden hover:-translate-y-2 transition duration-300"
            >
              <img
                src={tea.image}
                alt={tea.name}
                className="h-64 w-full object-cover"
              />

              <div className="p-6">
                <div className="flex items-center justify-between">
                  <h3 className="text-2xl font-bold">{tea.name}</h3>
                  <span className="text-yellow-400 font-bold">
                    {tea.price}
                  </span>
                </div>

                <button className="w-full mt-6 bg-yellow-400 text-black py-3 rounded-2xl font-bold hover:bg-yellow-300 transition">
                  Add to Cart
                </button>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Payment Section */}
      <section className="bg-zinc-950 border-t border-zinc-800">
        <div className="max-w-5xl mx-auto px-6 py-20 grid md:grid-cols-2 gap-12 items-center">
          <div>
            <p className="text-yellow-400 uppercase tracking-[0.3em] text-sm mb-4">
              Fast Checkout
            </p>

            <h2 className="text-4xl font-black leading-tight">
              Pay instantly with MTN MoMo
            </h2>

            <p className="mt-5 text-zinc-400 leading-relaxed">
              Customers can enter their MTN MoMo number and complete payments
              securely.
            </p>
          </div>

          <div className="bg-zinc-900 border border-zinc-800 rounded-3xl p-8 shadow-2xl">
            <h3 className="text-2xl font-bold mb-6">Checkout</h3>

            <div className="space-y-4">
              <input
                type="text"
                placeholder="Full Name"
                className="w-full bg-black border border-zinc-700 rounded-2xl px-4 py-3 outline-none"
              />

              <input
                type="tel"
                placeholder="MTN MoMo Number"
                className="w-full bg-black border border-zinc-700 rounded-2xl px-4 py-3 outline-none"
              />

              <select className="w-full bg-black border border-zinc-700 rounded-2xl px-4 py-3 outline-none">
                <option>Select Drink</option>
                <option>Classic Milk Tea</option>
                <option>Ginger Herbal Tea</option>
                <option>Lemon Green Tea</option>
              </select>

              <button className="w-full bg-yellow-400 text-black py-4 rounded-2xl font-black text-lg hover:scale-[1.02] transition">
                Pay with MTN MoMo
              </button>
            </div>

            <p className="text-xs text-zinc-500 mt-5 leading-relaxed">
              MVP Demo: Connect the button to MTN MoMo API or Hubtel payment
              gateway for live production payments.
            </p>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="border-t border-zinc-800 py-8 text-center text-zinc-500 text-sm">
        © 2026 IVAR JR Tea Spot — Futuristic Tea Ordering MVP
      </footer>
    </div>
  );
}
