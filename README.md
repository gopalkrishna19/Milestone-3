# Milestone-3
The ipynb file works perfectly in google colab
extern crate regex;

use regex::Regex;

fn main() {
    let date = "6/1/2025";
    let re = Regex::new(r"^(0?[1-9]|1[0-2])/([1-9]|[12][0-9]|3[01])/(\d{4})$").unwrap();

    if re.is_match(date) {
        println!("The string is in the correct format.");
    } else {
        println!("The string is not in the correct format.");
    }
}
