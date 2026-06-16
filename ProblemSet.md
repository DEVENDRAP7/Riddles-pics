# Riddles - Pics — 100 Answer Words

4 Pics 1 Word format. Each level = one answer word (4 image concepts + letter bank added later). 100 unique words, mixed lengths, difficulty ascends with length/abstractness. Level number = order.

---

## 3 letters (1–10)
1. SUN
2. CAR
3. DOG
4. CUP
5. KEY
6. BEE
7. ICE
8. EGG
9. HAT
10. PEN

## 4 letters (11–25)
11. FIRE
12. RAIN
13. BOOK
14. STAR
15. TREE
16. FISH
17. BELL
18. MOON
19. CAKE
20. SHIP
21. LEAF
22. RING
23. DRUM
24. GOLD
25. WIND

## 5 letters (26–45)
26. CLOCK
27. HEART
28. CHAIR
29. PLANT
30. CLOUD
31. BEACH
32. LIGHT
33. MUSIC
34. SMILE
35. WATER
36. HORSE
37. BREAD
38. TRAIN
39. PHONE
40. SNAKE
41. CROWN
42. BRUSH
43. PAINT
44. SWORD
45. RIVER

## 6 letters (46–65)
46. FLOWER
47. BRIDGE
48. CASTLE
49. CAMERA
50. ROCKET
51. GARDEN
52. WINTER
53. CANDLE
54. ISLAND
55. PUZZLE
56. PENCIL
57. WINDOW
58. GUITAR
59. ANCHOR
60. BUTTON
61. JUNGLE
62. MIRROR
63. PARROT
64. SCHOOL
65. TUNNEL

## 7 letters (66–80)
66. RAINBOW
67. BALLOON
68. DOLPHIN
69. PYRAMID
70. LIBRARY
71. COMPASS
72. DIAMOND
73. STADIUM
74. THUNDER
75. VOLCANO
76. PICTURE
77. FACTORY
78. HARVEST
79. JOURNEY
80. MACHINE

## 8 letters (81–92)
81. MOUNTAIN
82. ELEPHANT
83. SANDWICH
84. AIRPLANE
85. UMBRELLA
86. DINOSAUR
87. SNOWFALL
88. FIREWORK
89. BIRTHDAY
90. TREASURE
91. AIRCRAFT
92. DOORBELL

## 9+ letters (93–100)
93. TELESCOPE
94. ADVENTURE
95. CHOCOLATE
96. ORCHESTRA
97. WATERFALL
98. LIGHTHOUSE
99. BUTTERFLY
100. ENVIRONMENT

---

## Notes for build
- All 100 words are unique.
- JSON per level later: `level`, `answer`, `images[4]` (asset paths), `letterBank` (answer letters + decoys), `length` (auto = answer.length).
- 4 image concepts per word generated/sourced in a later step (~400 images total).
- Letter bank: answer letters shuffled + 4–6 decoy letters; boxes count = word length.
- Difficulty ascends by word length (3 → 11 letters).
