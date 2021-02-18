# jquery.cookie

<div id="AlertMaterial" class="alert border-bottom alert-dismissible">
    <button type="button" class="close" data-dismiss="alert">&times;</button>
    Материалы выложены<strong> в ознакомительных целях!</strong>
</div>

var delay_popup = 4000;
setTimeout("document.getElementById('AlertMaterial').style.display='block'", delay_popup);

$(function() {
    if ($.cookie('AlertMaterialClose')) {
        document.getElementById("AlertMaterial").remove();
    }
    $.cookie('AlertMaterialClose', true, {
        expires: 1,
        path: '/'

    });
});

#AlertMaterial {
    display: none;
}
