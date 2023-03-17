```php
<?php
namespace Humans\Burial0268;
use Humans\Burial0268\Introduction;

class About extends Me{

    public function __construct()
    {
        parent::__construct();
        $Introduction = new Introduction();
        $this->info = $Introduction->infoList;
        $Introduction->BootStrap();
    }

    public function getCommonInfo(): string
    {
        $Introduction->showMyProfileCard();
        return 'My common info: ' . var_dump($this->info->common);
    }
    public function getProjectList(): string
    { return 'My project info: ' . var_dump($this->info->project); }
    
    public function getMyStack(): string
    { return 'Tech stack: ' . var_dump($this->info->techStack); }
  
    public function getMyPosition(): string
    { return 'My position: ' . var_dump($this->info->location); }
    
    public function getFutureGoal(): string
    { return 'My goal: ' . var_dump($info->ftrGoal); }
}

$About = new Me();
echo $About->all();
```

```php
Strating introduction... done
Initialize the introduction process... done

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


My common info: array(3) {
    [0]=>
    string(41) "🔭 I’m currently working on GBCLstudio"
    [1]=>
    string(39) "🌱 I’m currently learning JavaScript"
    [2]=>
    string(39) "I am a Genshin Impact（天空岛） player, 大佬求带"
}

My project info: array(3) { 
    ["FoF-Upload-Qcloud"]=>
    string(47) "https://github.com/GBCLStudio/FoF-Upload-Qcloud" 
    ["Bili_Video"]=> 
    string(40) "https://github.com/GBCLStudio/Bili_Video" 
    ["Domain-Resolver-PHP"]=> 
    string(49) "https://github.com/GBCLStudio/Domain-Resolver-PHP" 
} 

Tech stack: array(3) {
    ["Backend"]=>
    string(25) "PHP(8.x), Laravel, Flarum"
    ["Frontend"]=>
    string(18) "Basic Html5 & CSS3"
    ["Other"]=>
    string(18) "CDN, VPS, DNS, WAF"
}

My position: string(14) "China Mainland"

My goal: array(4) { 
    [0]=> 
    string(30) "Study another foreign language" 
    [1]=> 
    string(16) "Study JavaScript" 
    [2]=> 
    string(43) "Finish the high school entrance examination" 
    [3]=> 
    string(29) "To contribute to open source." 
}
```

