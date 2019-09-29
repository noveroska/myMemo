# myMemo
$('li').click(function() {
  if ($(this).css('color') === 'rgb(128, 128, 128)') {
    $(this).css({
      color: 'black',
      textDecoration: 'none'
    });
  } else {
    $(this).css({
      color: 'gray',
      textDecoration: 'line-through'
    });
  }
});
$('#semangat').append(
  "<audio controls autoplay hidden> <source src='../css/semangat.mp3' type='audio/mpeg' /></audio>"
);
// lengkapi jquery untuk menlist hasil dari todolist yang di inputkan
  function newElement() {

    var li = document.createElement("li");
    var inputValue = document.getElementById("input").value;
    var t = document.createTextNode(inputValue);
    li.appendChild(t);
    if (inputValue === '') {
      alert("You must write something!");
    } else {
      document.getElementById("todos").appendChild(li);
    }
    document.getElementById("input").value = "";
    var span = document.createElement("SPAN");
    span.className = "fa fa-trash";
    li.appendChild(span); 
    $('li').click(function() {
      if ($(this).css('color') === 'rgb(128, 128, 128)') {
        $(this).css({
          color: 'black',
          textDecoration: 'none'
        });
    } else {
       $(this).css({
          color: 'gray',
          textDecoration: 'line-through'
     });
    }
  });
  
} //  code Here...
var close = document.getElementsByClassName("fa fa-trash");
var i;
for (i = 0; i < close.length; i++) {
  close[i].onclick = function() {
    var div = this.parentElement;
    div.style.display = "none";
  }
}

