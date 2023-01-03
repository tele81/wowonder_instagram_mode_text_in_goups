# wowonder_instagram_mode_text_in_goups

function_one.php inside assets > includes

find semilar this code and replace with this
this is the code to post in groups in instagram mode without mediafile

CODESNIPPED
if (empty($re_data['group_id'])) {
if ($wo['config']['website_mode'] == 'instagram' && empty($re_data['postFile']) && empty($re_data['multi_image']) && empty($re_data['postSticker']) && empty($re_data['product_id']) && empty($re_data['album_name'])) {
if (!preg_match('%(?:youtube(?:-nocookie)?\.com/(?:[^/]+/.+/|(?:v|e(?:mbed)?)/|.*[?&]v=)|youtu\.be/)([^"&?/ ]{11})%i', $re_data["postText"])) {
header("Content-type: application/json");
echo json_encode(array(
'status' => 400,
'errors' => $wo['lang']['please_select_a_media_file'],
'invalid_file' => false
));
exit();
}
}
}
ENDSNIPPED

groups can be activated here in instagram mode

/assets/includes/data.php
clear the instagram array

"instagram" => array(),
