# Generative Pretrained Transformers 2 (GPT-2) for Indonesian Instagram Post Caption Generation

GPT-2 adalah suatu model ciptaan OpenAI yang berbasis Transformers, yaitu jenis arsitektur deep learning yang menggunakan mekanisme atensi ([Paper lebih lanjut](https://arxiv.org/abs/1706.03762?amp=1)). GPT-2 sendiri merupakan model yang digunakan dalam tugas text generation. Secara umum, GPT-2 memerlukan proses fine-tuning untuk dapat menjalankan tugas spesifik karena GPT-2 sendiri masih bersifat *general model*. Fine-tuning ini dilakukan dengan melakukan *training* pada dataset yang berbentuk kumpulan teks. Dengan adanya proses ini, diharapkan model GPT-2 mampu menyerupai kemampuan manusia dalam membuat teks (*text generation*).


Pada repository ini, tugas *text generation* yang dilakukan adalah membuat caption Instagram berbahasa Indonesia dengan menggunakan dataset kumpulan caption post Instagram beberapa akun organisasi, himpunan, dan UKM yang ada di Universitas Gadjah Mada. Proses finetuning secara keseluruhan dapat dijabarkan dalam beberapa tahap:

1. Melakukan scraping posting Instagram. Untuk melakukan scraping ini, saya mengunduh secara manual halaman yang akan discrape dengan Instagram for Web karena Instagram cukup ketat dalam mencegah aktivitas bot. Setelah halaman discrape dalam bentuk raw HTML, dilakukan pengolahan data menjadi csv dengan bantuan *library* pandas, BeautifulSoup, dan regex. Hasilnya disimpan dalam bentuk .csv. Detail proses tersebut ada di dalam file `Caption Scraping.ipynb`
2. Melakukan fine-tuning model GPT-2. Model yang akan difinetune dapat diakses [di sini](https://huggingface.co/indonesian-nlp/gpt2-medium-indonesian). Proses finetune dilaksanakan dengan bantuan *library* Transformers. Detail dan hasil model lebih lanjut bisa dilihat di `CaptionFinetuning.ipynb`

Todo:
1. Membuat demo yang berbentuk *self-hosted*
