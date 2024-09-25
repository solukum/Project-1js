// create a variable to hold your NFT's

const NFTS = [];

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT (name, hairColor, clothType, bling) {
    const NFT = {
        "name": name,
        "hairColor": hairColor,
        "clothType": clothType,
        "bling":bling
    }
    NFTS.push(NFT);
    console.log("Minted: " + name);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs () {
    for(let i=0; i < NFTS.length; i++) { 
        console.log("\nID: \t\t" + (i + 1)); 
        console.log("Name: \t\t" + NFTS[i].name); 
        console.log("Eye : \t" + NFTS[i].hairColor); 
        console.log("Cloth Type: " + NFTS[i].clothType);
        console.log("Bling \t\t" + NFTS[i].bling);
    }
}


// print the total number of NFTs we have minted to the console
function getTotalSupply() {
    console.log("\n" + NFTS.length);
}


// call your functions below this line
mintNFT("ved prakash", "Blue", "Hoodie", "Gold Chain"); 
mintNFT("shreya", "Black", "Sweatshirt", "Diamond Chain"); 
mintNFT("shristi", "Red", "Jacket",    "Platinium Chain"); 
mintNFT("khushi", "Yellow", "Bomber jacket", " Silver Chain"); 

listNFTs();

getTotalSupply();
