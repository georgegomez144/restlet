<h2>DPM's "REST-let" mini API</h2>

<div>
    <h4>Starting Up the REST-let API</h4>
    <p>You must include all correct Database Credentials inside of the config.xml file located here:</p>
    
    /app/core/etc/config.xml
</div>

<div>
    <p>Also, inside of the .htaccess file in the root of the api directory, you must provide the RewriteBase path. The 
    path is currently set to /</p>
    
    RewriteBase /
</div>

<div>
    <h4>Accessing the API</h4>
    <p>Hash credentials are required to access the API. They can be provided in one of two ways.</p>
    <ol>
        <li>Via headers (prefered method)<br />(ex. settings header in ajax request<br/>headers: {"HASH":"YOUR_HASH_CODE_HERE"}<br />)</li>
        <li>Via the $_GET param (ex: ?hash=YOUR_HASH_CODE_HERE)</li>
    </ol>
</div>

<div>
    <h4>Controller</h4>
    <p><strong>Controller Class Naming Convention:</strong> Restlet_{Module Name}_Controller_{Controller Name}</p>
    <small>Ex File Name: Get.php</small>
    <small>Ex Class Name: Restlet_Core_Controller_Get</small>
    <p><strong>Method:</strong> All routing should be appended with Action</p>
    <small>Ex: getAction() or updateAction()</small>
<div>

</div>
    <h4>Model</h4>
    <p>New Model Classes must be created under the Model directory inside of a module (base modules is 'app/modules/core')</p>
    <p><strong>Model Class Naming Convention:</strong> Restlet_{Module Name}_Model_{Model Name}</p>
    <small>Ex File Name: Core.php</small><br />
    <small>Ex Class Name: Restlet_Core_Model_Core</small>
<div>

</div>
    <h4>Helper</h4>
    <p>New Helper Classes must be created under the Helper directory inside of a module (base modules is 'app/modules/core')</p>
    <p><strong>Helper Class Naming Convention:</strong> Restlet_{Module Name}_Helper_{Helper Name}</p>
    <small>Ex File Name: Data.php</small><br />
    <small>Ex Class Name: Restlet_Core_Helper_Data</small>
    <p><strong>NOTE:</strong> Only Helpers should be used to access the Database by extending the base Helper (Restlet_Core_Helper_Data)</p>
</div>