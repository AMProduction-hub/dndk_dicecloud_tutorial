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
# 🎲 Avrae Command Reference

Halaman ini berisi command Avrae yang paling sering digunakan dalam permainan D&D. Command dibagi menjadi **Non-Battle** dan **Battle** agar lebih mudah ditemukan.

> [!tip] Cara pakai halaman ini Klik judul setiap kategori (`▸`) untuk membuka/menutup daftar command di dalamnya.

---

## 📑 Ringkasan Cepat

|Kebutuhan|Command|
|---|---|
|Roll dadu|`!roll 1d20` / `!r 1d20`|
|Roll dengan advantage|`!roll 1d20 adv`|
|Roll dengan disadvantage|`!roll 1d20 dis`|
|Lihat character sheet|`!sheet`|
|Mulai combat|`!init begin`|
|Giliran berikutnya|`!init next`|
|Attack|`!attack <nama>` / `!a <nama>`|
|Cast spell|`!cast <nama spell>`|
|Bantuan|`!help <command>`|

---

## 🟢 Non-Battle

Command yang digunakan **di luar combat** — untuk mengelola character, melakukan dice roll, mencari informasi, dan kebutuhan lainnya.

> [!example]- 🎲 Dice & Rolling
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
> **Shortcut:** `!r 1d20`
> 
> ---
> 
> ## Advantage & Disadvantage
> 
> Melakukan roll **2 kali** dan mengambil hasil yang lebih tinggi (_advantage_) atau lebih rendah (_disadvantage_).
> 
> |Mode|Syntax|Shortcut|
> |---|---|---|
> |Advantage|`!roll 1d20 adv`|`!r 1d20 adv`|
> |Disadvantage|`!roll 1d20 dis`|`!r 1d20 dis`|
> 
> ---
> 
> ## `!rr`
> 
> Melakukan multiple roll sekaligus.
> 
> **Contoh**
> 
> ```text
> !rr 2 1d20
> ```
> 
> > [!tip] Yang paling sering dipakai
> > 
> > - `!roll 1d20` → normal roll
> > - `!roll 1d20 adv` → advantage
> > - `!roll 1d20 dis` → disadvantage
> > - `!r` → shortcut dari `!roll`

> [!example]- 🧙 Character
> 
> # `!character`
> 
> Melihat atau mengganti character aktif.
> 
> **Contoh**
> 
> ```text
> !character
> !character NamaCharacter
> ```
> 
> ### `!character list`
> 
> Melihat daftar character yang dimiliki.
> 
> ```text
> !character list
> ```
> 
> # `!import`
> 
> Mengimpor character sheet ke Avrae.
> 
> ```text
> !import <link-character-sheet>
> ```
> 
> # `!sheet`
> 
> Menampilkan character sheet aktif.
> 
> ```text
> !sheet
> ```
> 
> # `!update`
> 
> Memperbarui character sheet aktif.
> 
> ```text
> !update
> ```

> [!example]- 🔎 Lookup Digunakan untuk mencari informasi D&D.
> 
> |Command|Kegunaan|Contoh|
> |---|---|---|
> |`!monster`|Info monster|`!monster goblin`|
> |`!spell`|Info spell|`!spell fireball`|
> |`!item`|Info item|`!item longsword`|
> |`!class`|Info class|`!class fighter`|
> |`!race`|Info species/race|`!race elf`|
> |`!feat`|Info feat|`!feat sharpshooter`|
> |`!condition`|Info condition|`!condition poisoned`|
> |`!rule`|Info rule D&D|`!rule cover`|

> [!example]- ❤️ Character Status
> 
> #### `!game status`
> 
> Melihat status character.
> 
> ```text
> !game status
> ```
> 
> #### `!game hp`
> 
> Mengubah HP character.
> 
> ```text
> !game hp 25
> ```
> 
> Menambah/mengurangi HP:
> 
> ```text
> !game hp mod 5
> ```
> 
> #### `!game thp`
> 
> Mengatur temporary HP.
> 
> ```text
> !game thp 10
> ```
> 
> #### `!game longrest`
> 
> Melakukan long rest.
> 
> ```text
> !game longrest
> ```
> 
> **Shortcut:** `!lr`
> 
> #### `!game shortrest`
> 
> Melakukan short rest.
> 
> ```text
> !game shortrest
> ```
> 
> **Shortcut:** `!sr`

