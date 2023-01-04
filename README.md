# Stimulsoft Dashboards.PHP

#### Stimulsoft Dashboards.PHP is a complete software package for designing and viewing dashboards. You may use the tool for integration into your applications or as a standalone solution. At the same time, no complex configuration or third-party modules are required. You may easily integrate dashboards into almost any PHP application.

# Installation
The product is distributed using the [Composer](https://getcomposer.org/) repository. You can add the necessary libraries using the command:

```
composer require stimulsoft/dashboards-php
```

# Usage
Add the minimum required code to the page:
```php
<?php
require_once 'vendor/autoload.php';
?>
```

Render the necessary scripts in the `<head>` section
```php
<head>
<?php
    $js = new \Stimulsoft\StiJavaScript(\Stimulsoft\StiComponentType::Viewer);
    $js->renderHtml();
?>
</head>
```

Create and render a request handler in the `<script>` section of the page:
```php
<script>
<?php
    $handler = new \Stimulsoft\StiHandler();
    $handler->renderHtml();
?>
</script>
```

Create and render the component in the `<script>` section of the page:
```php
<script>
<?php
    $viewer = new \Stimulsoft\Viewer\StiViewer();
    $report = new \Stimulsoft\Report\StiReport();
    $report->loadFile('reports/SimpleDashboard.mrt');
    $viewer->report = $report;
    $viewer->renderHtml();
?>
</script>
```

# Useful links:

[Live Demo](http://demo.stimulsoft.com/#Js)

[Sample Projects](https://github.com/stimulsoft/Samples-Dashboards-JS-PHP)

[Product Page](https://www.stimulsoft.com/en/products/dashboards-php)

[Free Download](https://www.stimulsoft.com/en/downloads)

[License](LICENSE.md)
