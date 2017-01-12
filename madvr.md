配置文件

"1 NL Ngu low s-xbr125 hi" 默認設置 (NGU low/SSIM1D100%/super-xbr125 jincAR SSIM1D100AR/none)
"2 Ngu med s-xbr125 hi" (高質量低分辨率2次元視頻??)
"3 Ngu low s-xbr100 hi" --作為補強選項--
"4 Ngu low s-xbr125 hi LS" --作為補強選項-- 默認可加強一點線條,體感0.4,40%左右
"5 Ngu low s-xbr125 hi SRes" --作為補強選項-- 去模糊變銳利損失一點畫質有時候用這個還不如用NGR(動畫時)3次元有時可以用下,優勢不是很明顯(提升銳利度,可能會加重一點鋸齒-高清片源-,低清片源可以試下)
"6 Ngu low Ngu hi all" 1080P強制使用?? 25fps 720P都不能穩定壓住!!(除非超頻-)23.976(高碼率下依然會掉) 遊戲文件夾強制使用  720p質量很好(7.5分以上)圖像幹凈的視頻,3次元優先度大於2次元.  1080p藍光,2,3次元通用.  高清3d2次元動畫(優先度超高)
"7 Ngu med Ngu hi all" --作為補強選項-- (高質量低分辨率特別幹凈且模糊很少的2次元視頻)
"8 Ngu low Ngu hi all egg1" --作為補強選項-- NGU銳化1=柔化效果(全屏銳化柔化邊緣..然而會損失一些細節  偏向2,開1也可以
"9 Ngu low Ngu hi all egg2" --作為補強選項-- NGU銳化1=柔化效果(全屏銳化柔化邊緣..然而會損失一些細節  偏向2,開1也可以
"10 Ngu low Ngu hi- no hi no" 30fps720P專用 可用默認配置或此配置(高占用)
"11 Ngu low Ngu med-no hihi" 30fps720P專用 可用默認配置或此配置(中占用)
"12 s-sbr125 s-sbr125 hi" 60fps720P強制使用!
"13 Ngu low Ngu med-no hino"
===============================================================
if (srcWidth = 1920) and (srcHeight = 1080) and (deintFps > 31) "6 Ngu low Ngu hi all"
else if (srcWidth = 1920) and (srcHeight = 1080) "7 Ngu med Ngu hi all"
else if (srcWidth = 1280) and (srcHeight = 720) and (deintFps >=45 ) "12 s-sbr125 s-sbr125 hi"
else if (srcWidth = 1440) and (srcHeight = 1080) "2 Ngu med s-xbr125 hi"
else if (srcHeight > 1080) "11 Ngu low Ngu med-no hihi"

nico視頻文件夾,質量低-中,混合mmd
else if (filePath = "D:\BOON\bbbbb\*") and (fileName = "*mmd*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "D:\BOON\bbbbb\*") and (srcWidth <= 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "D:\BOON\bbbbb\*") and (srcWidth <= 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "D:\BOON\bbbbb\*") and (fileName = "*mmd*") and (srcWidth <= 960) and (srcHeight <= 720) and (deintFps < 25) "7 Ngu med Ngu hi all"
else if (filePath = "D:\BOON\bbbbb\*") and (fileName = "*mmd*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "D:\BOON\bbbbb\*") and (fileName = "*mmd*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "D:\BOON\bbbbb\*") and (fileName = "*mmd*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "D:\BOON\bbbbb\*") and (fileName = "*mmd*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"

(真人視頻全部用這個解決,包括紀錄片..)
else if (filePath = "D:\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps > 31) "1 NL Ngu low s-xbr125 hi"
else if (filePath = "D:\*") "2 Ngu med s-xbr125 hi"

二次元遊戲文件夾(質量中-高,狂用NGU)
else if (filePath = "H:\LastD\2 JI \單獨設置\*") "2 Ngu med s-xbr125 hi"
else if (filePath = "H:\LastD\2 JI \AA\BB單獨設置\*") "2 Ngu med s-xbr125 hi"

else if (filePath = "H:\LastD\2 JI\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth < 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "H:\LastD\2 JI\*") and (srcHeight < 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth = 1280) and (srcHeight = 1024) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth = 800) and (srcHeight = 600) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth = 854) and (srcHeight = 480) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth = 640) and (srcHeight = 480) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth = 1024) and (srcHeight = 768) and (deintFps < 31) "6 Ngu low Ngu hi all"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "H:\LastD\2 JI\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
else if (filePath = "H:\LastD\2 JI\*") "7 Ngu med Ngu hi all"

(真人視頻全部用這個解決)
else if (filePath = "H:\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps > 31) "1 NL Ngu low s-xbr125 hi"
else if (filePath = "H:\*") "2 Ngu med s-xbr125 hi"

(真人質量較低的視頻,分辨率中-低)
else if (filePath = "I:\77pan\*") and (srcWidth <= 720) "2 Ngu med s-xbr125 hi"
else if (filePath = "I:\77pan\*") and (srcHeight <= 576) "2 Ngu med s-xbr125 hi"
else if (filePath = "I:\77pan\*") "1 NL Ngu low s-xbr125 hi"

(高清真人視頻盤)
else if (filePath = "N:\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps > 31) "1 NL Ngu low s-xbr125 hi"
else if (filePath = "N:\*") "2 Ngu med s-xbr125 hi"

(動畫專用文件夾,主要為BD)
else if (filePath = "X:\BACCANO\*") and (srcWidth > 1280) and (srcHeight > 720) "2 Ngu med s-xbr125 hi"
else if (filePath = "X:\BACCANO\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 25) "6 Ngu low Ngu hi all"
else if (filePath = "X:\BACCANO\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "X:\BACCANO\*") and (srcWidth <= 1024) "2 Ngu med s-xbr125 hi"
else if (filePath = "X:\BACCANO\*") and (srcHeight <= 768) "2 Ngu med s-xbr125 hi"
else if (filePath = "X:\BACCANO\*") "7 Ngu med Ngu hi all"
(真人視頻解決)
else if (filePath = "X:\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps > 31) "1 NL Ngu low s-xbr125 hi"
else if (filePath = "X:\*") "2 Ngu med s-xbr125 hi"

(mmd高清動畫專用文件夾)
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth = 1600) and (srcHeight = 900) and (deintFps < 25) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth = 1600) and (srcHeight = 900) and (deintFps < 31) "12 s-sbr125 s-sbr125 hi"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth = 640) and (srcHeight = 480) and (deintFps > 50) "13 Ngu low Ngu med-no hino"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth = 1440) and (srcHeight = 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth <= 512) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth <= 1024) and (srcHeight <= 600) and (deintFps > 50) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth = 800) and (srcHeight = 600) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\MMDss\mmdaa\*") and (srcWidth <= 960) and (srcHeight <= 720) and (deintFps < 25) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\MMDss\mmdaa\*") "11 Ngu low Ngu med-no hihi"
(nico mmd專用文件夾)
else if (filePath = "Y:\BoonMmd\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\BoonMmd\*") and (srcWidth <= 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\BoonMmd\*") and (srcWidth <= 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\BoonMmd\*") and (srcWidth <= 960) and (srcHeight <= 720) and (deintFps < 25) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\BoonMmd\*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\BoonMmd\*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\BoonMmd\*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\BoonMmd\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
(nico mmd專用文件夾)
else if (filePath = "Y:\bbbbbb\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\bbbbbb\*") and (srcWidth <= 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\bbbbbb\*") and (srcWidth <= 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\bbbbbb\*") and (srcWidth <= 960) and (srcHeight <= 720) and (deintFps < 25) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\bbbbbb\*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\bbbbbb\*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\bbbbbb\*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\bbbbbb\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
(nico mmd專用文件夾)
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth <= 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth <= 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth <= 960) and (srcHeight <= 720) and (deintFps < 25) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\yousunbbbb\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
(nico陳年視頻)
else if (filePath = "Y:\skku\*") and (fileName = "*mmd*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\skku\*") and (srcWidth <= 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\skku\*") and (srcWidth <= 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\skku\*") and (fileName = "*mmd*") and (srcWidth <= 960) and (srcHeight <= 720) and (deintFps < 25) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\skku\*") and (fileName = "*mmd*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\skku\*") and (fileName = "*mmd*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\skku\*") and (fileName = "*mmd*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\skku\*") and (fileName = "*mmd*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
(nico陳年視頻)
else if (filePath = "Y:\bbbbb2\*") and (fileName = "*mmd*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\bbbbb2\*") and (srcWidth <= 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\bbbbb2\*") and (srcWidth <= 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\bbbbb2\*") and (fileName = "*mmd*") and (srcWidth <= 960) and (srcHeight <= 720) and (deintFps < 25) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\bbbbb2\*") and (fileName = "*mmd*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\bbbbb2\*") and (fileName = "*mmd*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\bbbbb2\*") and (fileName = "*mmd*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\bbbbb2\*") and (fileName = "*mmd*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
二次元遊戲文件夾(質量中-高)
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth = 1280) and (srcHeight = 720) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth < 640) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcHeight < 480) "2 Ngu med s-xbr125 hi"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth = 1280) and (srcHeight = 1024) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth = 800) and (srcHeight = 600) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth = 960) and (srcHeight = 540) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth = 854) and (srcHeight = 480) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth = 640) and (srcHeight = 480) and (deintFps < 31) "7 Ngu med Ngu hi all"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth = 1024) and (srcHeight = 768) and (deintFps < 31) "6 Ngu low Ngu hi all"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth <= 720) and (srcHeight <= 600) and (deintFps < 31) "10 Ngu low Ngu hi- no hi no"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth <= 1440) and (srcHeight <= 810) and (deintFps < 31) "11 Ngu low Ngu med-no hihi"
else if (filePath = "Y:\U\TDDO\sh\*") and (srcWidth >= 1280) and (srcHeight >= 720) and (deintFps >= 31) "13 Ngu low Ngu med-no hino"
else if (filePath = "Y:\U\TDDO\sh\*") "7 Ngu med Ngu hi all"

else if (filePath = "Y:\*") "2 Ngu med s-xbr125 hi"
