1.) Description:
		This challenge, incites one to gain immense insight into Metaplex's NFT Standard

	Challenge questions: 
		q. What are NFTs :
			a. Non Fungible Tokens, They are unduplicatable Tokens.
		q. List 4 fields of a metadata URI: 
			a. {Name, Symbol, Description, Image, Animation_url, Externa, Url, Atrributes} 
		q. How to do a Cross Program Invocation: 
			a. Utilize the Invoke or Invoke_signed method in a program instruction, specifying program the instructions, Accounts, and signatures if necessary
		q. How to Mint an NFT via CPI: 
			a. Cross Program invocate the create_metadata_account instruction, with a token mint of supply 1, mint authority, and and an appropriate metadata URI https://docs.metaplex.com/programs/token-metadata/instructions

	Resources:
		Metaplex Docs: https://docs.metaplex.com/programs/token-metadata/instructions#verify-the-collection
		Solana Cookbook Cross Program Invocations: https://solanacookbook.com/references/programs.html#how-to-do-cross-program-invocation
		Solana Cookbook NFTs: https://solanacookbook.com/references/nfts.html#non-fungible-tokens-nfts

2.) 	Description:
		This challenge, incites one to gain immense insight about what Program Derived addresses(PDAs) are, Finding one, and Signing Transactions with one.
	
	Challenge questions: 
		q. What are PDAs
			a. Program Derived addresses: These are addresses off the ed25519 curve, hence have no private keys. They are utilized by Program to sign transactions using the invoke_signed function.
		q. How to do a Cross Program Invocation: 
			a. Utilize the Invoke or Invoke_signed method in a program instruction, specifying the Transaction instructions, Accounts, and signatures if necessary, or use anchor's cpiContext
		q.) How to sign a transaction with a PDA:
			a.) use the invoke_signed function to provide the seed and bump utilized to generate the pda, alongside the TransactionInstruction + the accounts.
		q.) How to store data into an account
			a.) Create the account to stor the data into while allocating the appropriate space, and providen enough rent lamports, then add the data in question into the data field of the account info struct, utilizing the program that owns the account.

	Resources:
		PDAs Solana bytes: https://www.youtube.com/watch?v=ZwFNPvqUclM
		Solana Cookbook Cross Program Invocations: https://solanacookbook.com/references/programs.html#how-to-do-cross-program-invocation
		PaulX Escrow program sample: https://paulx.dev/blog/2021/01/14/programming-on-solana-an-introduction/
		Solana Cookbook PDAs: https://solanacookbook.com/core-concepts/pdas.html#program-derived-addresses-pdas
		anchor sample escrow: https://hackmd.io/@ironaddicteddog/anchor_example_escrow
		solana docs: https://docs.solana.com/developing/programming-model/accounts
		spl Program Token Transfer: https://github.com/solana-labs/solana-program-library/blob/master/token/program-2022/src/instruction.rs#L143
	
	
3.) 	Description:
		This challenge, incites one to gain immense insight into Solana Transaction v2 format, and apply it to a plausible problem

	Challenge questions: 
		q. What are PDAs
			a. Program Derived addresses: These are addresses off the ed25519 curve, hence have no private keys. They are utilized by Program to sign transactions using the invoke_signed function.
		q. How to do a Cross Program Invocation: 
			a. Utilize the Invoke or Invoke_signed method in a program instruction, specifying the Transaction instructions, Accounts, and signatures if necessary or use anchor's cpiContext
		q.) How to sign a transaction with a PDA:
			a.) use the invoke_signed function to provide the seed and bump utilized to generate the pda, alongside the TransactionInstruction + the accounts, or use anchor's CpiContext::new_with_signer
		q. How to transfer a Token via CPI: 
			a.) Invoke, Invoke_sign, or CPIContext the Transfer Instruction: https://github.com/solana-labs/solana-program-library/blob/master/token/program-2022/src/instruction.rs#L143


	Resources:
		
		Transaction v0 & Lookup tables Solana bytes: https://www.youtube.com/watch?v=8k68cMeLX2U&t=14s
		Solana Cookbook Cross Program Invocations: https://solanacookbook.com/references/programs.html#how-to-do-cross-program-invocation
		spl Program Token Transfer: https://github.com/solana-labs/solana-program-library/blob/master/token/program-2022/src/instruction.rs#L143
	
