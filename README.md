# obyektlar-va-ularni-xususyatlari
/**
 * Loyiha: Avtosalon Boshqaruv Tizimi
 * Mavzu: Obyektlar, xususiyatlar, metodlar va this kalit so'zi
 */

// 1. mashina nomli obyektni ochish
let mashina = {
    brend: "Chevrolet",
    model: "Gentra",
    yil: 2022,
    narx: 13000,
    tanirovka: false,

    // malumotBering metodi (this orqali ma'lumot chiqarish)
    malumotBering: function() {
        console.log(`Brend: ${this.brend}, Model: ${this.model}, Narxi: ${this.narx}$`);
    },

    // tanirovkaQildir metodi (tanirovkani true qilib, narxga 500$ qo'shish)
    tanirovkaQildir: function() {
        this.tanirovka = true;
        this.narx += 500;
    }
};

// 2. Obyektdan tashqarida yangi rang xususiyatini qo'shish va narxni yangilash
mashina.rang = "To'q kulrang";
mashina.narx = 12500;

// 3. Dastur so'ngida ketma-ketlikni bajarish va natijalarni tekshirish
console.log("--- Boshlang'ich ma'lumot ---");
mashina.malumotBering();

console.log("\n--- Tanirovka qilingandan keyin ---");
mashina.tanirovkaQildir();
mashina.malumotBering();

console.log("\n--- To'liq mashina obyekti ---");
console.log(mashina);
