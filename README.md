import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mic, PlayCircle, UploadCloud } from "lucide-react";

export default function Home() {
  return (
    <main className="min-h-screen bg-black text-white p-6 font-sans">
      <section className="text-center mb-10">
        <h1 className="text-5xl font-bold mb-2 text-yellow-400">Premier League Cast 2025/2026</h1>
        <p className="text-lg text-gray-300">Live Podcast | Matchday Reactions | Bold Opinions</p>
      </section>

      <section className="grid gap-6 md:grid-cols-3">
        {[1, 2, 3].map((ep) => (
          <Card key={ep} className="bg-zinc-900 border border-yellow-500">
            <CardContent className="p-5">
              <h2 className="text-2xl font-semibold text-yellow-300 mb-2">Episode {ep}</h2>
              <p className="text-gray-400 text-sm mb-4">Premier League Matchday {ep} Analysis & Commentary</p>
              <Button className="bg-yellow-500 text-black w-full">
                <PlayCircle className="mr-2" size={20} /> Listen Now
              </Button>
            </CardContent>
          </Card>
        ))}
      </section>

      <section className="mt-12 text-center">
        <h2 className="text-3xl font-bold mb-4 text-yellow-400">Upload New Episode</h2>
        <div className="flex flex-col md:flex-row gap-4 justify-center items-center">
          <input type="file" className="file:bg-yellow-400 file:text-black file:px-4 file:py-2 file:rounded-md" />
          <Button className="bg-yellow-500 text-black">
            <UploadCloud className="mr-2" size={20} /> Upload
          </Button>
        </div>
      </section>

      <footer className="mt-16 text-center text-gray-500 text-sm">
        &copy; 2025 Premier League Cast. Built by Abdiwahab.
      </footer>
    </main>
  );
}

