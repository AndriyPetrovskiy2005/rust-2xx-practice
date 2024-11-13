fn print_envelope(size: usize) {
    for i in 0..size {
        for j in 0..size {
            if i == 0 || i == size - 1 || j == 0 || j == size - 1 || i == j || i + j == size - 1 {
                print!("*");
            } else {
                print!(" ");
            }
        }
        println!();
    }
}

fn main() {
    let size = 30; 
    print_envelope(size);
}
