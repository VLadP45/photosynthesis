# photosynthesisclass Photosynthesis:
    def __init__(self, co2, h2o, sunlight):
        self.co2 = co2  # Carbon Dioxide
        self.h2o = h2o  # Water
        self.sunlight = sunlight  # Sunlight
    
    def perform_photosynthesis(self):
        # Chemical reaction: 6CO₂ + 6H₂O + sunlight -> C₆H₁₂O₆ + 6O₂
        if self.sunlight and self.co2 >= 6 and self.h2o >= 6:
            glucose = 1  # 1 glucose molecule
            oxygen = 6   # 6 oxygen molecules
            self.co2 -= 6
            self.h2o -= 6
            print(f"Photosynthesis complete! Produced {glucose} glucose and {oxygen} oxygen molecules.")
        else:
            print("Insufficient resources for photosynthesis!")

# Example usage:
plant = Photosynthesis(co2=12, h2o=10, sunlight=True)
plant.perform_photosynthesis()
