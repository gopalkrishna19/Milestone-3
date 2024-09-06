# Milestone-3
The ipynb file works perfectly in google colab
extern crate regex;

use regex::Regex;

fn main() {
    let date_time = "6/1/2025 0:00";
    let re = Regex::new(r"^(0?[1-9]|1[0-2])/([1-9]|[12][0-9]|3[01])/(\d{4}) ([01]?\d|2[0-3]):([0-5]?\d)$").unwrap();

    if re.is_match(date_time) {
        println!("The string is in the correct format.");
    } else {
        println!("The string is not in the correct format.");
    }
}
