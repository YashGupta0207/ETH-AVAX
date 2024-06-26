# Admission Class1

This Solidity program is a simple contract that checks the eligibility for a Admission in Class 1 based on the user's age. The purpose of this program is to demonstrate basic conditional checks, error handling using `require`, `assert`, and `revert`, and provide a foundation for more complex Solidity programming tasks.

## Description

This program includes a smart contract written in Solidity for the Ethereum blockchain, featuring two key functions:

checkEligibility: This function determines whether an individual qualifies for admission into Class1 in India based on their age.
applyForAdmission: This function illustrates the use of revert to manage scenarios where the applicant's age is under 6.            

In the checkEligibility function:                
1.The 'require' statement ensures the applicant is at least 6 years old.          
2.The 'assert' statement further verifies that the age is exactly 6.        
3.It returns suitable messages depending on the applicant's age.          

In the applyForAdmission function:          
1.The 'revert' statement is used to handle cases where the applicant is too young to apply.

## Getting Started

### Executing Program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at [https://remix.ethereum.org](https://remix.ethereum.org).

1. **Create a New File**:
    - Once you are on the Remix website, create a new file by clicking on the "Create New File" icon in the left-hand sidebar.
    - Save the file with a `.sol` extension (e.g., `admission.sol`).
    - Copy and paste the following code into the file:
  
    -  
      ```solidity
      // SPDX-License-Identifier: MIT
       pragma solidity >=0.8.0;
      contract AdmissionClasss1 {
       // Function to check eligibility for taking admission
      function checkEligibility(uint _age) public pure returns (string memory) {
        // Check if age is 6 or above
        require(_age >= 6, "You must be above 6 to take admission in Class 1 in India");
        // If age is 6, congratulate the applicant and assert age is exactly 6
        if (_age == 6) {
        assert(_age == 6);
         return "Congratulations! You are now eligible to take Admission";
      }
        // If age is above 6, return eligibility message
      return "You are eligible to take admission";
       }
      // Function to demonstrate revert if age is below 6
      function applyForAdmission(uint _age) public pure returns (string memory) {
        // Revert if age is below 18
        if (_age < 6) {
        revert("You are not eligible to take admission, age must be 6 or above");
       }
        // Return eligibility message
        return "You are eligible to take admission";
      }
        }
      ```

2. **Compile the Code**:
    - Click on the "Solidity Compiler" tab in the left-hand sidebar.
    - Make sure the "Compiler" option is set to a compatible version, such as "0.8.0".
    - Click on the "Compile Admission.sol" button.

3. **Deploy the Contract**:
    - Once the code is compiled, go to the "Deploy & Run Transactions" tab in the left-hand sidebar.
    - Select the "AdmissionClass1" contract from the dropdown menu.
    - Click on the "Deploy" button.

4. **Interact with the Contract**:
    - Once the contract is deployed, you can interact with it by calling the `checkEligibility` and `applyForAdmission` functions.
    - Click on the "AdmissionClass1" contract in the left-hand sidebar.
    - Click on the `checkEligibility` function, enter an age, and click "transact" to see if the person is eligible for a Admission.
    - Click on the `applyForAdmission` function, enter an age, and click "transact" to see if the person can apply for a Admission.

## Authors

YASH GUPTA  
[@YASH GUPTA]

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
