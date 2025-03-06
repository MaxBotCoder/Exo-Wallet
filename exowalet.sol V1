//SPDX-License-Identifier: MiT
pragma solidity 0.8.14;

contract mycode {

    uint public globalvalue = address(this).balance;

    uint public functionvalue; //Debuging no 2

    uint public quantitywithdrawn;

    string public executionstatus = "null";

    string public transactionstatus = "null";

    string public withdrawstatus = "null";

    address public publisher;

    mapping (address => mapping(address => bool)) public approvedaddress;

    constructor (address approved, bool approvestatus) {

        approvedaddress[approved][publisher] = approvestatus;

        publisher = msg.sender;

    }

    function sendmoneytoapproved(address to) payable public {

        functionvalue = msg.value;

        if(approvedaddress[to][publisher] = true){

        payable(to).call{value: msg.value}("");

        executionstatus = "succsessfull execution";

        } else if (approvedaddress[to][publisher] = false) {

        executionstatus = "failed execution";


        }

    } 


    function withdraw(uint towithdrawvalue) public payable {

       payable (publisher).transfer(towithdrawvalue);

    }


}
