🎉 **Botlarda mesaj ve ya embedlerde kullanacağımız discorda yeni gelen özellik olan butonları inceleyelim**


1️⃣ **Daha discord.js kütüphanesinde bununla ilgili bir şey olmadığından discord.js kullanmayacağız şimdilik**

2️⃣ **Kullanacağımız modül: https://npmjs.com/package/discord-buttons**

**PEKİ BU MODÜL NASIL KULLANILIR**

**İLk olarak const { MessageButton } = require('discord-buttons'); şeklinde discord-buttons modülünü tanımlamamız gerekli**

**Mesela örnek bir kod**
const { MessageButton } = require('discord-buttons');
exports.run = async(client, message, args) => {
  let button2 = new MessageButton()
    .setStyle('url')
    .setLabel('Bir buton')
    .setURL('https://github.com')
  
  return message.channel.send('İlk deneme butonum', {
    buttons: [
     button2
    ]
  });
}
exports.conf = {
    enabled: true,
    guildOnly: false,
    permLevel:0,
    aliases: []
    }
    exports.help = {
    name: "discord-buttons"
    }
__________________
