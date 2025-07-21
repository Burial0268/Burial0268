```rust
// hi, I'm Burial0268 👋

mod humans {
    pub struct Introduction {
        pub info_list: Vec<&'static str>,
        pub projects: std::collections::HashMap<&'static str, &'static str>,
        pub tech_stack: std::collections::HashMap<&'static str, &'static str>,
        pub position: &'static str,
        pub goals: Vec<&'static str>,
    }

    pub struct About {
        pub intro: Introduction,
    }

    impl About {
        pub fn bootstrap(&self) {
            println!("[Log/Boot] Starting introduction... done");
            println!("[Log]      Initialize the introduction process... done");

            println!(
r#"
      ___           ___           ___       ___       ___     
     /\__\         /\  \         /\__\     /\__\     /\  \    
    /:/  /        /::\  \       /:/  /    /:/  /    /::\  \   
   /:/__/        /:/\:\  \     /:/  /    /:/  /    /:/\:\  \  
  /::\  \ ___   /::\~\:\  \   /:/  /    /:/  /    /:/  \:\  \ 
 /:/\:\  /\__\ /:/\:\ \:\__\ /:/__/    /:/__/    /:/__/ \:\__\
 \/__\:\/:/  / \:\~\:\ \/__/ \:\  \    \:\  \    \:\  \ /:/  /
      \::/  /   \:\ \:\__\    \:\  \    \:\  \    \:\  /:/  / 
      /:/  /     \:\ \/__/     \:\  \    \:\  \    \:\/:/  /  
     /:/  /       \:\__\        \:\__\    \:\__\    \::/  /   
     \/__/         \/__/         \/__/     \/__/     \/__/    
"#);
        }

        pub fn dump(&self) {
            println!("\nMy common info: {:#?}", self.intro.info_list);
            println!("My project info: {:#?}", self.intro.projects);
            println!("Tech stack: {:#?}", self.intro.tech_stack);
            println!("My position: {}", self.intro.position);
            println!("My goals: {:#?}", self.intro.goals);
        }
    }
}

fn main() {
    use std::collections::HashMap;
    use humans::{About, Introduction};

    let intro = Introduction {
        info_list: vec![
            "🔭 Currently working on GBCLstudio",
            "🌱 A completely stupid student",
            "🎮 Minecraft fan + retro tech & SBCs lover",
            "🎵 EDM addicted, rhythm game enjoyer (sub Porter Robinson!)",
        ],
        projects: HashMap::from([
            ("FoF-Upload-Qcloud", "https://github.com/GBCLStudio/FoF-Upload-Qcloud"),
            ("Flarum-UserIP", "https://github.com/GBCLStudio/userip"),
        ]),
        tech_stack: HashMap::from([
            ("Backend", "PHP(8.x), Laravel, Flarum, TypeScript, Rust"),
            ("Frontend", "React, Vue, Vanilla JS, Mithril, Astro"),
            ("Other", "CDN, VPS, DNS, WAF, Tauri"),
        ]),
        position: "China Mainland",
        goals: vec![
            "Keep Alive😇",
            "Study Rust",
            "Finish endless examination",
            "To contribute to open source.",
        ],
    };

    let me = About { intro };
    me.bootstrap();
    me.dump();
}
