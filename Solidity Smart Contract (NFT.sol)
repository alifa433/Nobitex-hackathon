// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC721/extensions/ERC721Enumerable.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract NFT is ERC721Enumerable, Ownable {
    constructor() ERC721("Nobitex NFT", "NNFT") {}

    uint256 private tokenIdCounter = 1;

    event NFTMinted(address indexed owner, uint256 tokenId);

    function mintNFT(address to) public onlyOwner {
        uint256 tokenId = tokenIdCounter;
        _mint(to, tokenId);
        tokenIdCounter++;
        emit NFTMinted(to, tokenId);
    }
}
