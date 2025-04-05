import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mail, Phone, MapPin, LinkIcon } from "lucide-react";

export default function Home() {
  return (
    <main className="p-4 space-y-12 bg-white text-gray-800">
      {/* Hero Section */}
      <section className="text-center py-8">
        <img
          src="/santram_s-removebg-preview.png"
          alt="Santram Industries Logo"
          className="mx-auto h-32"
        />
        <h1 className="text-4xl font-bold mt-4">Santram Industries</h1>
        <p className="text-lg text-gray-600">Pasta, Vermicelli, Rusk & More</p>
      </section>

      {/* About Section */}
      <section className="max-w-3xl mx-auto">
        <h2 className="text-2xl font-semibold mb-2">About Us</h2>
        <p className="text-gray-700">
          Santram Industries is a leading manufacturer of bakery and food products,
          offering a wide range of high-quality items including macaroni, pasta,
          vermicelli, suji, maida, besan, dalia and rusk. Based in Dehradun,
          Uttarakhand, we serve a growing network of distributors with a focus on
          quality and innovation.
        </p>
      </section>

      {/* IndiaMART Section */}
      <section className="text-center">
        <a
          href="https://IndiaMART.in/POmXZjVD"
          target="_blank"
          className="inline-block mt-6 text-blue-600 underline text-lg font-medium"
        >
          📘 View Our IndiaMART Catalogue
        </a>
      </section>

      {/* Product Gallery */}
      <section>
        <h2 className="text-2xl font-semibold mb-4 text-center">Our Products</h2>
        <div className="grid grid-cols-2 md:grid-cols-3 gap-4">
          {[
            "RUSK 20.png",
            "RUSK.png",
            "DALIA.png",
            "BESAN.png",
            "SUJI.png",
            "MAIDA.png",
            "DEZIA LOGO RED.png"
          ].map((img, i) => (
            <Card key={i} className="rounded-2xl shadow-md">
              <CardContent className="p-2">
                <img
                  src={`/${img}`}
                  alt="product"
                  className="rounded-xl w-full h-48 object-contain"
                />
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Inquiry Form */}
      <section className="max-w-xl mx-auto">
        <h2 className="text-2xl font-semibold mb-4 text-center">Send an Inquiry</h2>
        <form className="space-y-4">
          <input
            type="text"
            placeholder="Your Name"
            className="w-full p-2 border border-gray-300 rounded-xl"
          />
          <input
            type="email"
            placeholder="Your Email"
            className="w-full p-2 border border-gray-300 rounded-xl"
          />
          <textarea
            placeholder="Your Message"
            className="w-full p-2 border border-gray-300 rounded-xl"
            rows={4}
          ></textarea>
          <Button className="w-full bg-green-600 hover:bg-green-700 text-white">
            Submit
          </Button>
        </form>
      </section>

      {/* Contact Section */}
      <section className="text-center">
        <h2 className="text-2xl font-semibold mb-2">Contact Us</h2>
        <div className="space-y-2 text-gray-700">
          <p className="flex items-center justify-center gap-2">
            <Phone className="h-4 w-4" /> +91-8077714106
          </p>
          <p className="flex items-center justify-center gap-2">
            <Mail className="h-4 w-4" /> arjundangwal@outlook.com
          </p>
          <p className="flex items-center justify-center gap-2">
            <MapPin className="h-4 w-4" /> Dehradun, Uttarakhand, India
          </p>
          <a
            href="https://wa.me/918077714106"
            target="_blank"
            className="text-green-600 underline"
          >
            Message us on WhatsApp
          </a>
        </div>
      </section>

      {/* Footer */}
      <footer className="text-center text-sm text-gray-500 pt-6 pb-2">
        © {new Date().getFullYear()} Santram Industries. All rights reserved.
      </footer>
    </main>
  );
}

