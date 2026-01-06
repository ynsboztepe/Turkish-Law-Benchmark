# Turkish-Law-Benchmark
Performance analysis of open-source LLMs (Llama-3.1, Gemma-2, Mistral) on Turkish Legal Texts using RAG architecture.

# ⚖️ Turkish Law Benchmark: LLM RAG Analysis

Bu proje, **RAG (Retrieval-Augmented Generation)** mimarisi kullanılarak güçlendirilmiş açık kaynak Büyük Dil Modellerinin (LLM), **Türk Hukuk Mevzuatı** üzerindeki performansını, doğruluk oranlarını ve terminoloji hakimiyetini karşılaştırmalı olarak analiz etmektedir.

## 🚀 Proje Hakkında
Hukuk dili, kendine has terminolojisi ve karmaşık yapısıyla NLP çalışmaları için zorlu bir alandır. Bu çalışmada, modellerin halüsinasyon (uydurma bilgi) riskini minimize etmek ve güncel kanun maddelerine erişimini sağlamak amacıyla **vektör tabanlı bir RAG sistemi** geliştirilmiştir.

Proje kapsamında **Llama-3, Gemma-2 ve Mistral** modelleri; T.C. Anayasası, TCK ve KVKK gibi temel kanunlar üzerinde test edilmiştir.

## 🛠️ Kullanılan Teknolojiler ve Modeller

### 🧠 Büyük Dil Modelleri (LLMs)
Projede "Instruction Tuned" (Talimat Odaklı) şu modeller kullanılmıştır:
* **Meta Llama-3.1-8B-Instruct:** Genel dil yeteneği ve bağlam takibi.
* **Google Gemma-2-9B-IT:** Yüksek muhakeme (reasoning) yeteneği.
* **Mistral-7B-v0.3-Instruct:** Parametre verimliliği ve stabilite.

### 🔍 Embedding & RAG Mimarisi
* **Embedding Modeli:** `BAAI/bge-m3` (Çok dilli, anlamsal bütünlük sağlayan model).
* **Donanım:** NVIDIA A100 GPU (Bfloat16 hassasiyetinde çıkarım).
* **Vektör Arama:** Semantik (anlamsal) eşleştirme ile madde bazlı getirme.

## 📚 Veri Seti (Dataset)
Veriler **T.C. Cumhurbaşkanlığı Mevzuat Bilgi Sistemi** üzerinden çekilmiş ve 9 temel kanun sisteme entegre edilmiştir:
1.  T.C. Anayasası
2.  Türk Ceza Kanunu (TCK)
3.  Ceza Muhakemesi Kanunu (CMK)
4.  Ceza ve Güvenlik Tedbirlerinin İnfazı Hakkında Kanun (CGTİHK)
5.  Kabahatler Kanunu
6.  Türk Medeni Kanunu
7.  Türk Borçlar Kanunu
8.  İş Kanunu
9.  Kişisel Verilerin Korunması Kanunu (KVKK)

## 📊 Sonuçlar ve Gözlemler
Yapılan deneyler sonucunda:
* **Llama-3.1**, Türkçe dil bilgisi ve akıcılık konusunda en dengeli sonuçları vermiştir.
* **Gemma-2**, mantıksal çıkarımlarda güçlü olsa da formatlama (prompt uyumu) konusunda özel optimizasyon gerektirmiştir.
* **RAG Mimarisi**, modellerin halüsinasyon oranını ciddi ölçüde düşürerek kanıta dayalı cevaplar üretmesini sağlamıştır.

## 📂 Kurulum ve Kullanım (Installation)

```bash
# Projeyi klonlayın
git clone [https://github.com/ynsboztepe/Turkish-Law-Benchmark.git](https://github.com/ynsboztepe/Turkish-Law-Benchmark.git)

# Proje dizinine girin
cd Turkish-Law-Benchmark

# Gereksinimleri yükleyin
pip install -r requirements.txt

# Uygulamayı çalıştırın (Örnek)
python main.py
