---
title: Command Avrae
description: Referensi command Avrae yang paling penting untuk bermain D&D di Discord.
tags:
  - Avrae
  - D&D
  - Discord
  - Commands
type: reference
---
Halaman ini berisi command Avrae yang paling sering digunakan dalam permainan D&D. Command dibagi menjadi **Non-Battle** dan **Battle** agar lebih mudah ditemukan.

# 🟢 NON-BATTLE

Command yang digunakan **di luar combat** untuk mengelola character, melakukan dice roll, mencari informasi, dan kebutuhan lainnya.

> [!example]- 🎲 Dice & Rolling
> Command untuk melakukan roll dadu secara manual.
>
> ## `!roll`
>
> Melakukan roll dadu.
>
> **Syntax**
>
> ```text
> !roll <dice>
> ```
>
> **Contoh**
>
> ```text
> !roll 1d20
> !roll 2d6+3
> !roll 1d20+5
> ```
>
> **Shortcut**
>
> ```text
> !r 1d20
> ```
>
> ## Advantage
>
> Melakukan roll **2 kali** dan mengambil hasil yang lebih tinggi.
>
> Gunakan `adv` setelah dice roll.
>
> **Contoh**
>
> ```text
> !roll 1d20 adv
> ```
>
> Shortcut:
>
> ```text
> !r 1d20 adv
> ```
>
> ## Disadvantage
>
> Melakukan roll **2 kali** dan mengambil hasil yang lebih rendah.
>
> Gunakan `dis` setelah dice roll.
>
> **Contoh**
>
> ```text
> !roll 1d20 dis
> ```
>
> Shortcut:
>
> ```text
> !r 1d20 dis
> ```
>
> ## `!rr`
>
> Melakukan multiple roll.
>
> **Contoh**
>
> ```text
> !rr 2 1d20
> ```
>
> > [!tip]
> > Untuk penggunaan sehari-hari, yang paling penting untuk diingat adalah:
> >
> > - `!roll 1d20` → normal roll
> > - `!roll 1d20 adv` → advantage
> > - `!roll 1d20 dis` → disadvantage
> > - `!r` → shortcut dari `!roll`

> [!example]- 🧙 Character
> Command untuk mengatur dan menggunakan character aktif.
>
> ## `!character`
>
> Melihat atau mengganti character aktif.
>
> **Contoh**
>
> ```text
> !character
> ```
>
> ```text
> !character NamaCharacter
> ```
>
> ## `!character list`
>
> Melihat daftar character yang dimiliki.
>
> ```text
> !character list
> ```
>
> ## `!import`
>
> Mengimpor character sheet ke Avrae.
>
> **Contoh**
>
> ```text
> !import <link-character-sheet>
> ```
>
> ## `!sheet`
>
> Menampilkan character sheet aktif.
>
> ```text
> !sheet
> ```
>
> ## `!update`
>
> Memperbarui character sheet aktif.
>
> ```text
> !update
> ```

> [!example]- 🔎 Lookup
> Digunakan untuk mencari informasi D&D.
>
> ## `!monster`
>
> Mencari informasi monster.
>
> ```text
> !monster goblin
> ```
>
> ## `!spell`
>
> Mencari informasi spell.
>
> ```text
> !spell fireball
> ```
>
> ## `!item`
>
> Mencari informasi item.
>
> ```text
> !item longsword
> ```
>
> ## `!class`
>
> Mencari informasi class.
>
> ```text
> !class fighter
> ```
>
> ## `!race`
>
> Mencari informasi species/race.
>
> ```text
> !race elf
> ```
>
> ## `!feat`
>
> Mencari informasi feat.
>
> ```text
> !feat sharpshooter
> ```
>
> ## `!condition`
>
> Mencari informasi condition.
>
> ```text
> !condition poisoned
> ```
>
> ## `!rule`
>
> Mencari informasi rule D&D.
>
> ```text
> !rule cover
> ```

> [!example]- ❤️ Character Status
> Command untuk melihat dan mengelola kondisi character di luar combat.
>
> ## `!game status`
>
> Melihat status character.
>
> ```text
> !game status
> ```
>
> ## `!game hp`
>
> Mengubah HP character.
>
> ```text
> !game hp 25
> ```
>
> Untuk menambah/mengurangi HP:
>
> ```text
> !game hp mod 5
> ```
>
> ## `!game thp`
>
> Mengatur temporary HP.
>
> ```text
> !game thp 10
> ```
>
> ## `!game longrest`
>
> Melakukan long rest.
>
> ```text
> !game longrest
> ```
>
> **Shortcut**
>
> ```text
> !lr
> ```
>
> ## `!game shortrest`
>
> Melakukan short rest.
>
> ```text
> !game shortrest
> ```
>
> **Shortcut**
>
> ```text
> !sr
> ```

> [!example]- ✨ Spell & Spellbook
> Command untuk melihat dan menggunakan spell di luar combat.
>
> ## `!spell`
>
> Mencari informasi spell.
>
> ```text
> !spell fireball
> ```
>
> ## `!spellbook`
>
> Melihat spell yang tersedia pada character.
>
> ```text
> !spellbook
> ```
>
> ## `!cast`
>
> Menggunakan spell dari character aktif.
>
> ```text
> !cast fireball
> ```
>
> > [!tip]
> > Penggunaan `!cast` biasanya lebih relevan ketika sedang berada dalam combat, tetapi command ini juga dapat digunakan di luar combat.

