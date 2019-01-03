Part 1: Hacking Panda the Bear's Resume

Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.

let image = document.querySelector('img');
image.src = 'https://placebear.com/200/300';
PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

1. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

let sky = document.querySelector('sky');
image.src = 'https://placebear.com/200/300';

2.Select the heading that says "Panda the Bear" and change it to your own name.

let clouds = document.querySelector('.photography');
clouds.src = 'https://picsum.photos/200/300/?random';

3.Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

document.querySelector('.bio-info-value').innerText = 'Marina';

4.Change the colour of the body.
document.querySelector('.info-title').innerText = 'Panda';

document.getElementsByTagName('body').style.backgroundColor = "red";

5.Change the colour of each element using the highlight class. Use a for loop to do this.
highlight.forEach ( function(element) {
    element.style.color = 'blue' });

6.Change the font family of the h1 to 'monospace'.

document.querySelector('h1').forEach ( function(element) {
    element.style.fontFamily = 'monospace' });

7. Find a way to select the round icons in the sidebar and then change their colour.

document.querySelector('.action-icon-bg').forEach(function(element){
  element.style.color = 'pink'});

8.Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

document.querySelector('#name').placeholder = 'Identify Yourself';

9.Change the placeholder attribute of the message field to "state your business".

document.querySelector('#massage').placeholder = 'state your business';

10.Give the name field a "value" attribute of "your nemesis".

document.querySelector('#name').value = 'your nemesis';

11. Change the value attribute of the email field to "koalathebear@gmail.com".

document.querySelector('#email').value = 'koalathebear@gmail.com';

12.Change the value of the submit button on the contact form to "En garde!".

document.querySelector('#submit').value = 'En garde!';

13. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).
document.querySelector('#submit').disabled = true;

14.We should help Panda protect their privacy by erasing their personal details from the sidebar.

let element = document.querySelector('.bio_info');
element.parentNode.removeChild(element);

Part 2:
Removing Elements from the DOM

1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. Use your googling and docs-skimming skillz to find a function that will allow you to remove elements from the DOM. (hint: there are multiple ways of doing this, but parentNode might be useful when it comes to selecting the right element)

let timeTravel = document.querySelector('#time-travel')
timeTravel.parentNode.remove();

Adding Elements to the DOM:

1. That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().

let Pikachu = document.querySelector('.pikachu')
let clone = pikachu.cloneNode();

2. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

for (i =0;  < 11 ; i++){ var pikachu = document.getElementById('right-image');
var clone = pikachu.cloneNode(true); document.querySelector('.portfolio-container').appendChild(clone) }

3. Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

const listItem = document.createElement('li');
listItem.className = 'bio-info-item';

const leftSpan = document.createElement('span');
leftSpan.className = 'bio-info-title';

var lastUpdated = document.createTextNode('Page last updated on');
leftSpan.appendChild(lastUpdated);
listItem.appendChild(leftSpan);

var rightSpan = document.createElement('span');
rightSpan.className = 'bio-info-value';
rightSpan.classList.add('bio-info-date');

var date = new Date();
var todayDate = document.createTextNode(date);
rightSpan.appendChild(todayDate);
listItem.appendChild(rightSpan);

var bioInfo = document.querySelector('.bio-info');
bioInfo.appendChild(listItem);
