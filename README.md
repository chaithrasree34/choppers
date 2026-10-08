# DC Chopper Calculator

print("DC CHOPPER CALCULATOR")
print("---------------------")

# Input values
Vs = float(input("Enter supply voltage (V): "))
D = float(input("Enter duty cycle (%): "))
R = float(input("Enter load resistance (Ohm): "))

# Convert duty cycle percentage to decimal
D_decimal = D / 100

# Average output voltage
Vo = D_decimal * Vs

# Average load current
Io = Vo / R

# Chopper ON and OFF time ratio
Ton_Toff_ratio = D_decimal / (1 - D_decimal)

# Display results
print("\n--- Results ---")
print(f"Duty Cycle       = {D:.2f}%")
print(f"Output Voltage   = {Vo:.2f} V")
print(f"Output Current   = {Io:.2f} A")
print(f"Ton/Toff Ratio   = {Ton_Toff_ratio:.2f}")

if D > 50:
    print("Chopper operates with duty cycle greater than 50%.")
elif D < 50:
    print("Chopper operates with duty cycle less than 50%.")
else:
    print("Chopper operates at 50% duty cycle.")# choppers