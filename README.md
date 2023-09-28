# aptos-social-network-contract
Move module for Aptos Social Network dApp.

## Developing

### Compile:
```sh
aptos move compile
```

### Publish:
```sh
aptos move publish
```

## Interacting With The Contract

### Initialize the social network:
```sh
aptos move run --function-id <MODULE-ADDRESS>::social_network::init
```

### Create a user profile:
```sh
aptos move run --function-id <MODULE-ADDRESS>::social_network::create_user_profile --args 'string:<NAME>' 'string:<BIO>' 'string:<PFP-URL>'
```

### Update a user profile:
```sh
aptos move run --function-id <MODULE-ADDRESS>::social_network::update_user_profile --args 'string:<NAME>' 'string:<BIO>' 'string:<PFP-URL>'
```

### Make a post:
```sh
aptos move run --function-id <MODULE-ADDRESS>::social_network::make_post --args 'string:<CONTENT>' 'string:<IMAGE-URL or none>'
```

### Make a comment:
```sh
aptos move run --function-id <MODULE-ADDRESS>::social_network::make_comment --args 'address:<POST-OWNER-ADDRESS>' 'u64:<POST-INDEX>' 'string:<COMMENT-CONTENT>'
```

### Like a post:
```sh
aptos move run --function-id <MODULE-ADDRESS>::social_network::like_post --args 'address:<POST-OWNER-ADDRESS>' 'u64:<POST-INDEX>'
```

### Like a comment:
```sh
aptos move run --function-id <MODULE-ADDRESS>::social_network::like_comment --args 'address:<POST-OWNER-ADDRESS>' 'u64:<POST-INDEX>' 'u64:<COMMENT-INDEX>'
```