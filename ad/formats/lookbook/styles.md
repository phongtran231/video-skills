# Lookbook styles

One `### Name` per style (Vietnamese name, shown in the picker). The lines under it:

- `id`: stable slug (cover image: public/styles/lookbook/<id>.jpg).
- `hot`: yes = shown under "Đang hot".
- `pipeline`: `fan` = the ceiling-fan composite (rooms + fan drawn in the edit, see lookbook.ts); `cut` = everything else.
- `beat`: seconds per outfit. `camera`: `fixed` (the framing is locked in the edit) or `free`.
- `transition`: ffmpeg xfade name used at each outfit change (fade, fadeblack, fadewhite, hblur, wipeleft, vertopen, circleopen…), `transition_s` its length.
- `sound`: what is heard at each change: whoosh, snap, clap, click or none.
- `description`: Vietnamese, for the picker.
- `scene`: the place (English). `framing`: the camera (English).
- `pose`: how she stands in the still each beat starts from (English). `motion`: what she does in the clip, ending on the moment that hides the change (English).

### Quạt trần đổi đồ
id: ceiling-fan
hot: yes
pipeline: fan
beat: 3
camera: fixed
transition: fan
transition_s: 0
sound: whoosh
description: Nhìn từ trần nhà xuống, người mẫu nằm trên thảm, mỗi lần cánh quạt lướt qua là một bộ đồ mới.
scene: a room seen from the ceiling
framing: top-down
pose: lying on the rug
motion: small natural movements

### Xoay một vòng đổi đồ
id: spin-change
hot: yes
pipeline: cut
beat: 3
camera: fixed
transition: hblur
transition_s: 0.35
sound: whoosh
description: Mỗi vòng xoay người là một bộ đồ mới, tóc và tà áo bay theo.
scene: a bright minimalist living room with a light oak floor, a cream wall and a tall plant in the corner
framing: vertical full-body shot at eye level, the whole figure in frame with space above the head
pose: standing in the middle of the frame facing the camera, a confident fashion pose
motion: she spins around once quickly on the spot, her hair and the outfit swirling with motion blur, and the spin carries on past the end of the shot

### Che ống kính
id: hand-cover-lens
hot: yes
pipeline: cut
beat: 3
camera: fixed
transition: fadeblack
transition_s: 0.3
sound: whoosh
description: Người mẫu đưa tay che ống kính, bỏ tay ra là đã thay bộ khác.
scene: a sunlit bedroom with white linen bedding, a full-length mirror and a wooden chair
framing: vertical medium-full shot at eye level, close enough that a hand can cover the lens
pose: standing a step from the camera, smiling at the lens, one hand on her hip
motion: she poses for a moment, then steps toward the camera and presses her open palm over the lens, the frame going dark at the end

### Nhảy lên đổi đồ
id: jump-change
hot: yes
pipeline: cut
beat: 3
camera: fixed
transition: fade
transition_s: 0.2
sound: whoosh
description: Bật nhảy lên, chân chạm đất là đã mặc bộ khác, năng lượng và vui nhộn.
scene: a quiet sunny street with a pastel wall, a small café table and potted plants
framing: vertical full-body shot at eye level, room above the head for the jump
pose: standing in the middle of the sidewalk, knees slightly bent, smiling at the camera
motion: she crouches and jumps straight up with arms raised, hair flying, and the shot ends at the top of the jump

### Búng tay đổi đồ
id: finger-snap
hot: yes
pipeline: cut
beat: 3
camera: fixed
transition: fadewhite
transition_s: 0.2
sound: snap
description: Búng tay một cái, chớp sáng, bộ đồ đã thay.
scene: a clean white studio with a soft grey backdrop and a single stool
framing: vertical medium-full shot at eye level
pose: standing facing the camera, one hand raised beside her face ready to snap
motion: she looks into the lens with a playful smile and snaps her fingers toward the camera, ending exactly on the snap

### Lau gương đổi đồ
id: mirror-wipe
hot: yes
pipeline: cut
beat: 3
camera: fixed
transition: wipeleft
transition_s: 0.45
sound: whoosh
description: Selfie trước gương, vuốt tay qua gương là sang bộ mới.
scene: a bathroom mirror selfie, a large round mirror, warm vanity light and a few plants
framing: mirror selfie, vertical, her full reflection holding a phone
pose: holding a phone up in front of the mirror, the other hand on her waist, posing for the selfie
motion: she poses, then sweeps her free hand across the mirror from right to left, as if wiping it, ending mid-wipe

