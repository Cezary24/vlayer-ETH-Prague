# Vlayer ETHGlobal Prague

Vlayer is a project utilizing zero-knowledge proof technology to verify OpenAI responses. The project enables:

- Secure verification of OpenAI API responses
- Generation of zero-knowledge proofs for responses
- Blockchain integration (Base)
- Verification of AI response authenticity

## Project Goal

The main objective of the project is to verify whether data regarding proposed tokens for purchase actually originates from OpenAI. The implementation uses the kraken-web-proof template.

## Implementation

### Smart Contracts
- Created OpenAIProver and OpenAIVerifier contracts
- Contracts were deployed on Base Mainnet using the `openai-prove.ts` script
- Web content verification works correctly using the SDK

### Implementation Challenges

1. **Gas Consumption**
   - High gas costs during blockchain operations

2. **Prove Function Issues**
   - Application hangs on the prove request
   - Lack of detailed error information
   - Timeout occurs without additional diagnostic information

3. **Configuration Issues**
   - Problematic reading of values from .env files
   - Required direct input of `EXAMPLES_TEST_PRIVATE_KEY` and `VLAYER_API_TOKEN` during script execution
   - "Invalid keys" errors despite properly configured .env files
   - Environment-related errors (prod vs test)
   - Issues with `estimateContractGas` due to "Invalid proof" errors

### Positive Aspects
- Intuitive Webproof creation using SDK
- Well-documented implementation process
- Effective web content verification
- Intuitive smart contract development
- Straightforward tool installation

## Features

- OpenAI response verification
- Zero-knowledge proof generation
- Smart contract integration
- Blockchain verification

## Suggestions for Improvement

1. **Debugging and Error Handling**
   - More information available with `DEBUG=*`
   - Detailed error informations
   - Immediate error reporting in the prove function

2. **Documentation**
   - More end-to-end examples
   - Examples requiring authorization access
   - Better environment configuration documentation

3. **Development Experience**
   - Improved error messages
   - Better handling of environment variables
   - More robust gas estimation


## Technologies

- Next.js
- Wagmi
- Vlayer SDK
- OpenAI API
- Zero-knowledge proofs
- Base (Layer 2)
