# Prashiskan-An-App-for-Academia-Industry-Interface
import React from "react"; import { motion } from "framer-motion";

// Prashiskshan - Single File React Prototype (TailwindCSS) // Default export a component that can be dropped into a create-react-app or Next.js page. // Uses Tailwind utility classes. Replace placeholder image URLs and logo with real assets.

export default function PrashiskshanPrototype() { const features = [ "Student Internship Portal", "Faculty Monitoring Panel", "Industry Collaboration System", "Skill Readiness Courses", "Auto Logbook & Report Generator", "Credit Integration System", ];

const benefits = [ "Real, verified internships", "Better skill development", "Transparent credit system", "Stronger college–industry partnership", ];

const team = [ "Sri Manaswini", "Anjali Reddy", "Nandini", "Rakesh", "Chandra Mohan", "Ganesh", ];

return ( <div className="min-h-screen bg-gradient-to-b from-blue-600 via-blue-500 to-blue-600 text-slate-900 antialiased"> <header className="max-w-6xl mx-auto px-6 py-6 flex items-center justify-between"> <div className="flex items-center gap-4"> {/* Placeholder for KPRIT logo */} <img
src="/logo-placeholder.png"
alt="KPRIT logo"
className="w-16 h-16 rounded-full bg-white p-1 object-contain"
/> <div> <h1 className="text-white text-xl font-semibold">KPRIT - UGC Autonomous</h1> <p className="text-slate-200 text-xs">Directorate of Colleges, Higher Education Department</p> </div> </div> <nav className="hidden md:flex gap-6 items-center text-white text-sm"> <a href="#features" className="hover:underline">Features</a> <a href="#solution" className="hover:underline">Solution</a> <a href="#team" className="hover:underline">Team</a> <a href="#contact" className="px-3 py-2 bg-white/10 rounded-md">Contact</a> </nav> </header>

<main className="max-w-6xl mx-auto px-6">
    {/* Hero */}
    <section className="grid grid-cols-1 md:grid-cols-2 gap-8 items-center py-12">
      <motion.div
        initial={{ opacity: 0, y: 10 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.5 }}
        className="text-white"
      >
        <h2 className="text-4xl md:text-5xl font-extrabold leading-tight">Prashiskshan</h2>
        <p className="mt-2 text-lg text-slate-200">Bridging Academia and Industry — One App. One Platform.</p>

        <ul className="mt-6 grid grid-cols-1 sm:grid-cols-2 gap-3">
          <li className="bg-white/10 p-3 rounded-md text-sm">NEP 2020 compliant internships</li>
          <li className="bg-white/10 p-3 rounded-md text-sm">Auto logbooks & report generator</li>
          <li className="bg-white/10 p-3 rounded-md text-sm">Faculty monitoring & credit system</li>
          <li className="bg-white/10 p-3 rounded-md text-sm">Remote-friendly internships for rural students</li>
        </ul>

        <div className="mt-6 flex gap-3">
          <a href="#features" className="px-5 py-3 bg-white text-blue-600 rounded-md font-semibold">Explore Features</a>
          <a href="#contact" className="px-5 py-3 border border-white/30 rounded-md text-white">Get in touch</a>
        </div>

        <div className="mt-4 text-sm text-slate-200">Category: <strong>Software</strong> · Theme: <strong>Smart Education</strong></div>
      </motion.div>

      <motion.div
        initial={{ opacity: 0, scale: 0.98 }}
        animate={{ opacity: 1, scale: 1 }}
        transition={{ duration: 0.6 }}
        className="flex justify-center md:justify-end"
      >
        {/* Illustration placeholder - replace with SVG or image */}
        <div className="w-full max-w-md bg-white rounded-2xl p-6 shadow-xl">
          <img
            src="/hero-illustration-placeholder.png"
            alt="students and industry illustration"
            className="w-full h-64 object-contain"
          />
        </div>
      </motion.div>
    </section>

    {/* Problem & Solution cards */}
    <section className="grid grid-cols-1 md:grid-cols-2 gap-6 my-8">
      <article className="bg-white rounded-2xl p-6 shadow-lg">
        <h3 className="text-xl font-semibold">Problem</h3>
        <p className="mt-3 text-sm text-slate-600">Many students struggle to access real internships due to poor college–industry ties, late planning, lack of mentorship, and fake certificates.</p>
        <ul className="mt-4 list-disc list-inside text-sm text-slate-600">
          <li>No industry tie-ups</li>
          <li>Poor monitoring and mentorship</li>
          <li>Unreliable remote options for rural students</li>
        </ul>
      </article>

      <article id="solution" className="bg-white rounded-2xl p-6 shadow-lg">
        <h3 className="text-xl font-semibold">Our Solution — Prashiskshan</h3>
        <p className="mt-3 text-sm text-slate-600">A centralized digital platform to connect students, colleges, and industries with real-time internship listings, automatic logbooks, and credit integration.</p>
        <div className="mt-4 text-sm">
          <strong>Outcomes:</strong>
          <ul className="list-inside list-disc">
            <li>Verified internships</li>
            <li>Skill readiness & training</li>
            <li>Transparent credits & reports</li>
          </ul>
        </div>
      </article>
    </section>

    {/* Features */}
    <section id="features" className="bg-white rounded-2xl p-6 shadow-lg mb-8">
      <h3 className="text-2xl font-semibold text-slate-800">Key Features</h3>
      <div className="mt-4 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
        {features.map((f) => (
          <div key={f} className="p-4 border rounded-lg">
            <h4 className="font-semibold text-slate-700">{f}</h4>
            <p className="mt-2 text-xs text-slate-500">A short description about how this feature helps students and colleges in a real-world internship.</p>
          </div>
        ))}
      </div>
    </section>

    {/* Benefits + stakeholders */}
    <section className="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
      <div className="bg-white rounded-2xl p-6 shadow-lg">
        <h3 className="text-xl font-semibold">Benefits</h3>
        <ul className="mt-4 space-y-2 text-sm text-slate-600">
          {benefits.map((b) => (
            <li key={b} className="flex items-start gap-3">
              <div className="w-6 h-6 bg-blue-600 text-white rounded-full flex items-center justify-center text-xs">✓</div>
              <div>{b}</div>
            </li>
          ))}
        </ul>
      </div>

      <div className="bg-white rounded-2xl p-6 shadow-lg">
        <h3 className="text-xl font-semibold">Stakeholders</h3>
        <div className="mt-3 text-sm text-slate-600">
          <p><strong>Students:</strong> Apply, log work, learn skills.</p>
          <p className="mt-2"><strong>Colleges:</strong> Mentor, verify, integrate credits.</p>
          <p className="mt-2"><strong>Industry:</strong> Post internships, evaluate interns, provide feedback.</p>
          <p className="mt-2"><strong>Government/NGOs:</strong> Support pilot & scaling.</p>
        </div>
      </div>
    </section>

    {/* Team */}
    <section id="team" className="bg-white rounded-2xl p-6 shadow-lg mb-12">
      <h3 className="text-2xl font-semibold text-slate-800">Team</h3>
      <div className="mt-4 flex flex-wrap gap-3">
        {team.map((m) => (
          <div key={m} className="px-4 py-2 bg-blue-50 rounded-full text-sm text-slate-700">{m}</div>
        ))}
      </div>
      <div className="mt-4 text-sm text-slate-600">Category: <strong>Software</strong> · Theme: <strong>Smart Education</strong></div>
    </section>

    {/* Call to action / Contact */}
    <section id="contact" className="bg-white rounded-2xl p-6 shadow-lg mb-16 flex flex-col md:flex-row items-center justify-between gap-4">
      <div>
        <h4 className="text-lg font-semibold">Interested to pilot Prashiskshan at your college?</h4>
        <p className="mt-2 text-sm text-slate-600">Contact the Directorate of Colleges, Higher Education Department or reach out to Team Prashiskshan.</p>
      </div>
      <div className="flex gap-3">
        <a href="#" className="px-4 py-2 bg-blue-600 text-white rounded-md">Contact Us</a>
        <a href="#" className="px-4 py-2 border border-slate-200 rounded-md">Download One-Pager</a>
      </div>
    </section>
  </main>

  <footer className="bg-slate-900 text-white py-6 mt-8">
    <div className="max-w-6xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-4">
      <div className="text-sm">© 2025 KPRIT (UGC Autonomous) — Prashiskshan | Designed by Team Prashiskshan</div>
      <div className="text-sm">Department: Directorate of Colleges, Higher Education Department</div>
    </div>
  </footer>
</div>

); }
