# create header footer dompdf
create header footer everypage
```
.footer {position: fixed; bottom: 0px; border-top: 1px solid #000;}
.header {font-size: 10.5px;position: fixed; top: -20px; border-bottom: 1px solid #000;overflow: hidden;}

<div class="header">
  <p>header</p>
</div>

<div class="footer">
  <p>footer</p>
</div>
```

create different header or footer
```
// CREATE DIFFERENT FOOTER OR HEADER IN DOMPDF
<?php
$canvas = $dompdf->get_canvas();
$canvas->page_script('
/*Logic what D U WANT*/
if ($PAGE_NUM % 2 == 0) {
    $current_page = $PAGE_NUM;
    $total_pages = $PAGE_COUNT;
    /*setting ur position $pdf->text(position,position,content,type font, font size, etc)*/
    $pdf->text(35, 17, "$current_page / $total_pages", "arial", 9, array(0,0,0));
}
');
?>
```
