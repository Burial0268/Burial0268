```php
<?php
namespace Humans\Burial0268;
use Humans\Burial0268\Introduction;
use Humans\HumanBeingInterface;

class About extends Me implements HumanBeingInterface
{

    public function __construct(Introduction $introduction)
    {
        parent::__construct($introduction);
        $this->info = $introduction->infoList;
        $introduction->BootStrap($this);
    }

    public function batchAllInfo(): array
    {
        return $this->info;
    }

    public function toVarDump(mixed $data): mixed
    {
        return var_dump($data);
    }
}
```

```php
[Log/Boot] Strating introduction... done
[Log]      Initialize the introduction process... done

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


My common info: array(4) {
    [0]=>
    string(37) "🔭 I’m currently working on GBCLstudio"
    [1]=>
    string(41) "🌱 A completely stupid high school student"
    [2]=>
    string(46) "Super Minecraft Fans! Also old things and SBCs"
    [3]=>
    string(60)   "EDM lover, rhytem games overdose, btw sub Porter Robinson :D"
}

My project info: array(2) { 
    ["FoF-Upload-Qcloud"]=>
    string(47) "https://github.com/GBCLStudio/FoF-Upload-Qcloud"
    ["Flarum-UserIP"]=> 
    string(36) "https://github.com/GBCLStudio/userip"
} 

Tech stack: array(3) {
    ["Backend"]=>
    string(24) "PHP(8.x), Laravel, Flarum"
    ["Frontend"]=>
    string(38) "React, Vue, Vanilla JS, Mithril, Astro"
    ["Other"]=>
    string(24) "CDN, VPS, DNS, WAF, Tauri"
}

My position: string(14) "China Mainland"

My goal: array(4) { 
    [0]=> 
    string(14) "Keep Alive😇"
    [1]=> 
    string(10) "Study Rust" 
    [2]=> 
    string(39) "Finish the college entrance examination" 
    [3]=> 
    string(29) "To contribute to open source." 
}
```

