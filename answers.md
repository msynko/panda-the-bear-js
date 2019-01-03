
let image = document.querySelector('img');
image.src = 'https://placebear.com/200/300';

let sky = document.querySelector('sky');
image.src = 'https://placebear.com/200/300';

let clouds = document.querySelector('.photography');
clouds.src = 'https://picsum.photos/200/300/?random';

document.querySelector('.bio-info-value').innerText = 'Marina';

document.querySelector('.info-title').innerText = 'Panda';

document.getElementsByTagName('body').style.backgroundColor = "red";

highlight.forEach ( function(element) {
    element.style.color = 'blue' });

document.querySelector('h1').forEach ( function(element) {
    element.style.fontFamily = 'monospace' });

document.querySelector('.action-icon-bg').forEach(function(element){
  element.style.color = 'pink'});

document.querySelector('#name').placeholder = 'Identify Yourself';

document.querySelector('#massage').placeholder = 'state your business';

document.querySelector('#name').value = 'your nemesis';

document.querySelector('#email').value = 'koalathebear@gmail.com';

document.querySelector('#submit').value = 'En garde!';

document.querySelector('#submit').disabled = true;

let element = document.querySelector('.bio_info');
element.parentNode.removeChild(element);
