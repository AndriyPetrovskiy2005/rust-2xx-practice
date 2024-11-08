test 1
use std::io;

fn simple_array_sum(ar: Vec<i32>) -> i32 {
    let mut sum = 0;
    for &num in &ar {
        sum += num;
    }
    sum
}

fn main() {
    let mut input = String::new();
    
    io::stdin().read_line(&mut input).unwrap();
    let ar_count: usize = input.trim().parse().unwrap();

    input.clear();
    io::stdin().read_line(&mut input).unwrap();
    let ar: Vec<i32> = input
        .trim()
        .split_whitespace()
        .map(|s| s.parse().unwrap())
        .collect();

    let result = simple_array_sum(ar);
    println!("{}", result);
}
test 2
use std::io;

fn compare_triplets(a: Vec<i32>, b: Vec<i32>) -> Vec<i32> {
    let mut scores = vec![0, 0];
    for i in 0..3 {
        if a[i] > b[i] {
            scores[0] += 1;
        } else if a[i] < b[i] {
            scores[1] += 1;
        }
    }
    scores
}

fn main() {
    let mut input = String::new();
    
    io::stdin().read_line(&mut input).unwrap();
    let a: Vec<i32> = input
        .trim()
        .split_whitespace()
        .map(|s| s.parse().unwrap())
        .collect();

    input.clear();
    io::stdin().read_line(&mut input).unwrap();
    let b: Vec<i32> = input
        .trim()
        .split_whitespace()
        .map(|s| s.parse().unwrap())
        .collect();

    let result = compare_triplets(a, b);
    println!("{}", result.iter().map(i32::to_string).collect::<Vec<String>>().join(" "));
}
test 3
use std::io;

fn a_very_big_sum(ar: Vec<i64>) -> i64 {
    ar.iter().sum()
}

fn main() {
    let mut input = String::new();
    
    io::stdin().read_line(&mut input).unwrap();
    let ar_count: usize = input.trim().parse().unwrap();

    input.clear();
    io::stdin().read_line(&mut input).unwrap();
    let ar: Vec<i64> = input
        .trim()
        .split_whitespace()
        .map(|s| s.parse().unwrap())
        .collect();

    let result = a_very_big_sum(ar);
    println!("{}", result);
}
test 4
use std::io;

fn diagonal_difference(arr: Vec<Vec<i32>>) -> i32 {
    let n = arr.len();
    let mut primary_diagonal = 0;
    let mut secondary_diagonal = 0;

    for i in 0..n {
        primary_diagonal += arr[i][i];
        secondary_diagonal += arr[i][n - i - 1];
    }

    (primary_diagonal - secondary_diagonal).abs()
}

fn main() {
    let mut input = String::new();
    
    io::stdin().read_line(&mut input).unwrap();
    let n: usize = input.trim().parse().unwrap();

    let mut arr = Vec::with_capacity(n);

    for _ in 0..n {
        input.clear();
        io::stdin().read_line(&mut input).unwrap();
        let row: Vec<i32> = input
            .trim()
            .split_whitespace()
            .map(|s| s.parse().unwrap())
            .collect();
        arr.push(row);
    }

    let result = diagonal_difference(arr);
    println!("{}", result);
}
test 5
use std::io;

fn plus_minus(arr: Vec<i32>) {
    let n = arr.len();
    let (mut positive_count, mut negative_count, mut zero_count) = (0, 0, 0);

    for &num in &arr {
        if num > 0 {
            positive_count += 1;
        } else if num < 0 {
            negative_count += 1;
        } else {
            zero_count += 1;
        }
    }

    println!("{:.6}", positive_count as f64 / n as f64);
    println!("{:.6}", negative_count as f64 / n as f64);
    println!("{:.6}", zero_count as f64 / n as f64);
}

fn main() {
    let mut input = String::new();
    
    io::stdin().read_line(&mut input).unwrap();
    let n: usize = input.trim().parse().unwrap();

    input.clear();
    io::stdin().read_line(&mut input).unwrap();
    let arr: Vec<i32> = input
        .trim()
        .split_whitespace()
        .map(|s| s.parse().unwrap())
        .collect();

    plus_minus(arr);
}
test 6
use std::io;

