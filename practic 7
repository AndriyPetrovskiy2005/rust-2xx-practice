fn draw_tree(triangles: usize) {
    (1..=triangles).for_each(|i| {
        (0..i * 2).for_each(|j| {
            let spaces = triangles * 2 - j - 1;
            let stars = j * 2 + 1;
            println!("{:width$}{}", "", "*".repeat(stars), width = spaces);
        });
    });
}

fn main() {
    let triangles = 5; 
    draw_tree(triangles);
}
