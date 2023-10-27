---
tags: cs-s
---

> Мои настройки для игры [[0006 Game/Counter-Strike Source]]

// Конфигурационный файл для удобной и приятный игры
unbindall

// Alias
bind "MOUSE3" "drop"
bind "g" "use weapon_c4; drop"

// Pistol Drop
alias "+pistoldrop" "slot2; wait; wait; wait; drop"
bind "." "+pistoldrop"

// Guns Drop
alias "+gunsdrop" "slot1; wait; wait; wait; wait; wait; wait; wait; drop"
bind "," "+gunsdrop"

// JumpThrow
alias "+jumpthrow" "+jump;-attack"
alias "-jumpthrow" "-jump"
bind "ALT" "+jumpthrow"

// Duck Jump
alias "+djump" "+jump; +duck"
alias "-djump" "-jump; -duck"
bind "SPACE" "+djump"

// Knife Run
alias "+knife" "use weapon_knife"
alias "-knife" "slot2; wait; wait; wait; slot1"
bind "MOUSE5" "+knife"

// Shok Fire
alias "+shokefire" "+attack"
alias "-shokefire" "-attack"
bind "MOUSE1" "+shokefire"

// Aim
//cl_crosshairalpha "255"
//cl_crosshaircolor "5"
//cl_crosshaircolor_b "255"
//cl_crosshaircolor_r "0"
//cl_crosshaircolor_g "255"
//cl_crosshairdot "0"
//cl_crosshairsize "0.9"
//cl_crosshairusealpha "1"
//cl_crosshairthickness "1"
//cl_dynamiccrosshair "1"

// Binds
// Slots
bind "0" "slot10"
bind "1" "slot1"
bind "2" "slot2"
bind "3" "slot3"
bind "" "slot4"
bind "5" "slot5"
bind "6" "slot6"
bind "7" "slot7"
bind "8" "slot8"
bind "9" "slot9"

// Move
bind "a" "+moveleft"
bind "d" "+moveright"
bind "s" "+back"
bind "w" "+forward"
bind "SHIFT" "+speed"
bind "c" "+duck; +use"
bind "e" "+use; r_cleardecals"
bind "r" "+reload; r_cleardecals"
bind "q" "lastinv"
bind "m" "chooseteam"
bind "MOUSE2" "+attack2"

// Buy
bind "b" "buymenu"
bind "v" "buyequip"
bind "F1" "autobuy"
bind "F2" "rebuy"

// Message
bind "y" "messagemode"  
bind "u" "messagemode2"
bind "g" "say !guns; say guns"
bind "o" "say !rs"
//bind "BACKSPACE" "+voicerecord"

// Other bind
bind "`" "toggleconsole"
bind "TAB" "+showscores"
bind "ESCAPE" "cancelselect"
bind "CAPSLOCK" "toggle cl_righthand 1 0"
bind "F4" "kill"

// Use grenade
bind "MOUSE4" "use weapon_flashbang"
bind "4" "use weapon_hegrenade"
bind "f" "use weapone_smokegrenade"


bind "MOUSE4" "use weapon_flashbang"
bind "g" "use weapon_smokegrenade"
bind "t" "use weapon_hegrenade"

// Buy guns & equipment
bind "kp_ins" "buy hegrenade;buy smokegrenade;buy flashbang;buy flashbang;buy vesthelm; buy vest;buy vest;buy defuser;"
bind "kp_del" "buy vesthelm; buy vest;buy vest;"
bind "kp_end" "buy ak47; buy m4a1;"
bind "kp_downarrow" "buy famas; buy galil;"
bind "kp_pgdn" "buy awp;"
bind "kp_leftarrow" "buy p90;"
bind "kp_rightarrow" "buy scout ;"
bind "kp_home" "buy deagle"
bind "kp_uparrow" "buy p228;"
bind "kp_pgup" "buy fiveseven"
bind "kp_5" "buy mp5navy;"
bind "kp_slash" "buy smokegrenade;"
bind "kp_multiply" "buy flashbang;buy flashbang;"
bind "kp_minus" "buy hegrenade;"

// Radar
cl_radar_locked 0 // (где Х — либо 0, либо 1) — выключает или включает фиксацию угла радара;
cl_radaralpha 255 // (где Х — число от 0 до 255) — регулирует прозрачность радара (невидимый при 0 и непрозрачный при 255);
drawradar — отображает радар;
// hideradar // скрывает радар;
overview_alpha 1 // (где Х — либо 0, либо 0.5, либо 1) — регулирует прозрачность карты на радаре (невидимая, прозрачная и непрозрачная соответственно);
overview_health 1 // (где Х — либо 0, либо 1) — выключает или включает отображение здоровья игроков на карте;
overview_locked 1 // (где Х — либо 0, либо 1) — выключает или включает фиксацию угла карты, чтобы она не крутилась при повороте камеры;
overview_names 1 // (где Х — либо 0, либо 1) — выключает или включает отображение имён игроков на карте;
overview_preferred_mode 1 // (где Х — либо 0, либо 1, либо 2) — задаёт стандартное отображение карты в режиме зрителя (карты нет, мини-карта, полная карта);
overview_tracks 0 // (где Х — либо 0, либо 1) — выключает или включает отображение следов игроков на карте.

clear

cl_crosshairalpha "255"; // Прозрачность
cl_crosshaircolor "4"; // Цвет прицела
cl_crosshaircolor_b "50"; // Оттенок синего
cl_crosshaircolor_r "50"; // Оттенок красного
cl_crosshaircolor_g "250"; // Оттенок зелёного
cl_crosshairdot "1"; // Отображение точки
cl_crosshairsize "0.9"; // Размер прицела
cl_crosshairusealpha "1"; // 0 = Вкл / 1 = Выкл прозрачности прицела
cl_crosshairthickness "1"; // Тольщина прицела

snd_mute_losefocus "0" // Отключаем звуки игры при сворочивании
cl_minmodels "1"
bind "z" "say !voice"
bind "ctrl" "+duck"
bind "F12" "hud_reloadscheme"

//server
mp_freezetime "0"
mp_buytime "9"



echo ======== Binds ==============
echo Mouse4 - Use Flash
echo T - Use HeGrenade
echo G - Use Smoke
echo . - Drop Pistol
echo , - Drop Guns
echo Mouse3 - Drop Bomb
echo Alt - Jump Throw
echo Space - Duck Jump
echo Mouse5 - Knife Run
echo Mouse1 - Shok Fire
echo R - Clear Blood
echo F - Guns
echo O - Reset Score   


[[0006 Game/config]]
