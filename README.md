db.buku.bulkWrite([
  {
    insertOne: {
      document: {
        judul: "Pemrograman Python",
        penulis: "Andi",
        tahun: 2023,
        kategori: "Teknologi",
        stok: 5
      }
    }
  },
  {
    updateOne: {
      filter: { judul: "Algoritma Dasar" },
      update: { $set: { stok: 10 } }
    }
  },
  {
    deleteOne: {
      filter: { judul: "Statistik Lanjut" }
    }
  }
]);
