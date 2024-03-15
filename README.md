#include <iostream>
 

int main() {
    double h; distance; angle_degrees;
    char distanceUnit;
    
 
    std::cout << "Enter the height of your eyes from the ground (in inches): ";
    std::cin >> h;

     std::cout << "Enter the distance to the tree followed by 'f' for feet or 'i' for inches (e.g., 10 f): ";
    std::cin >> distance >> distanceUnit;

     
    if (distanceUnit == 'f' || distanceUnit == 'F') {
        distance *= 12.0; 
    }

  
    std::cout << "Enter the angle in degrees: ";
    std::cin >> angle_degrees;

  
    double angle_radians = angle_degrees * (M_PI / 180.0);

     
    double tree_height_inches = h + distance * tan(angle_radians);

    
    double tree_height_feet = tree_height_inches / 12.0;

    std::cout << "The height of the tree is: " << tree_height_feet << " feet.\n";
    return 0;
}
