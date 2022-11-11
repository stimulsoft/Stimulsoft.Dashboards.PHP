# Stimulsoft Dashboards.PHP

#### Stimulsoft Dashboards.PHP is a complete software package for designing and viewing dashboards. You may use the tool for integration into your applications or as a standalone solution. At the same time, no complex configuration or third-party modules are required. You may easily integrate dashboards into almost any PHP application.

# Installation
The product is distributed using the [Composer](https://getcomposer.org/) repository. You can add the necessary libraries using the command:

```
composer require stimulsoft/dashboards-php
```

# Usage
Add the minimum required namespaces to use to the page:
```php
<?php
require_once $_SERVER['DOCUMENT_ROOT'] . '/vendor/autoload.php';

use Stimulsoft\Enums\StiComponentType;
use Stimulsoft\Report\StiReport;
use Stimulsoft\StiHandler;
use Stimulsoft\StiJavaScript;
use Stimulsoft\Viewer\StiViewer;
use Stimulsoft\Viewer\StiViewerOptions;
?>
```

Render the necessary scripts in the `<head>` section
```php
<head>
<?php
    $helper = new StiJavaScript(StiComponentType::Viewer);
    $helper->renderHtml();
?>
</head>
```

Create and render a request handler in the `<script>` section of the page:
```php
<script>
<?php
    $handler = new StiHandler();
    $handler->renderHtml();
?>
</script>
```

Create and render the component in the `<script>` section of the page:
```php
<script>
<?php
    $viewer = new StiViewer();
    $report = new StiReport();
    $report->loadFile("reports/SimpleDashboard.mrt");
    $viewer->report = $report;
    $viewer->renderHtml();
?>
</script>
```

# Useful links:

You can try the [Live Demo](http://demo.stimulsoft.com/#Js)

[Sample projects](https://github.com/stimulsoft/Samples-Dashboards-JS-PHP)

Read more about [Stimulsoft Dashboards.PHP](https://www.stimulsoft.com/en/products/dashboards-php)

[Free Download](https://www.stimulsoft.com/en/downloads)

[License](LICENSE.md)
