<script>
	import '../app.css';
	import Header from '../lib/components/header.svelte';
	import { Client, Account, ID } from 'appwrite';
	const client = new Client();

	client.setEndpoint('https://cloud.appwrite.io/v1').setProject('649ae9651ccb6065b211');
	const account = new Account(client);

	// Register User
	account.create(ID.unique(), 'me@example.com', 'password', 'Jane Doe').then(
		(response) => {
			console.log(response);
		},
		(error) => {
			console.log(error);
		}
	);
</script>

<body class="container mx-auto">
	<Header />
	<slot />
</body>
