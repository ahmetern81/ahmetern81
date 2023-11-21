import random

class Car:
    def __init__(self, brand, speed):
        self.brand = brand
        self.speed = speed

    def accelerate(self):
        acceleration = random.randint(5, 15)
        self.speed += acceleration
        print(f"{self.brand} hızlandı! Şu anki hız: {self.speed} km/saat")

    def brake(self):
        deceleration = random.randint(1, 10)
        self.speed -= deceleration
        print(f"{self.brand} fren yaptı. Şu anki hız: {self.speed} km/saat")

    def honk(self):
        print(f"{self.brand} korna çaldı!")

def main():
    print("Hoş geldiniz! Arabanızı sürün.")

    car_brand = input("Aracınızın markasını girin: ")
    initial_speed = random.randint(0, 100)
    
    player_car = Car(car_brand, initial_speed)

    while True:
        print("\nAraba Kontrolleri:")
        print("1. Hızlandır")
        print("2. Fren Yap")
        print("3. Korna Çal")
        print("4. Çıkış")

        choice = input("Seçiminizi yapın (1-4): ")

        if choice == '1':
            player_car.accelerate()
        elif choice == '2':
            player_car.brake()
        elif choice == '3':
            player_car.honk()
        elif choice == '4':
            print("Oyunu sonlandırıyorsunuz. İyi günler!")
            break
        else:
            print("Geçersiz seçim. Lütfen 1-4 arasında bir sayı girin.")

if __name__ == "__main__":
    main()