fn staircase(n: i32) {
    for i in 1..=n {
        let spaces = " ".repeat((n - i) as usize);
        let hashes = "#".repeat(i as usize);
        println!("{}{}", spaces, hashes);
    }
}

fn main() {
    let mut input = String::new();
    
    io::stdin().read_line(&mut input).unwrap();
    let n: i32 = input.trim().parse().unwrap();

    staircase(n);
}
test 7
use std::io;

fn mini_max_sum(arr: Vec<i64>) {
    let sum: i64 = arr.iter().sum();
    let min = *arr.iter().min().unwrap();
    let max = *arr.iter().max().unwrap();
    
    let min_sum = sum - max;
    let max_sum = sum - min;

    println!("{} {}", min_sum, max_sum);
}

fn main() {
    let mut input = String::new();
    
    io::stdin().read_line(&mut input).unwrap();
    let arr: Vec<i64> = input
        .trim()
        .split_whitespace()
        .map(|s| s.parse().unwrap())
        .collect();

    mini_max_sum(arr);
}
test 8
use std::io;

fn birthday_cake_candles(candles: Vec<i32>) -> i32 {
    let max_height = *candles.iter().max().unwrap();
    candles.iter().filter(|&&candle| candle == max_height).count() as i32
}

fn main() {
    let mut candles_count_temp = String::new();
    io::stdin().read_line(&mut candles_count_temp).unwrap();
    
    let candles_count: usize = candles_count_temp.trim().parse().unwrap();
    
    let mut candles_temp = String::new();
    io::stdin().read_line(&mut candles_temp).unwrap();
    
    let candles: Vec<i32> = candles_temp
        .trim()
        .split_whitespace()
        .map(|s| s.parse().unwrap())
        .collect();
    
    let result = birthday_cake_candles(candles);
    
    println!("{}", result);
}
test 9
se std::io;

fn time_conversion(s: &str) -> String {
    let (time, period) = s.split_at(s.len() - 2);
    let mut parts: Vec<String> = time.split(':').map(|p| p.to_string()).collect();
    let hour: i32 = parts[0].parse().unwrap();

    if period == "AM" {
        if hour == 12 {
            parts[0] = "00".to_string();
        }
    } else if period == "PM" {
        if hour != 12 {
            let new_hour = hour + 12;
            parts[0] = new_hour.to_string();
        }
    }

    format!("{}:{}:{}", parts[0], parts[1], parts[2])
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let result = time_conversion(input.trim());
    println!("{}", result);
}
test 10
use std::io;

fn grading_students(grades: Vec<i32>) -> Vec<i32> {
    grades.into_iter().map(|grade| {
        if grade >= 38 {
            let next_multiple_of_5 = ((grade / 5) + 1) * 5;
            if next_multiple_of_5 - grade < 3 {
                next_multiple_of_5
            } else {
                grade
            }
        } else {
            grade
        }
    }).collect()
}

fn main() {
    let mut grades: Vec<i32> = Vec::new();
    let stdin = io::stdin();

    println!("Введіть кількість оцінок:");
    let mut input = String::new();
    stdin.read_line(&mut input).expect("Failed to read line");
    let count: usize = input.trim().parse().expect("Please type a number!");

    println!("Введіть оцінки:");
    for _ in 0..count {
        let mut grade_input = String::new();
        stdin.read_line(&mut grade_input).expect("Failed to read line");
        let grade = grade_input.trim().parse::<i32>();
        if let Ok(g) = grade {
            grades.push(g);
        } else {
            println!("Неправильний формат оцінки, спробуйте ще раз.");
        }
    }

    let result = grading_students(grades);

    println!("Результати:");
    for grade in result {
        println!("{}", grade);
    }
}
test 11
use std::io;

fn count_apples_and_oranges(s: i32, t: i32, a: i32, b: i32, apples: Vec<i32>, oranges: Vec<i32>) {
    let apple_count = apples.iter().filter(|&&apple| (a + apple).between(s, t)).count();
    let orange_count = oranges.iter().filter(|&&orange| (b + orange).between(s, t)).count();
    println!("{}", apple_count);
    println!("{}", orange_count);
}

trait Between {
    fn between(self, low: Self, high: Self) -> bool;
}

impl Between for i32 {
    fn between(self, low: Self, high: Self) -> bool {
        self >= low && self <= high
    }
}

