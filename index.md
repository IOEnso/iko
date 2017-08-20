## Кисонька, АААААА
<div class="text">
    <div class="text-block">Линочка, доброе утро, моё солнышко 🌞</div>
    <div class="text-block">Сейчас мы с тобой поиграем в игру 🐱</div>
    <div class="text-block">Цель игры это узнать что за секрет таится в конце😊 </div>
    <div class="text-block">Только играть ЧЕСТНО 😛</div>
    <div class="text-block"><button>Нажми на меня!😮</button></div>
</div>
<script>
    $(document).ready(function() {
$('.text .text-block').eq(0).addClass('active').fadeIn(1000);
setInterval('AnimTXT();', 4000);
});

function AnimTXT() {
    var length = $('.text .text-block').length - 1;
    $('.text .text-block').each(function(index) {
         if($(this).hasClass('active') && index != length) {
             $(this).removeClass('active').fadeOut(1000).next('.text-block').addClass('active').fadeIn(1000);
             return false;
        } else if (index == length) {
             $(this).removeClass('active').fadeOut(1000);
             $('.text .text-block').eq(0).addClass('active').fadeIn(1000);
             return false;
         }
    });
};
</script>
<style>
    @import url('https://fonts.googleapis.com/css?family=Neucha');
.text {
    text-align: center;
}
.text-block {
    font-family: 'Neucha', cursive;
    font-size: 28px;
    position: absolute;
    display: none;    
}
button {
  font-family: 'Neucha', cursive;
  background: #2db6e9;
  padding: 5px;
  font-size: 18px;
  border: 1px solid #09abe7;
  color: #fff;
  border-radius: 4px;
}
    </style>
