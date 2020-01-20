def cost_of_ground_shipping(weight):
  if weight <= 2:
    price_per_pound = 1.50
  elif weight <= 6:
    price_per_pound = 3.00
  elif weight <= 10:
    price_per_pound = 4.00
  else:
    price_per_pound = 4.75
  return 20 + (price_per_pound * weight)

print(cost_of_ground_shipping(8.4))

premium_ground_shipping = 125.00

def cost_of_drone_shipping(weight):
  if weight <= 2:
    price_per_pound = 4.50
  elif weight <= 6:
    price_per_pound = 9.00
  elif weight <= 10:
    price_per_pound = 12.00
  else:
    price_per_pound = 14.25
  return (price_per_pound * weight)

print(cost_of_drone_shipping(1.5))

def print_cheapest_shipping(weight):
 ground = cost_of_ground_shipping(weight)
 drone = cost_of_drone_shipping(weight)
 premium = premium_ground_shipping

 if ground < drone and ground < premium:
  cost = ground
  method = "Ground Shipping"
 elif drone < ground and drone < premium:
  cost = drone
  method = "Drone Shipping"
 elif premium < ground and premium < drone:
  cost = premium
  method = "Premium Ground Shipping"
  
 print("The cheapest shipping will cost $%.2f and will be done by %s!"

  % (cost,method)
)

print_cheapest_shipping(41.5)

  
