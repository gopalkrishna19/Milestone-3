extern crate regex;

use regex::Regex;

fn is_valid_date(date: String) -> bool {
    let re = Regex::new(r"^(0?[1-9]|1[0-2])/([1-9]|[12][0-9]|3[01])/(\d{4})$").unwrap();
    re.is_match(&date)
}

fn main() {
    let date1 = String::from("6/1/2025");
    let date2 = String::from("12/31/2025");

    println!("Is '{}' a valid date? {}", date1, is_valid_date(date1));
    println!("Is '{}' a valid date? {}", date2, is_valid_date(date2));
}
