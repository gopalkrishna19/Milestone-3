fn is_valid_decimal(s: &str) -> bool {
    // Define a regex pattern to match up to 9 digits before the decimal point (0-9 digits),
    // and up to 2 digits after the decimal point (0-2 digits)
    let decimal_pattern = r"^\d{0,9}(\.\d{0,2})?$";
    let re = regex_lite::Regex::new(decimal_pattern).unwrap();

    // Check if the string matches the pattern
    re.is_match(s)
}

fn main() {
    let test_cases = vec![
        "123456789",   // valid (no decimal part)
        "123456789.12", // valid (2 decimal places)
        "1234567890.12", // invalid (more than 9 digits before decimal)
        "123456789.123", // invalid (more than 2 digits after decimal)
        "12345678.9",   // valid (1 decimal place)
        "1234567.",     // valid (no digits after the decimal)
        "abcdefg",      // invalid (non-numeric)
        ".12",          // valid (no digits before the decimal)
        ".",            // valid (no digits before or after the decimal)
        "0.",           // valid (only zero before the decimal)
        ".0",           // valid (only zero after the decimal)
    ];

    for case in test_cases {
        println!("Is '{}' a valid decimal? {}", case, is_valid_decimal(case));
    }
}
