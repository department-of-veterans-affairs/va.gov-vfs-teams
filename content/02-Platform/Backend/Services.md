---
title: Backend API Reference
label: API Reference
---

<div id="swagger-ui"></div>

<link rel="stylesheet" href="../../../api-reference/swagger-ui.css" type="text/css">
<script src="../../../api-reference/swagger-ui-bundle.js"> </script>
<script src="../../../api-reference/swagger-ui-standalone-preset.js"> </script>

<script>
	var url = "https://dev-api.vets.gov/v0/apidocs";

	if(window.location.href.match(/localhost/)){
		url = "http://localhost:3000/v0/apidocs";
	}

  const ui = SwaggerUIBundle({
    url: url,
    dom_id: '#swagger-ui',
    deepLinking: true,
    presets: [
      SwaggerUIBundle.presets.apis,
      SwaggerUIStandalonePreset
    ],
    plugins: [
      SwaggerUIBundle.plugins.DownloadUrl
    ],
    layout: "StandaloneLayout"
  })

  window.ui = ui
</script>

