# Datamining_Final_Presentation
Tahapan dalam Notebook:

Phase 1 Data Understanding & Preprocessing: pembersihan data, penanganan missing value, feature selection (korelasi, mutual information, entropy/information gain), feature engineering.

Phase 2 Segmentation via Clustering: K-Means (K=4) menghasilkan 4 segmen nasabah Credit-Reliant Customers, Low-Engagement Customers, Affluent Active Spenders, Affluent Conservative Savers.

Phase 3 Association Rule Mining: Apriori untuk menemukan pola antar-atribut nasabah (usia, tenor pinjaman, jenis transaksi, dll).

Phase 4 Anomaly & Outlier Detection: kombinasi IQR, Z-score, dan Isolation Forest, dengan cross-reference ke hasil clustering Phase 2.

Phase 5 Visualization & Knowledge Presentation: dashboard interaktif (Plotly Dash) dengan filter global, peta segmentasi, ranking kota, jaringan aturan asosiasi, dan detail anomali.

Cara Menjalankan:
1. Kebutuhan environment
pip install dash plotly pandas numpy scikit-learn networkx mlxtend

2. Jalankan notebook
Buka DataMining_Dashboard_FinalProject.ipynb di Jupyter/Colab, lalu jalankan seluruh cell dari atas ke bawah secara berurutan:
Cell pertama menginstall/uninstall dash versi yang dibutuhkan, setelah cell ini selesai, restart runtime satu kali, baru jalankan ulang seluruh notebook dari awal. Ini mencegah error module not found akibat versi dash lama masih terpakai di tengah proses.
Cell dashboard (Plotly Dash) berada di bagian paling akhir notebook (Phase 5), jalankan setelah cell "Setup — Rekap & Konsolidasi Phase 1–4" agar variabel yang dibutuhkan (df, top15_rules, rules_pool, city_agg, centroids_pca, cluster_names) sudah tersedia.

3. Akses dashboard
Setelah cell dashboard dijalankan, Dash akan menampilkan link lokal (biasanya http://127.0.0.1:8050) buka link tersebut di browser.
