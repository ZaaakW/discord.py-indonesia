# Discord Python Indonesia

<p align="center">
  <a href="https://github.com/ZaaakW/discord.py-indonesia/releases"><img src="https://img.shields.io/github/v/release/ZaaakW/discord.py-indonesia"></a>
  <a href="https://github.com/ZaaakW/discord.py-indonesia/commits/main"><img src="https://img.shields.io/github/last-commit/ZaaakW/discord.py-indonesia"></a>
  <a href="https://github.com/ZaaakW/discord.py-indonesia/blob/main/LICENSE.md"><img src="https://img.shields.io/github/license/ZaaakW/discord.py-indonesia"></a>
  <a href="https://github.com/ZaaakW/discord.py-indonesia"><img src="https://img.shields.io/github/languages/code-size/ZaaakW/discord.py-indonesia"></a>
  <a href="https://conventionalcommits.org/en/v1.0.0/"><img src="https://img.shields.io/badge/Conventional%20Commits-1.0.0-%23FE5196?logo=conventionalcommits&logoColor=white"></a>
</p>

Repositori ini adalah templat yang dapat digunakan semua orang untuk memulai membuat bot Discord.

Ketika saya pertama kali mulai membuat bot Discord, saya butuh beberapa saat untuk menyiapkan semuanya dan bekerja dengan cogs dan banyak lagi.
Saya akan senang jika ada template apa pun. Namun, tidak ada template yang ada. Itu sebabnya saya
memutuskan untuk membuat template saya sendiri agar **kalian** membuat bot Discord dengan mudah.

Harap dicatat bahwa template ini tidak seharusnya menjadi template terbaik, tetapi template yang bagus untuk mulai mempelajari caranya
discord.py berfungsi dan membuat bot Kamu sendiri dengan mudah.

Jika kamu berencana menggunakan templat ini untuk membuat templat atau bot Kamu sendiri, Kamu **harus**:

- Simpan kreditnya, dan tautan ke repositori ini di semua file yang berisi kode saya
- Pertahankan lisensi yang sama untuk kode yang tidak diubah

Lihat [file lisensi](https://github.com/kZaaakW/discord.py-indonesia/blob/master/LICENSE.md) untuk mengetahui lebih lanjut
informasi, saya berhak menghapus repositori apa pun yang tidak memenuhi persyaratan ini.

## Dukungan

Sebelum meminta dukungan, perlu diketahui bahwa templat ini mengharuskan kamu memiliki setidaknya pengetahuan dasar tentang Python dan pustakanya dirancang untuk pengguna tingkat lanjut. Jangan gunakan templat ini jika kamu tidak memahami dasar-dasarnya atau beberapa topik lanjutan seperti OOP atau async. Berikut tautan sumber daya untuk mempelajari Python.

Jika kamu memerlukan bantuan, jangan ragu untuk mengajukan masalah [di sini](https://discord.gg/NntdTNhFKh), tetapi jangan lupa untuk membaca FAQ sebelumnya.

## Gimana cara downloadnya?

1. Klone dengan menggunakan git:

   ```
   git clone https://github.com/ZaaakW/discord.py-indonesia.git
   cd discord.py-indonesia
   ```

2. Instal dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Konfigurasi environment:

    edit file di `.env.example` dan ubah nama jadi `.env`
    dan masukan api token discord bot dan database:
    ```
    DISCORD_TOKEN=YOUR_TOKEN_DISCORD_BOT
    DATABASE_HOST=YOUR_HOST
    DATABASE_PORT=YOUR_PORT
    DATABASE_USER=YOUR_USER
    DATABASE_PASSWORD=YOUR_PASSWORD
    DATABASE_NAME=YOUR_DATABASE 
    ```

    > **Note:** cara mendapatkan token bot [disini](https://discord.com/developers/applications) dan untuk database kamu bisa dengan menggunakan [supabase](https://supabase.com) atau dengan postgres lokal

4. Jalankan bot:

    ```bash
    python main.py
    ```

## Membuat Cog Baru

buatlah di `cogs/nama_cog` setelah itu isi dibawah ini untuk contoh penggunan simplenya:

   ```python
    import discord
    from discord.ext import commands

    class Example(commands.Cog):
       def __init__(self, bot):
           self.bot = bot

       @commands.command()
       async def hello(self, ctx):
           await ctx.send('Hello from Example!')

    async def setup(bot: commands.Bot):
        await bot.add_cog(Example(bot))
   ```

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=ZaaakW/discord.py-indonesia.git&type=Date)](https://www.star-history.com/#ZaaakW/discord.py-indonesia.git&Date)

## License  
Project ini menggunakan MIT Lisensi - untuk melihat detail lisensi [LICENSE.md](https://github.com/ZaaakW/discord.py-indonesia/blob/main/LICENSE.md)