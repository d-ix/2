

pragma solidity 0.8.24;

import "forge-std/Test.sol";

contract MaliciousReceiver {
    // Намеренно НЕТ receive() или fallback()
}

contract ReceiverContractPoc is Test {
    function test_closeTrove_reverts_if_receiver_is_contract() public {
        MaliciousReceiver receiver = new MaliciousReceiver();


}

