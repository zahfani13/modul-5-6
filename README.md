color_cycle = cycle(["light blue", "light green", "light pink", "light yellow", "light cyan"]) "untuk mewarnai telur"
egg_width = 45 "untuk mengetahui lebar telur"
egg_height = 55 "untuk mengetahui tinggi telur"
egg_score = 10 "jika telur masuk score bertambah 10"
egg_speed = 500 "kecepatan telur sampai 500"
catcher_color = "blue" "penangkap telur berwarna biru"
lives_remaining = 3 "permainan telur diberi kesempatan sampai 3 kali"
 messagebox.showinfo("Game Over!", "Final Score: "+ str(score)) "jika kesempatan sudah habis maka akan muncul tulisan game over"
 c.bind("<Left>", move_left) "untuk memindahkan penangkap telur ke kiri"
 c.bind("<Right>", move_right) "untuk memindahkan penangkap telur ke kanan"
 def increase_score(points):
    global score, egg_speed, egg_interval
    score += points
    egg_speed = int(egg_speed * difficulty)
    egg_interval = int(egg_interval * difficulty)
    c.itemconfigure(score_text, text="Score: "+ str(score)) "untuk menghitung score yang telah didapatkan dalam permainan"
