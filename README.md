# omb
<div id="wrgsv"></div>
<script type="text/javascript">
var wrgsv = {
	idBox: 'wrgsv',
	url_wiget: 'https://test.proweblab.xyz/widget/widget.php?post=1286',
	init: function(id) {
	    if (!id) { id = this.idBox; }
	    if (document.getElementById(id)) {
	        this.addStyle();
	        try {
                var XHR = ("onload" in new XMLHttpRequest()) ? XMLHttpRequest : XDomainRequest;
            	var xhr = new XHR();
            	xhr.open('GET', this.url_wiget, true);
            	xhr.onload = function() {
            	    if (this.response) {
                        document.getElementById(id).innerHTML = this.response;
                    }
            	}
            	xhr.onerror = function() { console.log('onerror '+this.status); }
    	        xhr.send();
	        } catch(e) {}
	    } else { console.log('The specified block ID "'+id+'" is missing'); }
	},
	addStyle: function() {
	    style = document.createElement('link');
        style.rel = 'stylesheet';
        style.type = 'text/css';
        document.head.appendChild(style);
	},
};
</script>
<script type="text/javascript">wrgsv.init();</script>
