
My portfolio website 
import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Mail, Phone, Globe } from "lucide-react";

const Portfolio = () => { return ( <div className="p-6 max-w-5xl mx-auto space-y-10"> <header className="text-center"> <h1 className="text-4xl font-bold">[Your Name]</h1> <p className="text-xl text-gray-600 mt-2">Graphic Designer</p> <p className="mt-4 max-w-xl mx-auto text-gray-500"> Passionate about turning ideas into beautiful and impactful designs. I specialize in branding, digital illustrations, and social media content. </p> </header>

<section>
    <h2 className="text-2xl font-semibold mb-4">Services I Offer</h2>
    <ul className="grid grid-cols-2 md:grid-cols-3 gap-4 text-gray-700">
      <li>Logo Design & Branding</li>
      <li>Social Media Creatives</li>
      <li>Posters, Flyers & Brochures</li>
      <li>Website Banners & Ads</li>
      <li>Infographics</li>
      <li>Packaging Design</li>
    </ul>
  </section>

  <section>
    <h2 className="text-2xl font-semibold mb-4">Tools I Use</h2>
    <div className="flex flex-wrap gap-4 text-gray-600">
      {['Photoshop', 'Illustrator', 'InDesign', 'Figma', 'Canva Pro', 'CorelDRAW'].map(tool => (
        <span key={tool} className="bg-gray-100 px-3 py-1 rounded-full text-sm">{tool}</span>
      ))}
    </div>
  </section>

  <section>
    <h2 className="text-2xl font-semibold mb-4">Portfolio Showcase</h2>
    <div className="grid md:grid-cols-2 gap-6">
      {[
        {
          title: 'Branding – Café Mocha',
          description: 'Logo, packaging, and brand identity for a cozy café.',
        },
        {
          title: 'Social Media Campaign – Fitness Brand',
          description: 'Energetic social media graphics for a health brand.',
        },
        {
          title: 'Event Poster – Music Fest 2024',
          description: 'Poster and ticket designs with vibrant neon style.',
        },
        {
          title: 'Illustration – Book Cover Design',
          description: 'Fantasy novel cover with hand-drawn elements.',
        },
      ].map((project, idx) => (
        <Card key={idx}>
          <CardContent className="p-4">
            <h3 className="text-lg font-semibold">{project.title}</h3>
            <p className="text-sm text-gray-600 mt-2">{project.description}</p>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  <section>
    <h2 className="text-2xl font-semibold mb-4">Testimonials</h2>
    <div className="space-y-4 text-gray-700">
      <blockquote className="italic">“Working with [Your Name] was a breeze. Her designs elevated our brand!” – Client A</blockquote>
      <blockquote className="italic">“Creative, punctual, and easy to collaborate with.” – Client B</blockquote>
    </div>
  </section>

  <footer className="text-center mt-10">
    <h2 className="text-xl font-semibold mb-2">Let’s Work Together</h2>
    <div className="flex justify-center gap-6 text-gray-600">
      <div className="flex items-center gap-2">
        <Mail className="w-4 h-4" />
        <span>your.email@example.com</span>
      </div>
      <div className="flex items-center gap-2">
        <Phone className="w-4 h-4" />
        <span>+91 XXXXX XXXXX</span>
      </div>
      <div className="flex items-center gap-2">
        <Globe className="w-4 h-4" />
        <span>behance.net/yourprofile</span>
      </div>
    </div>
  </footer>
</div>

); };

export default Portfolio;