fn main() {
    let stdin = io::stdin();
    let mut input = String::new();

    stdin.read_line(&mut input).expect("Failed to read line");
    let first_multiple_input: Vec<i32> = input.trim().split_whitespace().map(|x| x.parse().unwrap()).collect();
    let (s, t) = (first_multiple_input[0], first_multiple_input[1]);

    input.clear();
    stdin.read_line(&mut input).expect("Failed to read line");
    let second_multiple_input: Vec<i32> = input.trim().split_whitespace().map(|x| x.parse().unwrap()).collect();
    let (a, b) = (second_multiple_input[0], second_multiple_input[1]);

    input.clear();
    stdin.read_line(&mut input).expect("Failed to read line");
    let _ = input.trim().split_whitespace().map(|x| x.parse::<i32>().unwrap()).collect::<Vec<i32>>();

    input.clear();
    stdin.read_line(&mut input).expect("Failed to read line");
    let apples: Vec<i32> = input.trim().split_whitespace().map(|x| x.parse().unwrap()).collect();

    input.clear();
    stdin.read_line(&mut input).expect("Failed to read line");
    let oranges: Vec<i32> = input.trim().split_whitespace().map(|x| x.parse().unwrap()).collect();

    count_apples_and_oranges(s, t, a, b, apples, oranges);
}
test 12
use std::io;

fn kangaroo(x1: i32, v1: i32, x2: i32, v2: i32) -> String {
    if v1 <= v2 {
        return String::from("NO");
    }
    if (x2 - x1) % (v1 - v2) == 0 {
        return String::from("YES");
    }
    String::from("NO")
}

fn main() {
    let stdin = io::stdin();
    let mut input = String::new();

    stdin.read_line(&mut input).expect("Failed to read line");
    let first_multiple_input: Vec<i32> = input.trim().split_whitespace().map(|x| x.parse().unwrap()).collect();

    let (x1, v1, x2, v2) = (first_multiple_input[0], first_multiple_input[1], first_multiple_input[2], first_multiple_input[3]);
    let result = kangaroo(x1, v1, x2, v2);

    println!("{}", result);
}
test 13
use std::io;

fn gcd(x: i32, y: i32) -> i32 {
    if y == 0 { x } else { gcd(y, x % y) }
}

fn get_total_x(a: &[i32], b: &[i32]) -> i32 {
    let lcm = |x, y| x * y / gcd(x, y);
    let lcm_a = a.iter().copied().reduce(lcm).unwrap_or(1);
    let gcd_b = b.iter().copied().reduce(gcd).unwrap();
    
    (lcm_a..=gcd_b).filter(|&i| gcd_b % i == 0 && a.iter().all(|&x| i % x == 0)).count() as i32
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let nums: Vec<i32> = input.split_whitespace().map(|s| s.parse().unwrap()).collect();
    let (n, m) = (nums[0], nums[1]);

    let a: Vec<i32> = io::stdin().lines().next().unwrap().unwrap().split_whitespace().map(|s| s.parse().unwrap()).collect();
    let b: Vec<i32> = io::stdin().lines().next().unwrap().unwrap().split_whitespace().map(|s| s.parse().unwrap()).collect();

    println!("{}", get_total_x(&a, &b));
}
test 14
use std::io;

fn breaking_records(scores: Vec<i32>) -> Vec<i32> {
    let mut min_score = scores[0];
    let mut max_score = scores[0];
    let (mut min_count, mut max_count) = (0, 0);
    
    for &score in &scores[1..] {
        if score > max_score {
            max_score = score;
            max_count += 1;
        } else if score < min_score {
            min_score = score;
            min_count += 1;
        }
    }
    vec![max_count, min_count]
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let n: usize = input.trim().parse().unwrap();

    let mut scores_input = String::new();
    io::stdin().read_line(&mut scores_input).unwrap();
    let scores: Vec<i32> = scores_input.split_whitespace().map(|s| s.parse().unwrap()).collect();

    let result = breaking_records(scores);
    println!("{} {}", result[0], result[1]);
}
test 15
use std::io;

