import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Badge } from "@/components/ui/badge";
import { GraduationCap, Briefcase, Code, Award, Phone } from "lucide-react";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900">
      {/* Header */}
      <motion.div
        className="text-center py-10"
        initial={{ opacity: 0, y: -40 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        <h1 className="text-4xl font-bold">👨‍💻 Madhav Pathak</h1>
        <p className="text-lg text-gray-600 mt-2">
          "Turning ideas into scalable digital solutions"
        </p>
      </motion.div>

      {/* Professional Summary */}
      <motion.div
        className="max-w-3xl mx-auto mb-12"
        initial={{ opacity: 0 }}
        whileInView={{ opacity: 1 }}
        transition={{ duration: 1 }}
      >
        <Card className="rounded-2xl shadow-lg p-6 bg-white">
          <CardContent>
            <h2 className="text-2xl font-semibold mb-4">🚀 Professional Summary</h2>
            <p>
              Results-driven Backend Developer with proven expertise in
              <span className="font-semibold"> JavaScript, Node.js, Express.js, and SQL</span>.
              Demonstrated success in improving system performance by{" "}
              <Badge>25%</Badge> and optimizing database queries for{" "}
              <Badge>40%</Badge> faster results.
            </p>
          </CardContent>
        </Card>
      </motion.div>

      {/* Education */}
      <motion.div
        className="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-5xl mx-auto mb-12"
        initial={{ opacity: 0, y: 40 }}
        whileInView={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        <Card className="bg-gradient-to-r from-indigo-50 to-white shadow-md">
          <CardContent className="text-center p-6">
            <GraduationCap className="mx-auto text-indigo-600 w-10 h-10" />
            <h3 className="text-lg font-semibold mt-2">🎯 Current</h3>
            <p>MCA @ KIIT (2025 - 2027)</p>
          </CardContent>
        </Card>
        <Card className="bg-gradient-to-r from-green-50 to-white shadow-md">
          <CardContent className="text-center p-6">
            <GraduationCap className="mx-auto text-green-600 w-10 h-10" />
            <h3 className="text-lg font-semibold mt-2">🏆 Completed</h3>
            <p>BCA @ Chandigarh University (2022 - 2025)</p>
          </CardContent>
        </Card>
      </motion.div>

      {/* Experience */}
      <motion.div
        className="max-w-5xl mx-auto space-y-6 mb-12"
        initial={{ opacity: 0 }}
        whileInView={{ opacity: 1 }}
        transition={{ duration: 0.8 }}
      >
        <h2 className="text-2xl font-semibold text-center mb-6">💼 Professional Experience</h2>

        <Card className="p-6 shadow-lg hover:shadow-xl transition rounded-2xl">
          <CardContent>
            <h3 className="text-xl font-bold">🔥 Seagro - Backend Developer</h3>
            <p className="text-gray-600">May 2025 - Jun 2025</p>
            <ul className="list-disc ml-5 mt-3 space-y-1">
              <li>99.9% uptime with 30% faster response times</li>
              <li>Optimized SQL queries by 40%</li>
              <li>Built APIs handling 10,000+ requests/day</li>
              <li>Implemented JWT-based authentication</li>
            </ul>
          </CardContent>
        </Card>

        <Card className="p-6 shadow-lg hover:shadow-xl transition rounded-2xl">
          <CardContent>
            <h3 className="text-xl font-bold">🌱 Organic by Pooja - Full Stack Developer (Internship)</h3>
            <p className="text-gray-600">Aug 2024 - Sept 2024</p>
            <ul className="list-disc ml-5 mt-3 space-y-1">
              <li>40% improved transaction efficiency</li>
              <li>Built robust API endpoints (500+ daily requests)</li>
              <li>Integrated PhonePe payment gateway</li>
            </ul>
          </CardContent>
        </Card>
      </motion.div>

      {/* Projects */}
      <motion.div
        className="max-w-5xl mx-auto mb-12"
        initial={{ opacity: 0, y: 40 }}
        whileInView={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        <h2 className="text-2xl font-semibold text-center mb-6">🚀 Featured Project</h2>
        <Card className="p-6 rounded-2xl shadow-lg">
          <CardContent className="grid md:grid-cols-2 gap-6">
            <div>
              <h3 className="text-xl font-bold">🍽️ Satvik Meals - Healthy Food Delivery Startup</h3>
              <ul className="list-disc ml-5 mt-3 space-y-1">
                <li>Founded and built a complete platform (React, Node.js, SQL)</li>
                <li>Real-time delivery tracking & subscriptions</li>
                <li>Secure payment integration</li>
              </ul>
            </div>
            <div className="bg-gray-50 p-4 rounded-xl">
              <p>📈 Scaled platform successfully</p>
              <p>🤝 Strong client relationships</p>
              <p>🔄 High user retention</p>
            </div>
          </CardContent>
        </Card>
      </motion.div>

      {/* Contact */}
      <motion.div
        className="text-center py-10"
        initial={{ opacity: 0 }}
        whileInView={{ opacity: 1 }}
        transition={{ duration: 1 }}
      >
        <Phone className="mx-auto w-10 h-10 text-indigo-600" />
        <h2 className="text-2xl font-bold mt-4">📞 Let’s Connect</h2>
        <p className="text-gray-600 mt-2">
          Always open to discussing new opportunities and innovative projects!
        </p>
        <Button className="mt-4">⭐ Star My Work</Button>
      </motion.div>
    </div>
  );
}