### Bước qua cửa
id: door-walk
pipeline: cut
beat: 4
camera: fixed
transition: fadeblack
transition_s: 0.3
sound: whoosh
description: Mỗi lần bước qua khung cửa là một bộ đồ mới.
scene: a long bright hallway with a white door frame in the middle distance and a wooden floor
framing: vertical full-body shot from the end of the hallway, the door frame in the middle of the image
pose: standing just behind the door frame, about to walk through toward the camera
motion: she walks through the door frame toward the camera with a confident stride and keeps walking until she fills the frame at the end

### Sàn catwalk
id: runway
pipeline: cut
beat: 4
camera: fixed
transition: fade
transition_s: 0.15
sound: whoosh
description: Sải bước trên sàn diễn, mỗi lượt đi là một bộ trang phục.
scene: a fashion runway with a glossy black floor, bright white runway lights and a dark blurred audience
framing: vertical full-body shot from the end of the runway, centred
pose: standing at the far end of the runway, ready to walk
motion: she walks down the runway toward the camera with a model stride, stops at the end, strikes a pose and turns away

### Hất tóc đổi đồ
id: hair-flip
pipeline: cut
beat: 3
camera: fixed
transition: hblur
transition_s: 0.3
sound: whoosh
description: Cúi xuống rồi hất tóc lên, mái tóc che khung hình và bộ đồ đã đổi.
scene: a sunny balcony with white railings, green plants and a city view behind
framing: vertical medium shot from the waist up at eye level
pose: standing facing the camera with long loose hair, a soft smile
motion: she bends forward and flips her long hair back up toward the camera, the hair sweeping across the frame at the end

### Tung áo khoác
id: jacket-throw
pipeline: cut
beat: 3
camera: fixed
transition: fadeblack
transition_s: 0.25
sound: whoosh
description: Tung chiếc áo khoác về phía ống kính, áo che hết khung hình rồi lộ ra bộ mới.
scene: a stylish loft with exposed brick, a clothes rail and warm Edison bulbs
framing: vertical full-body shot at eye level
pose: standing in the middle of the room holding a light jacket in one hand
motion: she smiles and tosses the jacket straight at the camera, the fabric covering the lens at the end

### Kéo rèm
id: curtain-reveal
pipeline: cut
beat: 3
camera: fixed
transition: wiperight
transition_s: 0.45
sound: whoosh
description: Rèm kéo ngang qua khung hình, mở ra là đã sang bộ khác.
scene: a bright room with tall windows and long sheer white curtains in front of the camera
framing: vertical full-body shot through the curtains
pose: standing behind the half-open curtains, hand on the fabric
motion: she pulls the sheer curtain across in front of herself from left to right, the fabric sweeping over the frame at the end

### Cửa thang máy
id: elevator
pipeline: cut
beat: 3
camera: fixed
transition: vertopen
transition_s: 0.45
sound: click
description: Cửa thang máy đóng lại rồi mở ra với bộ đồ mới.
scene: inside a modern elevator with brushed steel walls and a mirror, seen from the lobby through the open doors
framing: vertical full-body shot facing the elevator doors
pose: standing in the middle of the elevator facing out, a cool confident pose
motion: she poses as the elevator doors slide closed in front of her, meeting in the middle at the end

### Xoay ô dưới mưa
id: umbrella-spin
pipeline: cut
beat: 3
camera: fixed
transition: circleopen
transition_s: 0.4
sound: whoosh
description: Xoay chiếc ô trong mưa, ô che khung hình và bộ đồ đổi theo.
scene: a rainy city street at dusk with wet reflective pavement and glowing shop windows
framing: vertical full-body shot at eye level
pose: standing under an open clear umbrella, smiling at the camera
motion: she twirls the umbrella and tilts it toward the camera so the canopy covers the frame at the end

### Bước xuống cầu thang
id: stairs
pipeline: cut
beat: 4
camera: fixed
transition: fade
transition_s: 0.3
sound: whoosh
description: Mỗi bậc cầu thang là một bộ đồ, sang trọng như tạp chí.
scene: a grand white marble staircase with a black iron railing and soft daylight
framing: vertical full-body shot from the foot of the stairs, looking slightly up
pose: standing on the upper steps with one hand on the railing
motion: she walks down two steps toward the camera, gracefully, one hand sliding on the railing

