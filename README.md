Tugas 05: Transfer Learning untuk Klasifikasi Citra dengan Data Terbatas

Dataset: Oxford-IIIT Pet (subset 10 kelas: 5 kucing, 5 anjing), split stratified 70/15/15. Model: ResNet-18 (ImageNet pretrained) dan EfficientNet-B0 (bonus).

Cara menjalankan
Buka DL_2802501306_GSLC1.ipynb di Google Colab, pilih runtime GPU T4.
Run all cells. Dataset diunduh otomatis lewat torchvision.datasets.OxfordIIITPet.
Hasil tersimpan di folder results/.
Kondisi eksperimen
B1: from scratch
B2: feature extraction (backbone beku)
B3: fine-tuning layer4 + fc (differential learning rate)
B4: B3 tanpa augmentasi vs dengan augmentasi
B5: EfficientNet-B0 (bonus)
Reproduksibilitas

Seed = 42 (Python, NumPy, PyTorch), cuDNN deterministic. Hasil dapat sedikit berbeda antar versi library/GPU.

Struktur
DL_2802501306_GSLC1.ipynb
requirements.txt
results/metrics_summary.csv|json, results/history_*.csv, gambar hasil
laporan.pdf
