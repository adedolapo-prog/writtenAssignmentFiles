Create an array with three elements - second element should be a function

const tradingCenters = [
{
name: "New York Center",
location: "USA",
tradeStrength: 30,
},

tradingVolume = () => {
let numberOfContracts = 30;
let numberOfTraders = 12;
const volume = numberOfContracts \* numberOfTraders;
console.log(volume);
return volume;
},

{
name: "London Center",
location: "UK",
tradeStrength: 25,
}
]

tradingCenters.forEach((center) => {
let objectValue = Object.values(center);
let secondValue = objectValue[1];
console.log(secondValue);
});

console.log(tradingVolume())

# Explain the difference between the two blocks of code

There is basically no difference between the two blocks of code as they do the same thing.
