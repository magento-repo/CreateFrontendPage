# Create New Page in Frontend

1. Create a etc/module.xml and registration.php to register your module
2. Define routes.xml under etc/frontend<br>
    <i><b>route id="learning" frontName="learningpath"</b><br>
    rount id used to create a layout file<br>
    frontendName used in the frontend navigation<i>
3. Create layout file under view/frontend/layout/learning_index_index.xml<br>
    <i>Layout filename should be RouteId/ControllerFolderName/FileName<br>
    Route id => learning<br>
    ControllerFolderName => index<br>
    FileName => index</i>
4. Define block and phtml in your layout file<br>
    <i><b>block class="LearningPath\CreateFrontendPage\Block\Index\Index" name="learning_index_index" template="LearningPath_CreateFrontendPage::index.phtml"</b><br>
    class - says which block file assigned to the template.<br>
    name - should be unquie<br>
    template - says where to define the phtml file</i>
5. Create a block file under Block/Index/Index.php<br>
   <i> All bussiness logic would be do it in block file.</i>
6. Create a phtml file under view/frontend/templates/index.phtml<br>
    <i>Onscreen look and feel would be defined in the phtml file </i>
7. Create a controller file under Controller/Index/Index.php <br>
    <i>Will do all action in the controller file.</i>
8. Run below commands<br>
    <i>php bin/magento setup:di:compile && php bin/magento setup:static:deploy -f && php bin/magento cache"clean<i>
9. Verify in the frontend {base_url}/routeFrontName i.e., http://127.0.0.1/magento2/learningpath
