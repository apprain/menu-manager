# Menu Manager
Interactive Drag and Drop Menu Manager 

# Description
This menu manager help to create site menu by drag and drop and publish in website. 


#How to use 

After installation go the Applications > Menu Manager 

Add new menu, arrange submenu in the tree and save. clik on Regresh Preview button to see the preview in the menu.


To display in the site menu :

* Step 1: Go to Preference Tab > Theme 
* Step 2: In Theme Subnav click on Header.The header will load in a editor.
* Step 3: Copy below user hook in the header 

        Remove below block: 
        <?php
           echo $this->siteMenuClear()
              ->siteMenu($this->baseurl("/"), 'Home', 'home')
             ->setRootHtmlOpts(array('class' => 'nav navbar-nav'))
             ->siteMenuRender('HTML', (isset($selected) ? $selected : ""), 'active');
  		  ?>
  		  
  		  Add below block
        <?php App::Hook('UI')->Render('menu_manager_nave'); #User Interface Hook ?>
        
        
  

