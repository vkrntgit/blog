<script>
</script>

<svelte:head />

<div class="content">
	<h1>
		Kubernetes - The very basics : Configuring K8 and troubleshooting initial setup issues on Linode
	</h1>

	<h2>What's the story</h2>
	I am playing around with a free Linode subscription. I have $300 to burn. My objective is to try and
	create a complete kubernetes setup and host a website (app + db). Then learn to manage the site, deploy
	new code and monitor what's happening with the traffice and new apps.

	<br /><br />
	I started off by creating a cluster on Linode (<a
		href="https://www.linode.com/docs/guides/deploy-and-manage-a-cluster-with-linode-kubernetes-engine-a-tutorial/#create-an-lke-cluster"
	>
		pretty straightforward</a
	>). Added a couple of nodes to the server. Then I connected to the node, installed kubernetes-cli
	and
	<h2>The first issue I faced was this error:</h2>

	"The connection to the server localhost:8080 was refused - did you specify the right host or
	port?"
	<br /><br />
	<h2>How I fixed it:</h2>

	Downloaded the kubeconfig file.<br />Copied the contents to /etc/kubernetes/admin.conf on the
	primary node.
	<br />
	Then copied /etc/kubernetes/admin.conf to ~/.kube/
	<br />Restarted the kubelet using
	<br /> "service kubelet restart"
	<br /><br />
</div>
