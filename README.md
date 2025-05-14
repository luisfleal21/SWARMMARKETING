import { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import { RocketIcon, UsersIcon, GlobeIcon, MailIcon } from "lucide-react";

const translations = {
  es: {
    title: "Swarm Marketing",
    subtitle: "Campañas masivas y coordinadas con microinfluencers que actúan como una colonia de hormigas. Impacto real, costos bajos, alcance viral.",
    requestCampaign: "Solicita tu campaña",
    microInfluencers: "Microinfluencers Coordinados",
    microInfluencersDesc: "Decenas o cientos de voces alineadas promoviendo tu marca en sincronía.",
    viralReach: "Alcance Viral",
    viralReachDesc: "Las acciones pequeñas se multiplican como una reacción en cadena.",
    smartSegmentation: "Segmentación Inteligente",
    smartSegmentationDesc: "Impacta justo donde importa gracias a nuestra red y análisis de datos.",
    readyTitle: "¿Listo para activar tu enjambre?",
    readyDesc: "Diseñamos campañas virales desde la lógica colectiva: pequeñas acciones, gran impacto. Te ayudamos a escalar como una colonia eficiente.",
    bookDemo: "Agenda una demo",
    testimonials: "Testimonios",
    packages: "Paquetes y Precios",
    basic: "Básico",
    professional: "Profesional",
    full: "Enjambre Total",
    basicDesc: "Hasta 50 microinfluencers",
    professionalDesc: "Hasta 150 microinfluencers + análisis de datos",
    fullDesc: "Campaña viral con más de 300 microinfluencers",
    contact: "Contáctanos",
    contactDesc: "¿Tienes dudas o una idea especial en mente? Escríbenos y nuestro equipo te responderá en menos de 24 horas.",
    sendMsg: "Enviar mensaje",
  },
  en: {
    title: "Swarm Marketing",
    subtitle: "Massive and coordinated campaigns with micro-influencers acting like an ant colony. Real impact, low costs, viral reach.",
    requestCampaign: "Request your campaign",
    microInfluencers: "Coordinated Micro-influencers",
    microInfluencersDesc: "Dozens or hundreds of aligned voices promoting your brand in sync.",
    viralReach: "Viral Reach",
    viralReachDesc: "Small actions multiply like a chain reaction.",
    smartSegmentation: "Smart Segmentation",
    smartSegmentationDesc: "Impact where it matters with our network and data analysis.",
    readyTitle: "Ready to activate your swarm?",
    readyDesc: "We design viral campaigns using collective logic: small actions, big impact. Let us help you scale like an efficient colony.",
    bookDemo: "Book a demo",
    testimonials: "Testimonials",
    packages: "Packages & Pricing",
    basic: "Basic",
    professional: "Professional",
    full: "Total Swarm",
    basicDesc: "Up to 50 micro-influencers",
    professionalDesc: "Up to 150 micro-influencers + data analysis",
    fullDesc: "Viral campaign with over 300 micro-influencers",
    contact: "Contact Us",
    contactDesc: "Got questions or a special idea? Write to us and our team will respond within 24 hours.",
    sendMsg: "Send message",
  },
  it: {
    title: "Swarm Marketing",
    subtitle: "Campagne massicce e coordinate con micro-influencer che agiscono come una colonia di formiche. Impatto reale, costi bassi, portata virale.",
    requestCampaign: "Richiedi la tua campagna",
    microInfluencers: "Micro-influencer Coordinati",
    microInfluencersDesc: "Decine o centinaia di voci allineate che promuovono il tuo marchio in sincronia.",
    viralReach: "Portata Virale",
    viralReachDesc: "Le piccole azioni si moltiplicano come una reazione a catena.",
    smartSegmentation: "Segmentazione Intelligente",
    smartSegmentationDesc: "Impatta dove conta grazie alla nostra rete e analisi dei dati.",
    readyTitle: "Pronto ad attivare lo sciame?",
    readyDesc: "Progettiamo campagne virali basate sulla logica collettiva: piccole azioni, grande impatto. Ti aiutiamo a crescere come una colonia efficiente.",
    bookDemo: "Prenota una demo",
    testimonials: "Testimonianze",
    packages: "Pacchetti e Prezzi",
    basic: "Base",
    professional: "Professionale",
    full: "Sciame Totale",
    basicDesc: "Fino a 50 micro-influencer",
    professionalDesc: "Fino a 150 micro-influencer + analisi dei dati",
    fullDesc: "Campagna virale con oltre 300 micro-influencer",
    contact: "Contattaci",
    contactDesc: "Hai domande o un'idea speciale? Scrivici e il nostro team risponderà entro 24 ore.",
    sendMsg: "Invia messaggio",
  },
};

export default function SwarmMarketingHome() {
  const [lang, setLang] = useState("es");
  const t = translations[lang];

  return (
    <div className="min-h-screen bg-white text-gray-900 p-8">
      <div className="flex justify-end mb-4">
        <select value={lang} onChange={(e) => setLang(e.target.value)} className="border border-gray-300 rounded px-3 py-1">
          <option value="es">Español</option>
          <option value="en">English</option>
          <option value="it">Italiano</option>
        </select>
      </div>

      <header className="text-center mb-16">
        <h1 className="text-5xl font-bold mb-4">{t.title}</h1>
        <p className="text-xl text-gray-600 max-w-xl mx-auto">{t.subtitle}</p>
        <Button className="mt-6 text-lg px-6 py-4" asChild>
          <a href="https://wa.me/584121745975">{t.requestCampaign}</a>
        </Button>
      </header>

      <section className="grid grid-cols-1 md:grid-cols-3 gap-6 mb-20">
        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-md p-6">
            <CardContent className="flex flex-col items-center text-center">
              <UsersIcon className="h-10 w-10 text-blue-600 mb-4" />
              <h3 className="text-xl font-semibold">{t.microInfluencers}</h3>
              <p className="text-gray-600 mt-2">{t.microInfluencersDesc}</p>
            </CardContent>
          </Card>
        </motion.div>

        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-md p-6">
            <CardContent className="flex flex-col items-center text-center">
              <RocketIcon className="h-10 w-10 text-green-600 mb-4" />
              <h3 className="text-xl font-semibold">{t.viralReach}</h3>
              <p className="text-gray-600 mt-2">{t.viralReachDesc}</p>
            </CardContent>
          </Card>
        </motion.div>

        <motion.div whileHover={{ scale: 1.05 }}>
          <Card className="rounded-2xl shadow-md p-6">
            <CardContent className="flex flex-col items-center text-center">
              <GlobeIcon className="h-10 w-10 text-purple-600 mb-4" />
              <h3 className="text-xl font-semibold">{t.smartSegmentation}</h3>
              <p className="text-gray-600 mt-2">{t.smartSegmentationDesc}</p>
            </CardContent>
          </Card>
        </motion.div>
      </section>

      <section className="text-center mb-20">
        <h2 className="text-3xl font-bold mb-4">{t.readyTitle}</h2>
        <p className="text-lg text-gray-600 mb-6 max-w-2xl mx-auto">{t.readyDesc}</p>
        <Button className="text-lg px-6 py-4" asChild>
          <a href="https://wa.me/584121745975">{t.bookDemo}</a>
        </Button>
      </section>

      <section className="mb-20">
        <h2 className="text-3xl font-bold text-center mb-8">{t.testimonials}</h2>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
          <Card className="p-6 shadow-md rounded-2xl">
            <CardContent>
              <p className="text-gray-700 italic">“Gracias a Swarm Marketing, pudimos posicionar nuestra marca en redes sociales sin pagar cifras absurdas. ¡Fue como magia colectiva!”</p>
              <p className="mt-4 font-semibold">— Carla Ruiz, Fundadora de EcoVida</p>
            </CardContent>
          </Card>

          <Card className="p-6 shadow-md rounded-2xl">
            <CardContent>
              <p className="text-gray-700 italic">“Una red organizada de microinfluencers es mucho más poderosa de lo que imaginamos. Swarm lo hace posible.”</p>
              <p className="mt-4 font-semibold">— Andrés Mejía, Director Creativo</p>
            </CardContent>
          </Card>

          <Card className="p-6 shadow-md rounded-2xl">
            <CardContent>
              <p className="text-gray-700 italic">“¡La viralidad que logramos fue impresionante! Lo recomendaría a cualquier startup.”</p>
              <p className="mt-4 font-semibold">— Lucía Fernández, CEO de AppFlow</p>
            </CardContent>
          </Card>
        </div>
      </section>

      <section className="mb-20">
        <h2 className="text-3xl font-bold text-center mb-8">{t.packages}</h2>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6 text-center">
          <Card className="p-6 shadow-md rounded-2xl border-2 border-blue-600">
            <CardContent>
              <h3 className="text-2xl font-semibold mb-2">{t.basic}</h3>
              <p className="text-gray-600 mb-4">{t.basicDesc}</p>
              <p className="text-2xl font-bold text-blue-600">$500 USD</p>
            </CardContent>
          </Card>

          <Card className="p-6 shadow-md rounded-2xl border-2 border-green-600">
            <CardContent>
              <h3 className="text-2xl font-semibold mb-2">{t.professional}</h3>
              <p className="text-gray-600 mb-4">{t.professionalDesc}</p>
              <p className="text-2xl font-bold text-green-600">$1,200 USD</p>
            </CardContent>
          </Card>

          <Card className="p-6 shadow-md rounded-2xl border-2 border-purple-600">
            <CardContent>
              <h3 className="text-2xl font-semibold mb-2">{t.full}</h3>
              <p className="text-gray-600 mb-4">{t.fullDesc}</p>
              <p className="text-2xl font-bold text-purple-600">$2,500 USD</p>
            </CardContent>
          </Card>
        </div>
      </section>

      <section className="text-center">
        <h2 className="text-3xl font-bold mb-4">{t.contact}</h2>
        <p className="text-lg text-gray-600 mb-6 max-w-xl mx-auto">{t.contactDesc}</p>
        <Button className="text-lg px-6 py-4 flex items-center gap-2 mx-auto" asChild>
          <a href="https://wa.me/584121745975"> <MailIcon className="h-5 w-5" /> {t.sendMsg}</a>
        </Button>
      </section>
    </div>
  );
}
