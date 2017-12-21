# Hacking Panda the Bear's Resume

## Part 1

# 1
var profileImg = document.querySelector('img.profile-image');
profileImg.src = 'https://i.pinimg.com/originals/d1/23/d3/d123d32bd3efc97e7e142d06eac0dbe9.jpg';

# 2
var header = document.querySelector('h1.highlight');
header.innerText = "Lena He Bear";

# 3
var title = document.querySelector('#employment .info-title');

title.innerText = 'Experience';

# 4
var body = document.querySelector('body');
body.style.background = '#900C3F';

# 5
var highlights = document.querySelectorAll('.highlight');
highlights.forEach(function(highlight){highlight.style.color='#DAF7A6'});

# 6
var h1 = document.querySelector('h1');
h1.style.fontFamily = 'monospace';

# 7
var roundIcons = document.querySelectorAll('.action-icon-bg');
roundIcons.forEach(function(icon){icon.style.backgroundColor='#E74C3C'});

# 8
var nameField = document.querySelector('input#name');
nameField.placeholder='Identify Yourself';

# 9
var messageField = document.querySelector('textarea#message');
messageField.placeholder='State Your Business';

# 10
nameField.value='your nemesis';

# 11
var emailField = document.querySelector('#email');
emailField.value = "koalathebear@gmail.com";

# 12
var btn = document.querySelector('#submit');
btn.value="En garde!";

# 13
btn.disabled=true;

# 14
var parentInfo = document.querySelector('ul.bio-info');
var childInfo = parentInfo.querySelectorAll('.bio-info-item');
childInfo.forEach(function(li){parentInfo.removeChild(li)});


## Part 2
## Removing Element from DOM
$("#time-travel").parent().remove();

## Adding Elements to the DOM
# 1
var pikapika = document.querySelector('[title="Pikachu"]');
pika = pikapika.cloneNode(true);
element = document.querySelector('.portfolio-container')
element.insertAdjacentElement('beforeend', pika);

# 2
for (var i = 0; i <= 10; i++) {
    element.insertAdjacentElement('beforeend', pikapika.cloneNode(true));
};

# 3
var listItem = document.createElement('li');
var leftSpan = document.createElement('span');
var lastUpdated = document.createTextNode('Page last updated on');
leftSpan.appendChild(lastUpdated);
listItem.appendChild(leftSpan);

var rightSpan = document.createElement('span');
var date = Date();
var dateMessage = document.createTextNode(date)
rightSpan.appendChild(dateMessage);

var ul = document.querySelector('ul.bio-info');
leftSpan.className="bio-info-title";
rightSpan.className="bio-info-value bio-info-phone";

listItem.appendChild(leftSpan);
listItem.appendChild(rightSpan);
ul.appendChild(listItem);
