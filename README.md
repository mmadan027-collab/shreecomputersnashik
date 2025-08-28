import React, { useMemo, useState } from "react";
import { motion } from "framer-motion";
import {
  ShoppingCart,
  Laptop,
  Cpu,
  HardDrive,
  Monitor,
  Printer,
  Headphones,
  Smartphone,
  Search,
  Star,
  Truck,
  ShieldCheck,
  PhoneCall,
  IndianRupee,
  X,
  Plus,
  Minus,
  ArrowRight,
  Wrench,
  MessageSquareText,
} from "lucide-react";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardDescription, CardFooter, CardHeader, CardTitle } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Badge } from "@/components/ui/badge";
import { Label } from "@/components/ui/label";
import { Textarea } from "@/components/ui/textarea";
import {
  Sheet,
  SheetContent,
  SheetHeader,
  SheetTitle,
  SheetTrigger,
  SheetFooter,
  SheetClose,
} from "@/components/ui/sheet";
import {
  Dialog,
  DialogContent,
  DialogHeader,
  DialogTitle,
  DialogDescription,
  DialogFooter,
  DialogTrigger,
} from "@/components/ui/dialog";

// ----------
// CONFIG: Edit these details for your shop
// ----------
const SHOP = {
  name: "Shree Computers — Sales & Service",
  tagline: "Trusted IT Solutions, Sales & Expert Repairs in Nashik",
  phone: "+919850902158",
  address: "Kamgar Nagar, Satpur, Nashik 422007",
  whatsappNumber: "+919850902158", // used for WhatsApp orders
  gmbUrl: "https://www.google.com/maps/search/?api=1&query=Shree+Computers+Satpur+Nashik",
  brandPrimary: "from-blue-800 to-blue-900", // updated to navy blue gradient
};

// Categories and Products stay same (for brevity not re-written fully)
// ...

// Format INR
function formatINR(value) {
  return new Intl.NumberFormat("en-IN", { style: "currency", currency: "INR", maximumFractionDigits: 0 }).format(value);
}

// Stars Component
function Stars({ value }) {
  const full = Math.floor(value);
  const half = value - full >= 0.5;
  return (
    <div className="flex items-center gap-1 text-yellow-500" aria-label={`Rated ${value} out of 5`}>
      {Array.from({ length: full }).map((_, i) => (
        <Star key={i} className="h-4 w-4 fill-current" />
      ))}
      {half && <Star className="h-4 w-4 opacity-70" />}
    </div>
  );
}

export default function App() {
  // State and logic remain same (not rewriting fully)
  // ...

  return (
    <div className="min-h-screen bg-gradient-to-b from-gray-100 via-white to-gray-50 font-sans text-gray-800">
      {/* Top Bar */}
      <header className="sticky top-0 z-50 backdrop-blur bg-white/80 border-b shadow-sm">
        <div className="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
          <div className="flex items-center gap-3">
            <motion.div initial={{ opacity: 0, y: -8 }} animate={{ opacity: 1, y: 0 }} className={`h-12 w-12 rounded-2xl bg-gradient-to-br ${SHOP.brandPrimary} grid place-items-center text-white shadow-md`}>
              <Laptop className="h-6 w-6" />
            </motion.div>
            <div>
              <h1 className="text-xl font-bold leading-tight tracking-tight">{SHOP.name}</h1>
              <p className="text-sm text-muted-foreground">{SHOP.tagline}</p>
            </div>
          </div>
          <nav className="hidden md:flex items-center gap-8 text-sm font-medium">
            <a href="#products" className="hover:text-blue-900 transition-colors">Shop</a>
            <a href="#services" className="hover:text-blue-900 transition-colors">Services</a>
            <a href={SHOP.gmbUrl} target="_blank" className="hover:text-blue-900 transition-colors">Reviews</a>
            <a href="#contact" className="hover:text-blue-900 transition-colors">Contact</a>
          </nav>
          <div className="flex items-center gap-2">
            <Button variant="outline" className="rounded-xl shadow-sm" asChild>
              <a href={`tel:${SHOP.phone}`}><PhoneCall className="h-4 w-4 mr-2"/>Call</a>
            </Button>
            {/* Cart Sheet remains same */}
          </div>
        </div>
      </header>

      {/* Hero Section */}
      <section className="bg-gradient-to-br from-white via-gray-50 to-blue-50 border-b">
        <div className="max-w-7xl mx-auto px-6 py-16 grid md:grid-cols-2 gap-10 items-center">
          <div>
            <motion.h2 initial={{ opacity: 0, y: 10 }} animate={{ opacity: 1, y: 0 }} className="text-4xl md:text-5xl font-extrabold leading-tight tracking-tight">
              Your Trusted <span className={`bg-clip-text text-transparent bg-gradient-to-r ${SHOP.brandPrimary}`}>Computer Partner</span>
            </motion.h2>
            <p className="mt-4 text-gray-600 text-lg max-w-lg">
              Complete range of laptops, PCs, accessories & on‑site IT services with AMC plans for homes and businesses in Nashik.
            </p>
            <div className="mt-6 flex flex-wrap gap-4">
              <Button className="rounded-xl px-6 py-3 text-lg shadow-md bg-gradient-to-r from-blue-800 to-blue-900 text-white" asChild>
                <a href="#products"><ShoppingCart className="h-5 w-5 mr-2"/>Start Shopping</a>
              </Button>
              <Button variant="outline" className="rounded-xl px-6 py-3 text-lg shadow-sm border-blue-900 text-blue-900 hover:bg-blue-50" asChild>
                <a href="#services"><Wrench className="h-5 w-5 mr-2"/>Book a Repair</a>
              </Button>
            </div>
            <div className="mt-8 grid grid-cols-2 sm:grid-cols-3 gap-4 text-sm">
              <div className="p-4 rounded-xl bg-white shadow-md border flex items-center gap-2"><Truck className="h-4 w-4 text-blue-900"/> Same‑Day Delivery*</div>
              <div className="p-4 rounded-xl bg-white shadow-md border flex items-center gap-2"><ShieldCheck className="h-4 w-4 text-green-600"/> 1‑Year Warranty</div>
              <div className="p-4 rounded-xl bg-white shadow-md border flex items-center gap-2"><Star className="h-4 w-4 text-yellow-500"/> 4.8★ Rated Locally</div>
            </div>
          </div>
          <motion.div initial={{ opacity: 0, y: 20 }} animate={{ opacity: 1, y: 0 }} className="relative">
            <img src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=1600&auto=format&fit=crop" alt="Computer shop" className="rounded-3xl shadow-2xl border"/>
            <Badge className="absolute bottom-5 left-5 rounded-xl backdrop-blur bg-white/90 text-gray-800 font-medium shadow-md">{SHOP.address}</Badge>
          </motion.div>
        </div>
      </section>

      {/* Rest of sections (products, services, testimonials, contact, footer) remain same */}
      {/* But all should use consistent shadow-md, rounded-xl, spacing, and navy blue highlights */}
    </div>
  );
}
