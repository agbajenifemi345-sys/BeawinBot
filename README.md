const TelegramBot = require('node-telegram-bot-api');

// Replace with your bot token
const token = '8344715533:AAEa-uKZsAOZp3nWj66Wmp0cPakCCe2n1TE';
const bot = new TelegramBot(token, { polling: true });

// Start message
bot.onText(/\/start/, (msg) => {
  const chatId = msg.chat.id;
  bot.sendMessage(chatId, `
👋 Welcome to *Beawin TaskBot*!

Here’s how to use the bot 👇

🔹 /task1 – Get your first task  
🔹 /task2 – Get your second task  
🔹 /task3 – Get your third task  
🔹 /tasks – How to complete tasks  
🔹 /balance – Check your balance  
🔹 /refer – Get your referral link  
🔹 /withdraw – Withdraw your earnings  
🔹 /submitproof – Submit proof of tasks  
🔹 /customerservice – Contact support  
🔹 /about – About Beawin  
🔹 /beawinchannels – Join our official channels  
`);
});

// Example commands
bot.onText(/\/about/, (msg) => {
  bot.sendMessage(msg.chat.id, "💼 *Beawin TaskBot* helps users earn by completing simple tasks, referring friends, and staying active!");
});

bot.onText(/\/customerservice/, (msg) => {
  bot.sendMessage(msg.chat.id, "💬 For help, message our support team on WhatsApp:\nhttps://wa.me/234XXXXXXXXXX");
});

bot.onText(/\/beawinchannels/, (msg) => {
  bot.sendMessage(msg.chat.id, `
🌍 *Join Beawin Communities!*
