import Image from "next/image";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mail, Phone, MapPin, Fax } from "lucide-react";
import { motion } from "framer-motion";

export default function EnvorsHome() {
  return (
    <div className="min-h-screen bg-white text-gray-800">
      {/* Header */}
      <header className="bg-gray-900 text-white p-6 shadow-md">
        <div className="max-w-7xl mx-auto flex justify-between items-center">
          <div className="flex items-center gap-4">
            <Image src="/회사로고_큰이미지_투명.png" alt="Envors Logo" width={120} height={40} />
            <h1 className="text-2xl font-bold hidden md:block">Envors</h1>
          </div>
          <nav className="space-x-6">
            <a href="#about" className="hover:underline">회사소개</a>
            <a href="#products" className="hover:underline">제품소개</a>
            <a href="#contact" className="hover:underline">문의하기</a>
          </nav>
        </div>
      </header>

      {/* Hero Section */}
      <section className="bg-blue-100 py-20 text-center">
        <motion.h2 className="text-4xl font-bold mb-4" initial={{ opacity: 0, y: 20 }} animate={{ opacity: 1, y: 0 }}>대기환경을 위한 정밀한 측정기</motion.h2>
        <p className="text-lg max-w-xl mx-auto">Envors는 대기질 모니터링 장비를 연구 및 제조하는 전문 기업입니다.</p>
      </section>

      {/* About Section */}
      <section id="about" className="py-16 px-4 max-w-5xl mx-auto">
        <h3 className="text-3xl font-semibold mb-4">회사 소개</h3>
        <p>
          Envors는 환경을 위한 기술 혁신을 통해 더 깨끗한 공기와 건강한 삶을 추구합니다.
          정밀한 측정기와 지속 가능한 솔루션으로 국내외 대기질 개선에 기여하고 있습니다.
        </p>
      </section>

      {/* Products Section */}
      <section id="products" className="bg-gray-100 py-16 px-4">
        <div className="max-w-6xl mx-auto">
          <h3 className="text-3xl font-semibold mb-8 text-center">제품 소개</h3>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
            <Card>
              <CardContent className="p-4">
                <h4 className="text-xl font-semibold mb-2">미세먼지 센서 (PM2.5)</h4>
                <p>고정밀 레이저 기반 센서로 PM2.5 및 PM10을 실시간 측정합니다.</p>
              </CardContent>
            </Card>
            <Card>
              <CardContent className="p-4">
                <h4 className="text-xl font-semibold mb-2">VOC 측정기</h4>
                <p>휘발성 유기화합물(VOC)을 정밀하게 감지하여 실내외 환경을 관리합니다.</p>
              </CardContent>
            </Card>
            <Card>
              <CardContent className="p-4">
                <h4 className="text-xl font-semibold mb-2">이동형 대기측정 장비</h4>
                <p>다양한 센서를 통합한 이동형 솔루션으로 현장 모니터링에 적합합니다.</p>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-16 px-4 max-w-4xl mx-auto">
        <h3 className="text-3xl font-semibold mb-6">문의하기</h3>
        <div className="space-y-4">
          <div className="flex items-center gap-2">
            <Mail className="w-5 h-5" />
            <span>envpower@envors.com</span>
          </div>
          <div className="flex items-center gap-2">
            <Phone className="w-5 h-5" />
            <span>042-635-9947 / 010-9566-4445</span>
          </div>
          <div className="flex items-center gap-2">
            <Fax className="w-5 h-5" />
            <span>042-635-9948</span>
          </div>
          <div className="flex items-center gap-2">
            <MapPin className="w-5 h-5" />
            <span>34417 대전광역시 대덕구 비래서로 11, 엔버스B/D (비래동)</span>
          </div>
        </div>
        <Button className="mt-6">이메일 보내기</Button>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-white text-center py-6 mt-10">
        <p>&copy; 2025 Envors. All rights reserved.</p>
      </footer>
    </div>
  );
}