### Bước tới máy quay
id: walk-toward
pipeline: cut
beat: 3
camera: free
transition: fade
transition_s: 0.15
sound: whoosh
description: Đi thẳng về phía máy quay, mỗi bước là một bộ đồ mới.
scene: a wide sunny park path lined with trees and dappled light
framing: vertical full-body shot, the camera slowly backing away in front of her
pose: walking toward the camera mid-stride, relaxed and smiling
motion: she keeps walking toward the camera with a natural stride, swinging her arms, the camera backing away in front of her

### Lật camera điện thoại
id: phone-flip
pipeline: cut
beat: 3
camera: fixed
transition: squeezeh
transition_s: 0.35
sound: click
description: Kiểu selfie, xoay điện thoại một vòng là thay đồ xong.
scene: a cosy café corner with a window seat, plants and warm light
framing: vertical phone-camera selfie, medium shot, slightly above eye level
pose: sitting by the window looking into the phone camera, smiling
motion: she waves at the camera, then turns the phone around quickly so the view spins sideways at the end

### Vỗ tay đổi đồ
id: clap-change
pipeline: cut
beat: 3
camera: fixed
transition: fadewhite
transition_s: 0.2
sound: clap
description: Vỗ tay một cái thật to, chớp sáng, bộ đồ mới xuất hiện.
scene: a colourful pastel room with a pink wall, a round mirror and a fluffy rug
framing: vertical full-body shot at eye level
pose: standing facing the camera with hands apart, ready to clap
motion: she grins and claps her hands once in front of her, ending on the clap

### Một nhịp nhảy
id: dance-move
pipeline: cut
beat: 3
camera: fixed
transition: slideleft
transition_s: 0.3
sound: whoosh
description: Mỗi động tác nhảy là một bộ đồ, hợp nhạc trend TikTok.
scene: a bright dance studio with a wooden floor, a mirror wall and soft daylight
framing: vertical full-body shot at eye level
pose: standing in a dance pose, weight on one leg, arms ready
motion: she does one short upbeat dance move to the right, hips and arms on the beat, ending mid-move

### Hạ kính xe
id: car-window
pipeline: cut
beat: 3
camera: fixed
transition: wipedown
transition_s: 0.4
sound: click
description: Ngồi trong xe, kính hạ xuống là đã sang bộ mới.
scene: a parked convertible-style car on a sunny city street, seen from outside the driver's window
framing: vertical medium shot through the car window
pose: sitting in the driver's seat looking out of the open window, sunglasses on her head
motion: she smiles at the camera, then the window glass rises up in front of her, covering her at the end

### Mở tủ đồ
id: closet-door
pipeline: cut
beat: 3
camera: fixed
transition: vertopen
transition_s: 0.45
sound: click
description: Đóng cửa tủ lại, mở ra là một bộ trang phục khác.
scene: a walk-in closet with white wardrobe doors, warm shelf lights and neatly hung clothes
framing: vertical full-body shot facing the wardrobe
pose: standing in front of the open wardrobe doors, holding the door edges
motion: she poses, then pulls both wardrobe doors closed in front of herself, ending as they meet

### Chụp ảnh polaroid
id: polaroid
pipeline: cut
beat: 3
camera: fixed
transition: fadewhite
transition_s: 0.25
sound: click
description: Chụp một tấm polaroid, ánh đèn flash loé lên là đổi đồ.
scene: a sunny rooftop with fairy lights, a small table and city views
framing: vertical medium-full shot at eye level
pose: standing holding an instant camera at chest height
motion: she raises the instant camera to her eye and takes a photo toward the lens, ending on the bright flash

### Ngả lưng ra giường
id: bed-fall
pipeline: cut
beat: 3
camera: fixed
transition: fade
transition_s: 0.3
sound: whoosh
description: Ngả lưng xuống giường, bật dậy là một bộ đồ mới, nhẹ nhàng và đáng yêu.
scene: a cosy bedroom with a big white bed, fluffy pillows and morning sunlight
framing: vertical full-body shot from the foot of the bed
pose: standing in front of the bed facing the camera, arms open
motion: she laughs and lets herself fall backwards onto the soft bed, arms open, ending as she lands

