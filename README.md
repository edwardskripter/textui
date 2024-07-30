# TextUI
The TextUI resource was designed for the RageMP platform, but it can be modified to be used outside the platform.

#Showcase
![image](https://github.com/user-attachments/assets/381cab82-1a15-4706-a03a-616a01fb39f2)

#Usage
Client-side
```javascript
mp.events.call("showTextUI", "E", "Pentru a deschide ATM-ul!");
mp.events.call("hideTextUI");
```

Server-side
```javascript
player.call("showTextUI", [ "E", "Pentru a deschide ATM-ul!" ]);
player.call("hideTextUI");
```

#Example
Client-side
```javascript
const checkProximityToATM = () => {
    const currentPosition = mp.players.local.position;
    const threshold = 3;

    if (isNearATM(currentPosition.x, currentPosition.y, currentPosition.z, threshold)) {
        mp.events.call("showTextUI", "E", "Pentru a deschide ATM-ul!");
    } else {
        mp.events.call("hideTextUI");
    }
};
```
