//fixed btn
function FixedAnime() {
	var elemTop = $('#low-trigger').offset().top;
	var scroll = $(window).scrollTop();
	if(scroll <= 20){
	} else if (scroll >= elemTop){
			$('#fixed-btn').addClass('low');
		}else{
			$('#fixed-btn').removeClass('low');
		}
}
//$(window).scroll(function () {
//	FixedAnime();
//});
//smooth
jQuery(function(){
	jQuery('a[href^="#"]').click(function(){
	  var speed = 500;
	  var href= jQuery(this).attr("href");
	  var target = jQuery(href == "#" || href == "" ? 'html' : href);
	  var position = target.offset().top;
	  jQuery("html, body").animate({scrollTop:position}, speed, "swing");
	  return false;
	});
});

document.addEventListener("DOMContentLoaded", function() {
  const fadeUpSelectors = [
    '.solution .cnt .tr-list',
    '.voice .vc-list'
  ];

  const headingSelectors = [
    '.point.sec .heading > p',
    '.point.sec .heading > h2.srf.fs30'
  ];

  const observer = new IntersectionObserver(handleIntersection, {
    rootMargin: "0px 0px -20% 0px"
  });

  fadeUpSelectors.forEach((selector) => {
    document.querySelectorAll(selector).forEach((element) => {
      observer.observe(element);
    });
  });

  headingSelectors.forEach((selector) => {
    document.querySelectorAll(selector).forEach((element) => {
      observer.observe(element);
    });
  });

  function handleIntersection(entries) {
    entries.forEach((entry) => {
      if (!entry.isIntersecting) {
        return;
      }

      if (entry.target.classList.contains('tr-list') || entry.target.classList.contains('vc-list')) {
        animateList(entry.target);
      } else {
        entry.target.classList.add('is-active');
      }

      observer.unobserve(entry.target);
    });
  }

  function animateList(list) {
    list.querySelectorAll('li').forEach((item) => {
      item.classList.add('is-active');
    });
  }
});