### Đạp xe qua
id: bicycle
pipeline: cut
beat: 4
camera: fixed
transition: slideleft
transition_s: 0.35
sound: whoosh
description: Mỗi lần đạp xe lướt qua là một bộ đồ, tươi tắn và nhẹ nhàng.
scene: a tree-lined country road with flowers along the edge and soft sunlight
framing: vertical full-body side view at the edge of the road
pose: riding a vintage bicycle with a basket, smiling
motion: she rides the bicycle past the camera from right to left, hair moving in the breeze, leaving the frame at the end

### Hoàng hôn
id: sunset
pipeline: cut
beat: 4
camera: free
transition: fade
transition_s: 0.4
sound: whoosh
description: Dạo bước trong nắng hoàng hôn, mỗi khung là một bộ đồ, lãng mạn.
scene: a beach boardwalk at golden hour with warm backlight and a glowing sea
framing: vertical full-body shot, the camera slowly tracking beside her
pose: walking along the boardwalk, looking back over her shoulder
motion: she walks slowly and turns to smile at the camera, the sunset glow behind her

### Đèn chớp tắt
id: light-flicker
pipeline: cut
beat: 3
camera: fixed
transition: fadeblack
transition_s: 0.2
sound: click
description: Đèn tắt phụt rồi sáng lại, người mẫu đã mặc bộ khác.
scene: a moody room with one hanging pendant lamp and a dark wall
framing: vertical full-body shot at eye level under the lamp
pose: standing under the pendant lamp, a cool fashion pose
motion: she poses under the lamp, then reaches up and the light switches off, the room going dark at the end

### Đèn sân khấu
id: spotlight
pipeline: cut
beat: 3
camera: fixed
transition: circleopen
transition_s: 0.4
sound: click
description: Một vệt đèn sân khấu bật sáng, mỗi lần bật là một bộ đồ.
scene: a dark stage with a black floor and a single round spotlight
framing: vertical full-body shot of the stage, centred
pose: standing in the circle of the spotlight, a dramatic pose
motion: she holds a dramatic pose and turns slowly as the spotlight narrows and fades to dark at the end

### Tung hoa giấy
id: confetti
pipeline: cut
beat: 3
camera: fixed
transition: fadewhite
transition_s: 0.3
sound: clap
description: Tung một nắm hoa giấy, giấy bay che khung hình là đổi đồ, rất hợp mùa lễ.
scene: a festive party room with balloons, string lights and a glittery backdrop
framing: vertical full-body shot at eye level
pose: standing facing the camera with a handful of confetti
motion: she throws the confetti up toward the camera with a big smile, the pieces filling the frame at the end

### Vung khăn lụa
id: scarf-swipe
pipeline: cut
beat: 3
camera: fixed
transition: wipeleft
transition_s: 0.4
sound: whoosh
description: Vung chiếc khăn lụa ngang ống kính, khăn lướt qua là sang bộ mới.
scene: a bright garden terrace with white columns and climbing roses
framing: vertical medium-full shot at eye level
pose: standing holding a long silk scarf in both hands
motion: she swings the silk scarf across in front of the camera from right to left, the fabric sweeping over the frame at the end

### Vung túi xách
id: bag-swing
pipeline: cut
beat: 3
camera: fixed
transition: hblur
transition_s: 0.3
sound: whoosh
description: Vung túi xách về phía máy quay, túi lướt qua là thay đồ.
scene: a chic shopping street with boutique windows and soft daylight
framing: vertical full-body shot at eye level
pose: standing on the sidewalk holding a handbag by its strap
motion: she swings the handbag toward the camera in an arc, the bag sweeping across the lens at the end

### Phố đèn lồng
id: lantern-street
pipeline: cut
beat: 4
camera: free
transition: fade
transition_s: 0.4
sound: whoosh
description: Dạo phố cổ đèn lồng, mỗi góc phố là một bộ đồ, hợp áo dài và đồ truyền thống.
scene: an old town street at night with rows of colourful silk lanterns and yellow walls
framing: vertical full-body shot, the camera gently tracking backward in front of her
pose: walking slowly under the lanterns, holding the hem of her outfit
motion: she walks slowly toward the camera under the glowing lanterns, smiling and looking up at them
