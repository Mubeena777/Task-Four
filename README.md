# Task Four

In this task, we will create two programs in Kali Linux. The first one is a Rust program that prints "Hello Mubeena D, right now the time is <current time>". The second is a PHP file that outputs the same message. This document will guide you through the process of installing the required software and writing the programs.

## Rust Program

### Step 1: Install Rust in Kali Linux
1. Open Terminal: We can do this by searching for "Terminal" in our applications.
2. Install Rust using rustup: Run the following command to download and install rustup, which will manage our Rust installation:
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

3.  Follow the Installation Prompts: The script will guide us through the installation. We can usually select the default options by pressing 1 when prompted.

4. Update our Path: After installation, We need to add Rust to our PATH. We can do this by adding the following line to our .bashrc or .bash_profile file:
```
export PATH="$HOME/.cargo/bin:$PATH"
```
Then run:
```
source ~/.bashrc
```
5. Verify Installation: Check if Rust is installed correctly by running:
```
rustc --version
```
### Step 2: Create a New Rust Project
1. Create a New Directory for our Project:
```
mkdir hello_rust
cd hello_rust
```
2. Create a New Rust Project: Run the following command to create a new Rust project using Cargo (Rust's package manager):
```
cargo init
```
### Step 3: Edit the Main Rust File
1. Open the Main File: Open src/main.rs in our preferred text editor For example:
```
nano src/main.rs
```
2. Write the Rust Code: Replace the contents of src/main.rs with the following code:
```
use chrono::Local;

fn main() {
    let current_time = Local::now().format("%Y-%m-%d %H:%M:%S").to_string();
    println!("Hello Mubeena D, right now the time is {}", current_time);
}
```
### Step 4: Add the Chrono Dependency
1.Open Cargo.toml: This file is located in the root of our project directory. Open it with:
```
nano Cargo.toml
```
2. Add the Chrono Dependency: Under the [dependencies] section, add the following line:
```
chrono = "0.4"
```
### Step 5: Build and Run Our Program
1. Build the Program: In our project directory, run:
```
cargo build
```
2. Run the Program: After building, We can run the program with:
```
cargo run

```
### Final Output
``
Hello Mubeena D, right now the time is 2024-09-27 15:30:45
``

## php Program

### Step 1: Install PHP
1. Open Terminal: We can do this by searching for "Terminal" in our applications.

2. Update Package List: Run the following command to update our package list:

```
sudo apt update
```
3. Install PHP: Run the following command to install PHP and the Apache web server:
```
sudo apt install php
```
4. Verify PHP Installation: Check if PHP is installed correctly by running:

```
php -v
```
### Step 2: Create a PHP File
1. Create a New PHP File: Use a text editor to create a new PHP file. For example, to create a file named hello.php, run:
```
nano hello.php
```
3. Write the PHP Code: Add the following code to the hello.php file:

```
<?php
date_default_timezone_set('Asia/Kolkata'); // Replace with your timezone
echo "Hello Mubeena D, right now the time is " . date("Y-m-d H:i:s");
?>
```
Note: Replace Our/Timezone with your actual timezone (e.g., Asia/Kolkata, America/New_York). We can find the list of supported timezones here.
4. Save and Exit:
- If you're using nano, press CTRL + S, then CTRL + X.
### Step 3: Run Our Program
1. We can run the program with:

```
php hello.php
```
### Final Output
``
Hello Mubeena D, right now the time is 2024-09-27 15:30:45
``
SAMPLE OF PHP
[PHP](https://github.com/Mubeena777/taskfour/blob/main/php.png)







