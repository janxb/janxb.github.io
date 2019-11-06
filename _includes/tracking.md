<noscript><p><img src="https://matomo.janbrodda.de/trck.html?idsite=4&rec=1" alt=""/></p></noscript>
<script type="text/javascript">
	const trackingBaseUrl = 'https://matomo.janbrodda.de/trck';
	const trackingPageId = 4;
	const trackingValidation = new Image(1, 1);
	trackingValidation.onload = function () {
		const d = document, g = d.createElement('script'), s = d.getElementsByTagName('script')[0];
		g.src = trackingBaseUrl + '.js';
		g.async = true;
		g.defer = true;
		s.parentNode.insertBefore(g, s);

		function waitForTracker() {
			if (typeof Piwik !== "undefined") {
				const tracker = Piwik.getTracker(trackingBaseUrl + ".html", trackingPageId);
				tracker.enableLinkTracking();
				tracker.trackPageView();
			} else {
				setTimeout(waitForTracker, 100);
			}
		}

		waitForTracker();
	};
	trackingValidation.onerror = function () {
		const d = document, g = d.createElement('img'), s = d.getElementsByTagName('script')[0];
		g.src = trackingBaseUrl + '.html?idsite=' + trackingPageId + '&rec=1';
		s.parentNode.insertBefore(g, s);
	};
	trackingValidation.src = trackingBaseUrl + '.html?action_name=&idsite=' + trackingPageId + '&rec=0&send_image=1';
</script>
