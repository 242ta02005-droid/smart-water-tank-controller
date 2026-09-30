# smart-water-tank-controller
# Smart Water Tank Controller

print("SMART WATER TANK CONTROLLER")
print("---------------------------")

pump = False

while True:
    level = float(input("\nEnter water level (%): "))

    if level <= 20:
        pump = True
        print("Water Level: LOW")
        print("Pump: ON")
        print("Alert: Tank needs water.")

    elif level >= 90:
        pump = False
        print("Water Level: HIGH")
        print("Pump: OFF")
        print("Alert: Tank is almost FULL.")

    else:
        pump = False
        print("Water Level: NORMAL")
        print("Pump: OFF")

    print("Pump Status:", "ON" if pump else "OFF")

    choice = input("\nCheck again? (yes/no): ")

    if choice.lower() != "yes":
        print("\nSmart controller stopped.")
        break