> [!example]- 🛠️ Utility
> Command sederhana untuk kebutuhan umum.
>
> ## `!ping`
>
> Mengecek apakah Avrae merespons.
>
> ```text
> !ping
> ```
>
> ## `!invite`
>
> Mendapatkan link untuk mengundang Avrae.
>
> ```text
> !invite
> ```

# 🔴 BATTLE

Command yang digunakan ketika **combat sedang berlangsung**.

> [!example]- ⚔️ Memulai Combat
> ## `!init begin`
>
> Memulai initiative tracker.
>
> ```text
> !init begin
> ```
>
> Setelah combat dimulai, setiap peserta dapat bergabung menggunakan:
>
> ```text
> !init join
> ```
>
> atau:
>
> ```text
> !init add
> ```

> [!example]- 📋 Initiative
> Command utama untuk mengatur giliran combat.
>
> ## `!init list`
>
> Melihat daftar peserta combat.
>
> ```text
> !init list
> ```
>
> ## `!init next`
>
> Berpindah ke combatant berikutnya.
>
> ```text
> !init next
> ```
>
> **Shortcut**
>
> ```text
> !init n
> ```
>
> ## `!init`
>
> Melihat status initiative saat ini.
>
> ```text
> !init
> ```
>
> ## `!init join`
>
> Menambahkan character aktif ke combat.
>
> ```text
> !init join
> ```
>
> ## `!init end`
>
> Mengakhiri combat.
>
> ```text
> !init end
> ```

> [!example]- 🗡️ Attack & Action
> Command untuk melakukan attack atau action menggunakan character aktif.
>
> ## `!attack`
>
> Melakukan attack.
>
> ```text
> !attack Longsword
> ```
>
> **Shortcut**
>
> ```text
> !a Longsword
> ```
>
> > [!tip]
> > Nama attack/action biasanya mengikuti data yang tersedia pada character sheet Anda.

> [!example]- ✨ Cast Spell
> Command untuk menggunakan spell selama combat.
>
> ## `!cast`
>
> Melakukan casting spell.
>
> ```text
> !cast fireball
> ```
>
> Contoh spell dengan target:
>
> ```text
> !cast cure wounds -t NamaCharacter
> ```
>
> ## `!init cast`
>
> Melakukan casting spell melalui initiative tracker.
>
> ```text
> !init cast fireball
> ```

> [!example]- 🛡️ Check & Saving Throw
> Command untuk melakukan ability check dan saving throw.
>
> ## `!check`
>
> Melakukan ability check.
>
> ```text
> !check perception
> ```
>
> Contoh:
>
> ```text
> !check stealth
> ```
>
> ## `!save`
>
> Melakukan saving throw.
>
> ```text
> !save dex
> ```
>
> ## `!init check`
>
> Melakukan ability check sebagai bagian dari combat.
>
> ```text
> !init check perception
> ```
>
> ## `!init save`
>
> Melakukan saving throw sebagai bagian dari combat.
>
> ```text
> !init save dex
> ```

> [!example]- ❤️ HP & Status
> Command untuk mengelola HP dan kondisi combatant.
>
> ## `!game hp`
>
> Mengubah HP character aktif.
>
> ```text
> !game hp mod -5
> ```
>
> ## `!init hp`
>
> Mengubah HP combatant dalam initiative tracker.
>
> ```text
> !init hp NamaCharacter 20
> ```
>
> ## `!init thp`
>
> Mengatur temporary HP combatant.
>
> ```text
> !init thp NamaCharacter 10
> ```
>
> ## `!init status`
>
> Melihat status combatant.
>
> ```text
> !init status
> ```

> [!example]- 🔄 Turn & Combat Management
> Command untuk mengatur jalannya combat.
>
> ## `!init next`
>
> Berpindah ke turn berikutnya.
>
> ```text
> !init next
> ```
>
> ## `!init prev`
>
> Kembali ke turn sebelumnya.
>
> ```text
> !init prev
> ```
>
> ## `!init move`
>
> Berpindah ke combatant tertentu.
>
> ```text
> !init move NamaCharacter
> ```
>
> ## `!init end`
>
> Mengakhiri combat.
>
> ```text
> !init end
> ```

# ❓ HELP & REFERENSI

> [!example]- ❓ Help
> ## `!help`
>
> Melihat bantuan Avrae.
>
> ```text
> !help
> ```
>
> Untuk command tertentu:
>
> ```text
> !help roll
> ```
>
> ```text
> !help init
> ```
>
> ```text
> !help attack
> ```
>
> > [!tip]
> > Jika Anda lupa cara menggunakan sebuah command, `!help <command>` adalah cara paling aman untuk melihat syntax yang tersedia di server Anda.
>
> ## `!tutorial`
>
> Menjalankan tutorial Avrae.
>
> ```text
> !tutorial
> ```

> [!info] Catatan
> Prefix Avrae secara default adalah `!`, tetapi administrator server dapat mengubahnya. Jika `!command` tidak bekerja, tanyakan prefix Avrae yang digunakan pada server.