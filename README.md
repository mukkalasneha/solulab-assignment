# solulab-assignment
webapp to connect metamask.
const Web3 = require("web3");

export const LoadWeb3 = async () => {
  if (window.ethereum) {
    window.web3 = new Web3(window.ethereum);
    await window.ethereum.enable();
  }

  else if (window.web3) {
    window.web3 = new Web3(window.web3.currentProvider);
  }

  else{
    window.alert(
      "Consider using metamask or web3 compatible browser(Mist)."
    );
  }
};
