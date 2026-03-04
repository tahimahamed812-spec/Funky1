import React from "react"; import { motion } from "framer-motion"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { ShoppingCart, Menu } from "lucide-react";

export default function StreetwearWebsite() { return ( <div className="min-h-screen bg-gradient-to-b from-gray-50 to-white text-gray-900 font-sans"> {/* Navbar */} <nav className="flex justify-between items-center p-6 bg-white shadow-sm"> <h1 className="text-2xl font-extrabold tracking-widest">FUNKY</h1> <div className="hidden md:flex gap-8 text-sm uppercase font-semibold"> <a href="#shop" className="hover:text-gray-500">Shop</a> <a href="#about" className="hover:text-gray-500">About</a> <a href="#contact" className="hover:text-gray-500">Contact</a> </div> <div className="flex gap-4"> <ShoppingCart className="cursor-pointer" /> <Menu className="cursor-pointer md:hidden" /> </div> </nav>

{/* Hero Section */}
  <section className="flex flex-col items-center justify-center text-center py-32 px-6 bg-gradient-to-r from-gray-100 via-white to-gray-100">
    <motion.h2
      initial={{ opacity: 0, y: -30 }}
      animate={{ opacity: 1, y: 0 }}
      transition={{ duration: 0.8 }}
      className="text-5xl md:text-7xl font-black tracking-tight"
    >
      LUXE STREET ENERGY
    </motion.h2>
    <p className="mt-6 max-w-2xl text-gray-600 text-lg">
      Where bold street culture meets refined minimal luxury. Oversized silhouettes, premium textures, fearless graphics.
    </p>
    <Button className="mt-10 px-10 py-4 rounded-2xl text-lg bg-black text-white hover:bg-gray-800 shadow-lg">
      Shop The Drop
    </Button>
  </section>

  {/* Highlight Banner */}
  <section className="py-10 text-center bg-black text-white">
    <p className="tracking-widest uppercase text-sm">Limited Edition Release • Worldwide Shipping • Premium Quality</p>
  </section>

  {/* Products Section */}
  <section id="shop" className="py-24 px-6">
    <h3 className="text-3xl font-bold text-center mb-14">Featured Collection</h3>
    <div className="grid grid-cols-1 md:grid-cols-3 gap-12">
      {["Luxury Oversized Hoodie", "Statement Baggy Denim", "Bold Graphic Tee"].map((item, index) => (
        <motion.div
          key={index}
          initial={{ opacity: 0, y: 40 }}
          whileInView={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
        >
          <Card className="bg-white border border-gray-200 rounded-2xl shadow-md hover:shadow-2xl transition duration-300">
            <CardContent className="p-6">
              <div className="h-72 bg-gradient-to-br from-gray-100 to-gray-200 rounded-2xl mb-6" />
              <h4 className="text-xl font-semibold">{item}</h4>
              <p className="text-gray-500 mt-2">Premium Street Luxe Edition</p>
              <Button className="mt-6 w-full rounded-2xl bg-black text-white hover:bg-gray-800">
                Add to Cart
              </Button>
            </CardContent>
          </Card>
        </motion.div>
      ))}
    </div>
  </section>

  {/* About Section */}
  <section id="about" className="py-24 px-6 bg-gray-100 text-center">
    <h3 className="text-3xl font-bold mb-6">About FUNKY</h3>
    <p className="max-w-3xl mx-auto text-gray-600 leading-relaxed text-lg">
      FUNKY is built for the bold generation. We combine high-end minimal tailoring with expressive street graphics. Designed for creators, trendsetters, and leaders who move differently.
    </p>
  </section>

  {/* Newsletter */}
  <section className="py-20 px-6 bg-white text-center">
    <h3 className="text-2xl font-bold mb-4">Join The Movement</h3>
    <p className="text-gray-500 mb-6">Early access to drops & exclusive releases.</p>
    <div className="flex flex-col md:flex-row justify-center gap-4 max-w-xl mx-auto">
      <input
        type="email"
        placeholder="Enter your email"
        className="px-6 py-3 rounded-2xl border border-gray-300 w-full focus:outline-none focus:ring-2 focus:ring-black"
      />
      <Button className="px-8 py-3 rounded-2xl bg-black text-white hover:bg-gray-800">
        Subscribe
      </Button>
    </div>
  </section>

  {/* Footer */}
  <footer className="py-10 text-center border-t border-gray-200 text-gray-500 bg-white">
    © 2026 FUNKY. All Rights Reserved.
  </footer>
</div>

); }
