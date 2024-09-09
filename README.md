fn is_positive_number(s: &str) -> bool {
    // Try to parse the string into a number
    if let Ok(num) = s.parse::<f64>() {
        // Check if the number is positive
        num > 0.0
    } else {
        // Return false if parsing fails
        false
    }
}

fn main() {
    let test_str = "42";
    println!("Can be converted to positive number: {}", is_positive_number(test_str));
}
