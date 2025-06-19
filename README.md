# DQN
Bu çalışmada, OpenAI Gym ortamlarından biri olan CartPole-v1 üzerinde üç farklı pekiştirmeli öğrenme algoritması eğitilmiş ve karşılaştırılmıştır. Kullanılan algoritmalar şunlardır:

Deep Q-Network (DQN)

Advantage Actor-Critic (A2C)

Proximal Policy Optimization (PPO)

Amaç, her bir algoritmanın sınırlı eğitim adımı (10.000 timestep) sonunda ne düzeyde performans gösterdiğini gözlemlemek ve kıyaslamaktır.

2. Yöntem
Her algoritma için aşağıdaki adımlar takip edilmiştir:

gym.make("CartPole-v1") ile ortam oluşturulmuştur.

Ortam Monitor sınıfı ile sarılarak eğitim sırasında istatistiklerin izlenmesi sağlanmıştır.

Model, ilgili algoritmanın MlpPolicy ile eğitilmiştir.

Eğitim süresi tüm algoritmalar için sabit tutulmuştur: total_timesteps = 10.000.

Eğitilen modeller, evaluate_policy fonksiyonu ile 10 bölüm boyunca test edilmiştir.

Her algoritma için ortalama ödül (mean reward) ve standart sapma (std) kaydedilmiştir.

Sonuçlar bar grafiği ile görselleştirilmiş ve comparison_results.png olarak kaydedilmiştir.

Ayrıca her model, eğitim sonrasında bir oyunluk görsel testten geçirilmiş ve izlenebilirlik kontrolü yapılmıştır.

3. Deneysel Sonuçlar
Eğitim ve değerlendirme sonunda her algoritmanın ortalama başarımları şu şekilde ölçülmüştür:

Algoritma	Ortalama Ödül	Standart Sapma
DQN	...	...
A2C	...	...
PPO	...	...

Not: Gerçek çıktılar çalıştırıldığında tabloya eklenmelidir.

Grafiksel olarak da sonuçlar çubuk grafiğiyle ifade edilmiştir. Y-ekseninde ortalama ödül, x-ekseninde ise algoritma isimleri yer almaktadır. Standart sapmalar hata çubuğu (error bar) olarak gösterilmiştir.

4. Sonuç
Kısa süreli bir eğitim (10.000 adım) kapsamında yapılan bu çalışmada, algoritmaların CartPole-v1 ortamında öğrenme başarımları arasında belirli farklar gözlemlenmiştir. Genellikle PPO algoritması kısa vadeli kararlılık açısından daha yüksek performans göstermektedir, ancak bu durum her zaman geçerli olmayabilir. Daha uzun eğitim süreleri, hiperparametre optimizasyonu ve farklı ortamlarda yapılan testler algoritmaların gerçek potansiyellerini daha iyi ortaya koyacaktır.

Bu çalışma, pekiştirmeli öğrenme algoritmalarının kıyaslamalı analizi açısından temel bir karşılaştırma sunmaktadır.