> [!example]- ✨ Spell & Spellbook
> 
> ### `!spell`
> 
> Mencari informasi spell.
> 
> ```text
> !spell fireball
> ```
> 
> ### `!spellbook`
> 
> Melihat spell yang tersedia pada character.
> 
> ```text
> !spellbook
> ```
> 
> ### `!cast`
> 
> Menggunakan spell dari character aktif.
> 
> ```text
> !cast fireball
> ```
> 
> > [!tip] Penggunaan `!cast` biasanya lebih relevan ketika sedang berada dalam combat, tetapi command ini juga dapat digunakan di luar combat.

> [!example]- 🛠️ Utility
> 
> ### `!ping`
> 
> Mengecek apakah Avrae merespons.
> 
> ```text
> !ping
> ```
> 
> ### `!invite`
> 
> Mendapatkan link untuk mengundang Avrae.
> 
> ```text
> !invite
> ```

---

## 🔴 Battle

Command yang digunakan ketika **combat sedang berlangsung**.

> [!example]- ⚔️ Memulai Combat
> 
> ### `!init begin`
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

> [!example]- 📋 Initiative Command utama untuk mengatur giliran combat.
> 
> |Command|Kegunaan|Shortcut|
> |---|---|---|
> |`!init`|Melihat status initiative saat ini|—|
> |`!init list`|Melihat daftar peserta combat|—|
> |`!init join`|Menambahkan character aktif ke combat|—|
> |`!init next`|Berpindah ke combatant berikutnya|`!init n`|
> |`!init end`|Mengakhiri combat|—|

> [!example]- 🗡️ Attack & Action
> 
> ### `!attack`
> 
> Melakukan attack.
> 
> ```text
> !attack Longsword
> ```
> 
> **Shortcut:** `!a Longsword`
> 
> > [!tip] Nama attack/action biasanya mengikuti data yang tersedia pada character sheet Anda.

> [!example]- ✨ Cast Spell
> 
> ### `!cast`
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
> ### `!init cast`
> 
> Melakukan casting spell melalui initiative tracker.
> 
> ```text
> !init cast fireball
> ```

> [!example]- 🛡️ Check & Saving Throw
> 
> ### `!check`
> 
> Melakukan ability check.
> 
> ```text
> !check perception
> !check stealth
> ```
> 
> ### `!save`
> 
> Melakukan saving throw.
> 
> ```text
> !save dex
> ```
> 
> ### `!init check` / `!init save`
> 
> Melakukan ability check atau saving throw sebagai bagian dari combat.
> 
> ```text
> !init check perception
> !init save dex
> ```

> [!example]- ❤️ HP & Status
> 
> ### `!game hp`
> 
> Mengubah HP character aktif.
> 
> ```text
> !game hp mod -5
> ```
> 
> ### `!init hp`
> 
> Mengubah HP combatant dalam initiative tracker.
> 
> ```text
> !init hp NamaCharacter 20
> ```
> 
> ### `!init thp`
> 
> Mengatur temporary HP combatant.
> 
> ```text
> !init thp NamaCharacter 10
> ```
> 
> ### `!init status`
> 
> Melihat status combatant.
> 
> ```text
> !init status
> ```

> [!example]- 🔄 Turn & Combat Management
> 
> |Command|Kegunaan|
> |---|---|
> |`!init next`|Berpindah ke turn berikutnya|
> |`!init prev`|Kembali ke turn sebelumnya|
> |`!init move NamaCharacter`|Berpindah ke combatant tertentu|
> |`!init end`|Mengakhiri combat|

---

## ❓ Help & Referensi

> [!example]- ❓ Help
> 
> ### `!help`
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
> !help init
> !help attack
> ```
> 
> > [!tip] Jika Anda lupa cara menggunakan sebuah command, `!help <command>` adalah cara paling aman untuk melihat syntax yang tersedia di server Anda.
> 
> ### `!tutorial`
> 
> Menjalankan tutorial Avrae.
> 
> ```text
> !tutorial
> ```

> [!info] Catatan Prefix Avrae secara default adalah `!`, tetapi administrator server dapat mengubahnya. Jika `!command` tidak bekerja, tanyakan prefix Avrae yang digunakan pada server.