import React from 'react';
import { Code2, Database, Cloud, Globe, Layers, Sparkles } from 'lucide-react';

export default function TechStackCard() {
  const techStack = [
    {
      category: "Programming Languages",
      icon: <Code2 className="w-5 h-5" />,
      skills: ["C", "Java", "Python"],
      color: "from-emerald-500 to-teal-500"
    },
    {
      category: "Frontend Development",
      icon: <Layers className="w-5 h-5" />,
      skills: ["React", "Vite", "JavaFX"],
      color: "from-green-500 to-emerald-500"
    },
    {
      category: "Backend & Databases",
      icon: <Database className="w-5 h-5" />,
      skills: ["MySQL"],
      color: "from-teal-500 to-cyan-500"
    },
    {
      category: "Cloud & DevOps",
      icon: <Cloud className="w-5 h-5" />,
      skills: ["Docker", "Google Cloud"],
      color: "from-lime-500 to-green-500"
    },
    {
      category: "Web & Blockchain",
      icon: <Globe className="w-5 h-5" />,
      skills: ["Web3.js"],
      color: "from-emerald-500 to-green-600"
    }
  ];

  return (
    <div className="min-h-screen bg-gradient-to-br from-gray-900 via-emerald-900/40 to-teal-900/30 flex items-center justify-center p-6">
      <div className="max-w-4xl w-full">
        {/* Header */}
        <div className="text-center mb-12">
          <div className="inline-flex items-center gap-3 mb-4">
            <div className="relative">
              <div className="absolute inset-0 bg-gradient-to-br from-emerald-500 to-green-600 rounded-xl blur-lg opacity-60 animate-pulse"></div>
              <div className="relative w-12 h-12 bg-gradient-to-br from-emerald-500 to-green-600 rounded-xl flex items-center justify-center shadow-lg shadow-emerald-500/50">
                <Code2 className="w-7 h-7 text-white" />
              </div>
            </div>
            <h1 className="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-emerald-400 to-green-500">
              Tech Stack
            </h1>
          </div>
          <p className="text-gray-400 text-lg flex items-center justify-center gap-2">
            <Sparkles className="w-4 h-4 text-emerald-500" />
            Student Software Developer
            <Sparkles className="w-4 h-4 text-emerald-500" />
          </p>
        </div>

        {/* Tech Stack Grid */}
        <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
          {techStack.map((section, index) => (
            <div
              key={index}
              className="relative group"
            >
              {/* Glowing border effect */}
              <div className="absolute -inset-0.5 bg-gradient-to-r from-emerald-500 to-green-600 rounded-2xl opacity-30 group-hover:opacity-60 blur transition duration-300"></div>
              
              {/* Card content */}
              <div className="relative bg-gray-950/90 backdrop-blur-sm rounded-2xl p-6 border border-emerald-500/30 hover:border-emerald-500/60 transition-all duration-300 hover:transform hover:scale-105 shadow-lg shadow-emerald-900/20">
                {/* Category Header */}
                <div className="flex items-center gap-3 mb-4">
                  <div className={`relative w-10 h-10 bg-gradient-to-br ${section.color} rounded-lg flex items-center justify-center shadow-lg shadow-emerald-500/30`}>
                    {section.icon}
                  </div>
                  <h3 className="text-lg font-semibold text-emerald-100">{section.category}</h3>
                </div>

                {/* Skills */}
                <div className="flex flex-wrap gap-2">
                  {section.skills.map((skill, skillIndex) => (
                    <span
                      key={skillIndex}
                      className="px-4 py-2 bg-emerald-950/50 text-emerald-200 rounded-lg text-sm font-medium border border-emerald-700/40 hover:bg-emerald-900/50 hover:border-emerald-600/60 hover:shadow-lg hover:shadow-emerald-900/30 transition-all duration-200"
                    >
                      {skill}
                    </span>
                  ))}
                </div>
              </div>
            </div>
          ))}
        </div>

        {/* Footer Badge */}
        <div className="mt-12 text-center">
          <div className="relative inline-flex items-center gap-2 px-6 py-3 rounded-full group">
            <div className="absolute inset-0 bg-gradient-to-r from-emerald-600 to-green-600 rounded-full blur opacity-60 group-hover:opacity-80 transition duration-300"></div>
            <div className="relative flex items-center gap-2 bg-gradient-to-r from-emerald-600 to-green-600 px-6 py-3 rounded-full shadow-lg shadow-emerald-500/40">
              <div className="w-2 h-2 bg-green-300 rounded-full animate-pulse shadow-lg shadow-green-300/60"></div>
              <span className="text-white font-medium">Open to Learning & Collaboration</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  );
}
