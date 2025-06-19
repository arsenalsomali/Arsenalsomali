import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Mic, Play, UploadCloud } from "lucide-react";

export default function PremierLeaguePodcast() {
  return (
    <main className="min-h-screen bg-black text-white font-sans px-6 py-10">
      <header className="text-center mb-10">
        <h1 className="text-5xl font-bold uppercase tracking-wide text-red-600">
          Premier League Cast
        </h1>
        <p className="mt-4 text-lg text-gray-300">
          Podcast Every Premier League Game – 2025/2026 Season
        </p>
      </header>

      <section className="grid md:grid-cols-2 gap-8">
        <Card className="bg-gray-900 text-white shadow-lg">
          <CardContent className="p-6">
            <h2 className="text-2xl font-bold mb-4">🎙️ Latest Episodes</h2>
            <div className="space-y-4">
              <div className="bg-gray-800 p-4 rounded-lg flex items-center justify-between">
                <span>Man City vs Arsenal - Matchday 1</span>
                <Button className="bg-red-600 hover:bg-red-700">
                  <Play className="mr-2 h-4 w-4" /> Play
                </Button>
              </div>
              <div className="bg-gray-800 p-4 rounded-lg flex items-center justify-between">
                <span>Man Utd vs Chelsea - Matchday 1</span>
                <Button className="bg-red-600 hover:bg-red-700">
                  <Play className="mr-2 h-4 w-4" /> Play
                </Button>
              </div>
            </div>
          </CardContent>
        </Card>

        <Card className="bg-gray-900 text-white shadow-lg">
          <CardContent className="p-6">
            <h2 className="text-2xl font-bold mb-4">🔴 Upload New Episode</h2>
            <div className="space-y-4">
              <Input type="text" placeholder="Episode Title" className="bg-gray-800 text-white" />
              <Input type="file" className="bg-gray-800 text-white" />
              <Button className="bg-green-600 hover:bg-green-700 w-full">
                <UploadCloud className="mr-2 h-4 w-4" /> Upload
              </Button>
            </div>
          </CardContent>
        </Card>
      </section>

      <footer className="mt-16 text-center text-gray-500 text-sm">
        &copy; {new Date().getFullYear()} Premier League Cast. All rights reserved.
      </footer>
    </main>
  );
}
