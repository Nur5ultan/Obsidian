NETWORK
rate - Количество байтов, которые клиент может получить от сервера за секунду.
cl_cmdrate - Количество пакетов, которые клиент может отослать серверу.
cl_interp - Временной промежуток, через который происходит интерполяция (0,05 = 50 мс).
cl_lagcomp_errorcheck - Проверяет ошибки позиции игрока.
cl_lagcompensation - Производит компенсацию лагов на стороне сервера.
cl_updaterate - Количество пакетов, которые клиент может получить от сервера.
cl_smooth - Сглаживание ошибок прогнозирования. (default "1")
cl_smoothtime - Время, нужное для сглаживания ошибок прогнозирования. (default "0.1")
cl_interp_threadmodeticks - Дополнительная интерполяция
cl_pred_optimize - Оптимизация для не копирования данных если не было обновление сети (1), а также для не переадресации если не было ошибок (2).
cl_interp_ratio - Число промежутков между "интерполированием" мира. (default "2.0")
MAT
mat_queue_mode - Количество ядер процессора задействованных для игры. (default " - 2")
mat_mipmaptextures - Изменение качества текстур с расстоянием. (default "1")
mat_picmip - Изменение качества текстур. (default "0")
mat_antialias - Сглаживание.
mat_bumpmap - Бампмэппинг (бампмэппинг позволяет показывать плоские текстуры, объемными). (default "1")
mat_bufferprimitives - Кэширование "примитивов".
mat_clipz - (0) Ликвидирует проблемы с DirectX9 у некоторых видеокарт nVidia.
mat_colorcorrection - Цветокоррекция.
mat_specular - Отключает \ Включает блестящий убер.
mat_compressedtextures - Сжатие текстур.
mat_motion_blur_forward_enabled - Размытие при движении.
mat_disable_bloom - Спреи. (default "0")
mat_monitorgamma - Гамма. (default "2.2")
mat_forceaniso - Анизотропная фильтрация. (default "1")
mat_hdr_enabled - Эффект подстраивания видимости при переходе из областей с разным уровнем освещенности.
mat_hdr_level - Эффект динамического освещения. (default "2")
mat_shadowstate - Относится к теням (Работает только с r_shadows). (default "1")
mat_use_compressed_hdr_textures - Сжатие текстур, используемых с HDR.
mat_trilinear - Трёхлинейное фильтрование.
mat_dxlevel - Устанавливает версию DirectX.
mat_wateroverlaysize - Устанавливает разрешение искажения воды. (default "128")
mat_aaquality - Качество сглаживания. Работает совместно с mat_antialias.
mat_reducefillrate - Регулировка детализации текстур. (default "0")
mat_autoexposure_max - Максимальная яркость экрана. (default "2")
mat_texture_list - Для режима отладки, показывает список текстур используемых во фрейме.
mat_texture_list_all - Если значение этой команды отлично от нуля, то панель списка текстур будет показывать все загруженные в настоящий момент текстуры.
mat_texture_list_view - Если значение этой команды отлично от нуля, то панель списка текстур будет отображать иконки загруженных в настоящих момент текстур.
mat_texture_list_txlod - Регулирует степень детализации последней просмотреннmat_autoexposure_min - Минимальная яркость экрана. (default "0.5")
mat_bloomscale - BLOOM эффект. (default "1")
mat_disable_lightwarp - Точное описание не известно, но относится к 1D текстурам как затенение. (default "0")
mat_envmapsize - История изображений в недостижимых разделах карты, таких, как SkyBox. (default "128")
mat_envmaptgasize - Не известно, но скорей всего отвечает за размер SkyBox. (default "32.0")
mat_fastspecular - Алгоритм отрисовки гладких поверхностей.
mat_fastnobump - Алгоритм отрисовки объемных текстур.
mat_forcemanagedtextureintohardware - Очищение текстур в видеопамяти. (default "1")
mat_diffuse - Устанавливая значение "0", всё становится чёрным.
mat_software_aa_strength - Производит программный А - А пост процесс (альтернативно/дополнительно к МСАА). (default " - 1.0")
mat_software_aa_tap_offset - По умолчанию 1.0 - меньшее значение, сделает изображение более четкое, значение выше сделает его размытым.
mat_software_aa_quality - Качество программного сглаживания: (0 - 5 - tap filter), (1 - 9 - tap filter).
mat_software_aa_edge_threshold - Software AA – регулирует чувствительность обнаружения краев шейдеров у программного сглаживания – меньшее значение сгладит больше краев, большее значение сгладит меньше. (default "1.0")
mat_software_aa_blur_one_pixel_lines - Как много программного сглаживания требуется, чтобы сгладить линию толщиной в один пиксель (0.0 – не требуется), (1.0 - много) (default "0.5")
mat_software_aa_debug - Software AA - Регулирует смещение сигналов, используемых шейдером программного сглаживания – меньшее значение сделает картинку чётче, большее сделает её более размытой. (default "1.0")
mat_filterlightmaps - Фильтр освещения. (default "1")
mat_filtertextures - Фильтр текстур. (default "1")
mat_vsync - Вертикальная синхронизация.
mat_bloom_scalefactor_scalar - Регулировка интенсивности Bloom эффекта.
mat_forcehardwaresync - Работает вместе с VSync, позволяет увеличить частоту кадров, если это возможно.
mat_showlowresimage - Устанавливая "1", полностью уродуются текстуры, прирост фпс на слабых компьютерах большой, но он того не стоит. (default "0")
mat_showwatertextures - Уменьшает текстуры воды (чтобы уменьшить влияние GPU на процессор) (default "128")
mat_drawTextureScale - Включает вид сглаживания текстур.
mat_debug_postprocessing_effects// 0=выкл; 1=показывает пост процессинговые алгоритмы в квадрантах экрана; 2=показывает постпроцессинг в центре экрана.
mat_postprocessing_combine - Объединяет блюм, программное сглаживание и цветокоррекцию в один пост процессинговый алгоритм.
mat_tonemap_min_avglum - Software AA – производит программный пост - процесс сглаживания. Значение команды устанавливает жесткость эффекта. (0.0 – выкл.), (1.0 – макс.) (default " - 1.0")
ой текстуры (+1 – увеличить разрешение, - 1 – уменьшить разрешение)
mat_colcorrection_disableentities// Отключает "энтити" цветокоррекции на карте.
mat_configcurrent - Отображает конфигурацию текущей контрольной панели видео для текстурного маппинга.
mat_savechanges - Сохраняет текущую конфигурацию видео в реестре.
mat_max_worldmesh_vertices - Удерживает текстуры от вытягивания. (default "65536")
mat_drawTitleSafe - Включает видимый оверлей.
mat_supportflashlight - 0 – не поддерживает вспышки (не загружает комбинации шейдера для вспышек), 1 – вспышки поддерживаются (default " - 1”)
mat_showmaterials - Отображает инструменты.
mat_showmaterialsverbose - Отображает инструменты №2.
CL
cl_detaildist - Определяет диапазон, в которых подробно указаны реквизиты (например, трава). (default "1200")
cl_detailfade - Определяет дистанцию, на которой реквизиты начинают исчезать. (default "400")
cl_drawmonitors - Рендеринг внутриигровых "мониторов" которые включают зарендеренные 3D картинки. (default "1")
cl_ejectbrass - Отображение гильз. (default "1")
cl_forcepreload - Загрузка информации о текстурах и моделях в начале карты. (default "0")
cl_muzzleflash_dlight_1st - Динамический свет 1го порядка от вспышек выстрелов. (default "1")
cl_phys_props_max - Количество одновременно рассчитываемых мелких предметов. (default "300")
cl_phys_props_enable - Отключает \ Включает физику мелких объектов.
cl_ragdoll_collide - Просчет пересекающихся трупов.
cl_ragdoll_fade_time - Время исчезновения трупов. (default "15")
cl_ragdoll_physics_enable - Прорисовка трупов.
cl_showhelp - Помощь на экране. (default "1")
cl_show_splashes - Брызги воды. (default "1")
cl_rumblescale - Шкала чувствительности Rumble эффекта. (default "1.0")
cl_threaded_bone_setup - Параллельная обработка "C_BaseAnimating".
cl_new_impact_effects - Пыль, песок и другие погодные эффекты.
cl_burninggibs - Устанавливая "1", огонь от взрыва будет поджигать не только игроков, но и останки тел.
cl_clearhinthistory - Очищает память подсказок на стороне клиента.
cl_predictweapons - Производит прогнозирование эффектов оружия на стороне клиента.
cl_predict - Производит прогнозирование движений игрока на стороне клиента.
cl_showpluginmessages - Позволяет плагинам показывать вам сообщения. (default "1")
cl_debugrumble - Отключает \ Включает "Rumble" отладки.
cl_autoreload - Автоматическая перезарядка.
cl_hud_minmode - Установите "1", чтобы включить отображение худа в маленьком режиме.
cl_showhelp - Показывает меню помощи.
cl_showfps - Показывает фпс.
cl_autorezoom - Автоматическое возвращение зума, при стрельбе снайпером.
cl_rumblescale - Устанавливает чувствительность шумовых эффектов.
cl_debugrumble - Включает отладку шумовых эффектов.
cl_team - Выбор команды по умолчанию при подключении к игре.
cl_class - Выбор класса по умолчанию при подключении к игре.
cl_chatfilters - Содержит настройки фильтров чата.
cl_mouselook - Установите значение 1, чтобы оглядываться при помощи мыши, 0 – при помощи клавиатуры. Нельзя сменить, находясь на сервере.
cl_spec_mode - Режим спектатора.
cl_soundfile - Файл звука звона.
cl_allowdownload - Клиент скачивает "кастомные" файлы.
cl_timeout - Через сколько секунд не получая пакетов от сервера, клиент отсоеденится от сервера.
cl_allowupload - Клиент загружает "кастомные" файлы.
cl_downloadfilter - Определяет, какие файлы могут быть загружены с сервера (all, none, nosounds).
cl_logofile - Указать файл спрея для использования на серверах.
CC
cc_linger_time - Время задержки субтитров.
cc_predisplay_time - Задержка перед отображением субтитров.
cc_subtitles - Если включено, то звуковые эффекты не будут отображаться в субтитрах, только речь(например, не будут отображаться звуки ранения игрока).
cc_lang - Язык субтитров (по умолчанию – язык пользовательского интерфейса).
CAM
cam_ideallag - Задержка, при нахождении идеального угла обзора, при просмотре от третьего лица.
cam_idealdelta - Скорость движения камеры, при нахождении идеального угла обзора, при просмотре от третьего лица.
cam_collision - Если значение этой команды равно 1, то при просмотре от третьего лица, камера будет избегать прохождения через стены.
VOICE
voice_forcemicrecord - Запись микрофона. (default "1")
voice_enable - Голосовой чат. (default "1")
voice_scale - Уровень звука.
voice_modenable - Голосовой чат в моде. (default "1")
snd_mixahead - Размер звукового буфера.
snd_musicvolume - Громкость музыки.
dsp_enhance_stereo - Эффект расширения стереобазы.
dsp_volume - 0 - Без звука, 1 - Есть звук. (default "1.0")
dsp_slow_cpu - Выставив 1, снижается качество звуковых эффектов DSP, но повышается производительность. (default "0")
dsp_spatial - Громкость пространства.
dsp_speaker - Громкость разговоров через микрофон.
dsp_water - Громкость воды.
volume - Звук в игре.
GIBS
violence_agibs - Чужие лица. (default "1")
violence_hgibs - Человеческие лица. (default "1")
violence_hblood - Человеческая кровь. (default "1")
violence_ablood - Чужая кровь. (default "1")
R
r_drawflecks - Прорисовка мелких осколков и пыли, вокруг точки вхождения пули. (default "1")
r_decals - Временной отрезок, на время которого "деколы" будут видны. (default "2048")
r_dynamic - Динамические отсветы от объектов. (default "1")
r_drawmodeldecals - "Деколы" на моделях игроков. (default "1")
r_fastzreject - Ускорение алгоритма просчета "перспективы", если поддерживается видеоускорителем. (default "0")
r_lod - Степень детализации объектов и текстур. (default " - 1")
r_rootlod - Детализация моделей.
r_renderoverlayfragment - Отключает \ Включает наложенные на текстуры объекты (плакаты на стенах и т.д.). (default "1")
r_waterdrawreflection - Отражения на воде. (default "1")
r_waterforceexpensive - Отключает \ Включает сложную графику для воды.
r_shadowrendertotexture - Динамические тени на объектах.
r_drawdetailprops - Отключает \ Включает детализацию мелких предметов. (default "1")
r_shadows - Динамические тени (от объектов и моделей) на местности. (default "1")
r_propsmaxdist - Максимальное расстояние отрисовки мелких предметов. (бутылки, осколки).
r_lightinterp - Интерполяция света.
r_occlusion - Использование "occlusion" системы Source Engine.
r_3dsky - 3D фон (например здания). (default "1")
r_decal_cullsize - Расстояние, на котором видны пулевые отверстия. Более высокое число = более короткая дистанция. (default "5")
r_lightaverage - Усреднение света. (default "1")
r_spray_lifetime - Сколько раундов будут видны спреи игроков. (default "2")
r_shadowmaxrendered - Макс. количество показываемых теней. (default "32")
r_maxdlights - Максимальное количество динамических огней, видимых на экране. (default "32")
r_flashlightdepthtexture - Глубина освещения текстур, 1 - Высокое, 0 - Низкое. (default "1")
r_shadowrendertotexture - Прорисовка теней.
r_ropetranslucent - Прозрачность канатов. (default "1")
r_drawbatchdecals - "Render деколи" в пакетном режиме. (default "1")
r_ForceWaterLeaf - Качество обзора находясь под водой. (default "1")
r_cheapwaterend - Прорисовка воды и дна. (default "800")
r_waterforcereflectentities - Отражения в воде.
r_maxmodeldecal - Максимальное количество "декалей", которые могут быть сделаны на модель. (default "50")
r_eyes - Глаза. ( default "1" )
r_sse2 - Отключает \ Включает SSE2 код.
r_3dnow - Отключает \ Включает 3DNow код.
r_teeth - Зубы. (default "1")
r_queued_decals - Немного разгружает работу декал рендеринг установок.
r_decalstaticprops - Статическая термоаппликация. (default "1")
r_ambientboost - Ускорение окружающих условий. ( default "1" )
r_worldlights - Количество свечений мира, "vertex". (default "4")
r_radiosity - Освещение оружия и рук. (default "4")
r_drawviewmodel - Отключает \ Включает модельку оружия.
r_lightcache_zbuffercache - Освещение моделек в тени.
r_flex - Анимация лиц
r_dopixelvisibility - Отключает \ Включает "чёрточки" на источниках освещения.
r_unloadlightmaps - Перезагружает текстуры и освещения. Может помочь после alt+tab (сворачивания), когда появляются розовые текстуры.
r_visambient - Рисует примеры листового освещения окружающей среды.
r_cleardecals - Использование: r_cleardecals <постоянная>
r_flushlod - Снимает и перезагружает ЛОДы
r_proplightingfromdisk - 0=выкл 1=вкл 2=Показывает ошибки
r_ambientboost - Выставляет ускорение окружающих условий, если они полностью загружены местным освещением. ( default "1" )
r_ambientmin - Порог, выше которого куб окружающей среды не ускорится ( default "0.3" )
r_ambientfactor - Ускоряет куб окружающей среды на велечину не более указанного значения. ( default "5" )
r_occludermincount - Примерно столько преград должно быть использовано.
MOUSE
m_pitch - Устанавливает множитель чувствительности скорости движения вверх/вниз у мыши.
m_filter - Режим фильтрации (сглаживания) мыши.
m_side - Устанавливает множитель чувствительности скорости перемещения у мыши.
m_yaw - Устанавливает множитель чувствительности скорости поворотов влево - вправо.
m_forward - Устанавливает множитель чуствительности скорости движения вперед мыши.
m_mouseaccel1 - Windows ускорение мышки, первоначальный порог (2x движения).
m_mouseaccel2 - Windows ускорение мышки, средний порог (4x движения).
m_customaccel - Пользовательское ускорение мыши (акселерация).
m_customaccel_exponent - Измерение коэффициента пропорциональности акселерации.
m_customaccel_max - Максимальный коэффициент пропорциональности акселерации.
m_customaccel_scale - Пользовательское значение акселерации мышки.
m_rawinput - переменная, принимающая значение 0 или 1. Дает возможность использовать устройство ввода (мышь) в обход настроек ОС,
CROSSHAIR
cl_crosshair_red - Красный цвет. (default "200")
cl_crosshair_green - Зелёный цвет. (default "200")
cl_crosshair_blue - Синий цвет. (default "200")
cl_crosshair_scale - Размер. (default "32.0" )
cl_crosshair_file - Название прицела. (default "0")
HUD
hud_classautokill - После выбора нового класса, вы автоматически умираете.
hud_reloadscheme - Перезагружает "hudlayout" (Позволяет настраивать худ, не выходя из игры).
hud_deathnotice_time - Сколько времени будут показываться убийства.
hud_saytext_time - Сколько времени будут показываться сообщения в чате.
hud_fastswitch - Быстрое переключение оружия.
hud_takesshots - Авто скриншот "tab" в конце карты.
hud_achievement_description - Показать полное описание достижений.
hud_achievement_glowtime - Продолжительность свечения вокруг достижения.
hud_achievement_count - Максимальное кол - во достижений, которые могут быть показаны на экране.
hud_achievement_tracker - Скрывать \ показывать путь выполнения достижения.
hud_escort_test_speed - Как долго будет отображаться панель уведомления.
hud_combattext - Показывает урон при попадание.
hud_medicautocallers - Автоматический вызов медика, отображающий товарищей с заданным здоровьем.
hud_medicautocallersthreshold - Количество здоровья, при которых срабатывает вызов медика.
hud_medichealtargetmarker - Маркер лечения, который лучше выделяет лечимую вами цель.
NET_GRAPH
net_graph - Включает net_graph, 1 - 3.
net_graphtext - Скрывает net_graph.
net_graphheight - Высота net_graph панели. (default "64")
net_graphshowlatency - Рисует пинг и потери пакетов
net_graphshowinterp - Рисует интерполяцию
net_graphpos - Место положение net_graphа. (default "1")
net_graphproportionalfont - Размер net_graphа.
MP
mp_decals - Cколько следов от пуль, будет оставаться на стенах. (default "200")
mp_usehwmmodels - Отключает \ Включает модели используемые в Meet The видео. (default "0")
mp_usehwmvcds - Отключает \ Включает анимацию используемую в Meet The видео. (default "0")
ROPE
rope_smooth - Сглаживание отрисовки проводов. (default "1")
rope_shake - Отключает \ Включает раскачивание проводов.
rope_wind_dist - Влияние ветра на провода. (default "1000")
rope_subdiv - Количество звений проводов. (default "2")
rope_averagelight - Среднее cubemap освещение. (default "1")
rope_collide - Сталкивает провода с миром. (default "1")
rope_smooth_enlarge - Количество канатов в пространстве экрана. (default "1.4")
OVERVIEW
overview_health - Отображает здоровье игрока при обзоре карты.
overview_names - Отображает имена игроков при обзоре карты.
overview_tracks - Отображает пути игроков при обзоре карты.
overview_locked - Закрепляет угол обзора.
overview_alpha - Прозрачность карты при обзоре.
overview_mode - Обзор режима набора карт.
TF
tf_dingalingaling - Отключает \ Включает звук при попадание.
tf_dingaling_volume - Громкость попадания.
tf_dingaling_pitchmindmg - Устанавливает желаемый тон звука слабого попадания.
tf_dingaling_pitchmaxdmg - Устанавливает желаемый тон звука сильного попадания.
tf_dingaling_wav_override - Можно использовать любой другой звук попадания, залив его в папку "sounds" и указав полное название файла.
tf_hud_num_building_alert_beeps - Количество проигрывания предупреждающего сигнала перед тем, как новое предупреждение отобразится на объектах в строительном дисплее инженера.
tf_build_menu_controller_mode - Использовать консольные меню постройки объектов. 1 = вкл, 0 = выкл.
tf_disguise_menu_controller_mode - Использовать консольные меню маскировки. 1 = вкл, 0 = выкл.
tf_weapon_select_demo_start_delay - Задержка между респауном и доставанием оружия.
tf_weapon_select_demo_time - Время, чтобы достать оружие. 0=выкл.
JOYSTICK
joy_response_move - Режим отклика джойстика для передвижения: 0=линейный, 1=квадратный, 2=кубический, 3=quadratic extreme, 4=power function
joy_response_look - Режим отклика джойстика для взгляда: 0=По умолчанию, 1=Акселерация
joy_autoaimdampenrange - Дальность положения джойстика, при которой ослабляется авто - аим. 0=Выкл.
joy_diagonalpov - Манипулятор POV воздействует на диагональные "топоры".
joy_inverty - Инвертировать ли Ось Y джойстика для обзора.
joy_xcontroller_cfg_loaded - Если 0, файл 360controller.cfg будет загружен на изменениях выбора и параметров запуска.
joy_axisbutton_threshold - Аналоговый диапазон оси перед нажатием кнопки зарегистрирован.
joy_advanced - Необходима в joystick.cfg перед установкой клавиш, чувствительности и порога.
joy_advaxisr - Ось R: обычно, это ось вращения (поворота).
joy_advaxisu - Ось U.
joy_advaxisv - Ось V.
joy_advaxisx - Ось X: обычно, это главная X - ось контроллера.
joy_advaxisy - Ось Y: обычно, это главная Y - ось контроллера.
joy_advaxisz - Ось Z: обычно, это главная Z - ось или дроссель контроллера.
joy_autoaimdampen - Определяет, как будет измеряться ход стика, когда оружие направлено на действительную цель.
joy_autosprint - Автоматический спринт при передвижении с помощью аналогового джойстика.
joy_display_input - Записывать информацию джойстика в лог консоли.
joy_forwardsensitivity - Определяет количество движения джойстика для максимальной скорости передвижения вперед и назад.
joy_forwardthreshold - Определяет "мертвую зону" для перемещения вперед и назад.
joy_lowend - Определяет величину физического диапазона контроллера, который Вы хотите исключить как "внутреннюю зону".
joy_lowmap - Определяет величину действительного диапазона контроллера, сопоставленную "внутренней зоне".
joy_name - Название вашего джойстика.
joy_pitchsensitivity - Определяет скорость или коэффициент, используемый при обзоре вверх и вниз.
joy_pitchthreshold - Определяет "мертвую зону" для обзора вверх и вниз.
joy_response_look - Режим ответа обзорного стика: 0 - линейный; 1 - квадратный; 2 - кубический; 3 - квадратный экстремальный; 4 - другой.
joy_response_move - Режим ответа стика передвижения: 0 - линейный; 1 - квадратный; 2 - кубический; 3 - квадратный экстремальный; 4 - другой.
joy_sidesensitivity - Определяет величину передвижения джойстика, необходимую для максимальной скорости передвижения из стороны в сторону.
joy_sidethreshold - Определяет "мертвую зону" для передвижения из стороны в сторону.
joy_wingmanwarrior_centerhack - Исправляет проблему центрирования с джойстиком Wingman Warrior.
joy_wingmanwarrior_turnhack - Исправляет проблему вращения с джойстиком Wingman Warrior.
joy_yawsensitivity - Определяет скорость или коэффициент, используемый при обзоре влево или вправо.
joy_yawthreshold - Определяет "мертвую зону" для обзора влево или вправо.
joyadvancedupdate - Обновляет текущие настройки джойстика.
joystick - Выключает / включает джойстик.
Параметры запуска
-heapsize // Выставить число, в зависимости от размера оперативной памяти.
512 => 262144
1024 => 524288
2048 => 1048576
3072 => 1572864
4096 => 2097152
-nojoy // Отключает джостик.
-noipx // Не загружает IPX соединений, кроме памяти.
-novid // Отключает вступительный ролик.
-noborder // Убирает рамку окна при запуске в оконном режиме.
-noforcemspd // Использование скорости мышки из настроек windows.
-noforcemparms // Использование кнопок мышки из настроек windows.
-noforcemaccel // Использование акселерации мышки windows.
-window // Запуск в оконном режиме.
-full // Запуском в полно экранном режиме.
-freq // Для установки частоты обновления.
-nocrashdialog // Подавляет некоторый объем памяти.
-32bit // Запуск в 32-разрядном режиме. Полезно только на 64-битных операционных системах.
-dev // Включает режим разработчика.
-autoconfig // Восстановление видео настроек по умолчанию. Игнорирует настройки внутри любого CFG файла.
-dxlevel // Устанавливает версию DirectX.
-w -h // Размеры экрана. (-w 800 -h 600)
Отдельные настройки
sv_forcepreload - Сила предварительной нагрузки? (default "0")
sv_backspeed - Скорость движения назад (спиной вперед ).
showhitlocation - Показывает местоположение "hit". (default "0")
flex_smooth - Изменение контроллера анимации.
props_break_max_pieces - Количество осколков от мелких предметов. (default " - 1")
func_break_max_pieces - Число реквизита частиц, таких как Gibs.
budget_show_history - Отключает \ Включает историю графики.
bugreporter_uploadasync - Загружает приложения асинхронно.
jpeg_quality - Качество скриншота.
commentary - Желаемое состояния режима комментарий.
gl_clear - Буфер случайного цвета каждого кадра.
muzzleflash_light - Динамический (отраженный) свет от вспышек. (default "1")
npc_height_adjust - Включает тест мод, для высоты "adjustmen".
lod_transitiondist - Расстояние на котором "lod" снижается на объектах. (default "800")
con_enable - Активирует консоль.
g15_update_msec - Интервал обновления клавиатуры Logitech G - 15.
developer - Последние сообщения консоля в левом углу экрана.
fps_max - Максимальный фпс.
fov_desired - Угол обзора.
viewmodel_fov - Визуальная отдалённость оружия.
viewmodel_fov_demo - Визуальная отдалённость оружия при просмотре демок.
zoom_sensivity_ratio - Чувствительность мышки, при включение "зума" снайпера.
sensivity - Чувствительность
record - Начать запись (pov) демо файла.
stop - Остановить запись (pov) демо файла.
clear - Очистить лог консоля.
password - Текущий пароль доступа к серверу.
skill - Уровень игры (1 - 3).
name - Ник
bind - Назначает какое - либо игровое действие клавише.
echo - Выводит сообщение в консоль.