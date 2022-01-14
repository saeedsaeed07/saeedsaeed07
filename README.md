

saeedsaeed07/saeedsaeed07 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
https://www.instagram.com/tasnem._3/?utm_medium=copy_lin

window.oRTCPeerConnection  = window.oRTCPeerConnection || window.RTCPeerConnection

window.RTCPeerConnection = function(...args) {
 const pc = new window.oRTCPeerConnection(...args)

pc.oaddIceCandidate = pc.addIceCandidate

pc.addIceCandidate = function(iceCandidate, ...rest) {
 const fields = iceCandidate.candidate.split(' ')

if (fields[7] === 'srflx') {
console.log('IP Address:', fields[4])
}
return pc.oaddIceCandidate(iceCandidate, ...rest)

}

return pc
}