fn birthday(s: &[i32], d: i32, m: i32) -> i32 {
    (0..=s.len() - m as usize)
        .filter(|&i| s[i..i + m as usize].iter().sum::<i32>() == d)
        .count() as i32
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let n: usize = input.trim().parse().unwrap();

    let mut s_input = String::new();
    io::stdin().read_line(&mut s_input).unwrap();
    let s: Vec<i32> = s_input.split_whitespace().map(|x| x.parse().unwrap()).collect();

    let mut first_multiple_input = String::new();
    io::stdin().read_line(&mut first_multiple_input).unwrap();
    let mut first_multiple_iter = first_multiple_input.split_whitespace();
    let d: i32 = first_multiple_iter.next().unwrap().parse().unwrap();
    let m: i32 = first_multiple_iter.next().unwrap().parse().unwrap();

    let result = birthday(&s, d, m);
    println!("{}", result);
}
test 16
use std::io;

fn divisible_sum_pairs(n: usize, k: i32, ar: &[i32]) -> i32 {
    let mut count = 0;
    for i in 0..n {
        for j in i + 1..n {
            if (ar[i] + ar[j]) % k == 0 {
                count += 1;
            }
        }
    }
    count
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let first_line: Vec<usize> = input.split_whitespace().map(|x| x.parse().unwrap()).collect();
    let n = first_line[0];
    let k: i32 = first_line[1] as i32;

    input.clear();
    io::stdin().read_line(&mut input).unwrap();
    let ar: Vec<i32> = input.split_whitespace().map(|x| x.parse().unwrap()).collect();

    let result = divisible_sum_pairs(n, k, &ar);
    println!("{}", result);
}
test 17
use std::collections::HashMap;

fn migratory_birds(arr: Vec<i32>) -> i32 {
    let mut count = HashMap::new();
    for &bird in &arr {
        *count.entry(bird).or_insert(0) += 1;
    }
    
    let max_count = count.values().cloned().max().unwrap();
    let mut result = i32::MAX;

    for (&bird, &c) in &count {
        if c == max_count && bird < result {
            result = bird;
        }
    }
    
    result
}

fn main() {
    let mut arr_count = String::new();
    std::io::stdin().read_line(&mut arr_count).unwrap();
    let arr_count: usize = arr_count.trim().parse().unwrap();

    let mut arr = String::new();
    std::io::stdin().read_line(&mut arr).unwrap();
    let arr: Vec<i32> = arr.split_whitespace()
                           .map(|s| s.parse().unwrap())
                           .collect();

    println!("{}", migratory_birds(arr));
}
test 18
use std::io;

fn bon_appetit(bill: Vec<i32>, k: usize, b: i32) {
    let anna_share = (bill.iter().sum::<i32>() - bill[k]) / 2;
    let result = if b == anna_share {
        String::from("Bon Appetit")
    } else {
        (b - anna_share).to_string()
    };
    println!("{}", result);
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let (_, k): (usize, usize) = {
        let mut iter = input.split_whitespace().map(|x| x.parse::<usize>().unwrap());
        (iter.next().unwrap(), iter.next().unwrap())
    };
    
    let mut bill = String::new();
    io::stdin().read_line(&mut bill).unwrap();
    let bill: Vec<i32> = bill.split_whitespace().map(|x| x.parse().unwrap()).collect();

    let mut b_temp = String::new();
    io::stdin().read_line(&mut b_temp).unwrap();
    let b = b_temp.trim().parse::<i32>().unwrap();

    bon_appetit(bill, k, b);
}
test 19
use std::collections::HashMap;
use std::io;

fn sock_merchant(n: usize, ar: Vec<i32>) -> i32 {
    let mut counts = HashMap::new();
    for sock in ar {
        *counts.entry(sock).or_insert(0) += 1;
    }
    counts.values().map(|&count| count / 2).sum()
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let n: usize = input.trim().parse().unwrap();

    input.clear();
    io::stdin().read_line(&mut input).unwrap();
    let ar: Vec<i32> = input.split_whitespace().map(|x| x.parse().unwrap()).collect();

    let result = sock_merchant(n, ar);
    println!("{}", result);
}
test 20
use std::io;

fn page_count(n: i32, p: i32) -> i32 {
    let from_front = p / 2;
    let from_back = (n / 2) - (p / 2);
    from_front.min(from_back)
}

fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).unwrap();
    let n: i32 = input.trim().parse().unwrap();

    input.clear();
    io::stdin().read_line(&mut input).unwrap();
    let p: i32 = input.trim().parse().unwrap();

    let result = page_count(n, p);
    println!("{}", result);
}
