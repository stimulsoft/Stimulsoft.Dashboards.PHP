# Stimulsoft Dashboards.PHP

#### Stimulsoft Dashboards.PHP is a complete software package for designing and viewing dashboards. You may use the tool for integration into your applications or as a standalone solution. At the same time, no complex configuration or third-party modules are required. You may easily integrate dashboards into almost any PHP application, including those built on the Laravel framework.

# Installation
You can add the necessary libraries using the command:
```
composer require stimulsoft/dashboards-php
```

# Usage
To work with the dashboard viewer, use the following code:
```php
<?php
require_once 'vendor/autoload.php';
 
use Stimulsoft\Report\StiReport;
use Stimulsoft\Viewer\StiViewer;
 
$viewer = new StiViewer();
$viewer->process();
 
$report = new StiReport();
$report->loadFile('reports/SimpleDashboard.mrt'); 
$viewer->report = $report;
 
$viewer->printHtml();
?>
```

To work with the dashboard designer, use the following code:
```php
<?php
require_once 'vendor/autoload.php';
 
use Stimulsoft\Report\StiReport;
use Stimulsoft\Designer\StiDesigner;
 
$designer = new StiDesigner();
$designer->process();
 
$report = new StiReport();
$report->loadFile('reports/SimpleDashboard.mrt'); 
$designer->report = $report;
 
$designer->printHtml();
?>
```

These code examples are basic. There are many features, options, and other variations. For details, see our examples and documentation. For more details, please see our [examples](https://github.com/stimulsoft/Samples-Dashboards.PHP) and [documentation](https://www.stimulsoft.com/en/documentation/online/programming-manual/reports_and_dashboards_for_php.htm).

# Useful links:
* [Live Demo](http://demo.stimulsoft.com/#Js)
* [Product Page](https://www.stimulsoft.com/en/products/dashboards-php)
* [Sample Projects](https://github.com/stimulsoft/Samples-Dashboards.PHP)
* [Documentation](https://www.stimulsoft.com/en/documentation/online/programming-manual/reports_and_dashboards_for_php.htm)
* [Free Download](https://www.stimulsoft.com/en/downloads)
* [License](LICENSE.md)
