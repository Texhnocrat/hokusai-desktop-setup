# 🌊 Ukiyo-e Desktop Setup (Kubuntu)

A clean, minimalist desktop environment inspired by traditional Japanese woodblock prints—specifically Katsushika Hokusai's *The Sea at Satta in Suruga Province* and *The Great Wave off Kanagawa*. 

This setup features a unified parchment-and-ink color space, a borderless tiling terminal configuration, customized audio layout tracking, and custom standalone artwork assets.

---

## 🎥 Walkthrough & Demos

### Main System Walkthrough
This complete recording demonstrates the boot-to-desktop sequence, our custom fastfetch greeting, tab management inside the terminal, active reading layouts, and launching an video file via the CLI using `mpv`.

![Full Walkthrough](assets/unixmainc.mp4)

### Custom Lock Screen
A quick look at the minimalist security screen utilizing our custom ukiyo-e terminal workstation art.

![Lockscreen Demo](assets/Lockscreen.mp4)

---

## 🖼️ Visual Gallery & Component Breakdown

### 1. The Main Desktop Environment
The core desktop layout utilizes a flat taskbar matching the soft blue oceanic hues of the main print. 

![Main Desktop](assets/My_Linux_Rice/2.mainscreen.png)
* **Wallpaper Asset:** ![Wallpaper Asset](assets/My_Linux_Rice/11.UkiyoPicture.jpeg)
* **Second Monitor Screen:** ![Calm Before Storm](assets/My_Linux_Rice/8.calmbeforestorm.jpeg) (A peaceful evening featuring two boats sailing on calm waters)

### 2. Custom Terminal Environment (Kitty)
Driven by the Kitty terminal backend, this interface strips away window borders and title bars for maximum screen real estate. 

* **Greeting Screen:** ![Greeting Screen](assets/My_Linux_Rice/1.terminalgreeting.png) Features a custom text greeting over the parchment canvas.
* **System Diagnostics:** ![Fastfetch View](assets/My_Linux_Rice/3.fastfetchview.png) & ![Btop View](assets/My_Linux_Rice/7.btop.png) Shows detailed system information and core performance layout using custom canvas-colored borders.
* **CMatrix Theme:** ![CMatrix Theme](assets/My_Linux_Rice/4.cmatrix.png) Terminal matrix stream utilizing matching dark ink tones.

![Terminal Overview](assets/My_Linux_Rice/3.fastfetchview.png)

<details>
<summary>📄 Click to view the full kitty.conf file</summary>

```toml
# Hokusai: The Sea at Satta in Suruga Province Theme
# Background and foreground
background #E8DCC2
foreground #1f1f1f

no_titlebar yes

font_family        IBM Plex Mono
bold_font          auto
italic_font        auto
bold_italic_font   auto
font_size 13.0

cursor_shape block
cursor_blink_interval 0
cursor_stop_blinking_after 0
shell_integration no-cursor

scrollback_lines 5000
wheel_scroll_multiplier 3.0
mouse_hide_wait -1

remember_window_size  no
initial_window_width  1200
initial_window_height 750
window_border_width 1.5pt
enabled_layouts tall
window_padding_width 0
window_margin_width 2
hide_window_decorations titlebar-only

enabled_layouts tall,stack

map ctrl+shift+enter new_window
map ctrl+shift+] next_window
map ctrl+shift+[ previous_window
map ctrl+shift+l next_layout
map ctrl+alt+r   goto_layout tall
map ctrl+alt+s   goto_layout stack

cursor #2c6e91
cursor_text_color #ffffff

selection_background #a3cdd9
selection_foreground #1f1f1f

color0  #2e2e2e
color1  #b0493e
color2  #728c69
color3  #c4a45f
color4  #4d8ea3
color5  #7a6e80
color6  #7bb0a8
color7  #dcdcdc

color8  #505050
color9  #c65b51
color10 #8dae7a
color11 #ddc67b
color12 #5ea2b4
color13 #9e85a0
color14 #a2d0c5
color15 #ffffff

tab_bar_style powerline
tab_powerline_style slanted
tab_bar_edge bottom
tab_bar_align left
active_tab_font_style   bold
inactive_tab_font_style normal
active_tab_background   #a3cdd9
active_tab_foreground   #1f1f1f
inactive_tab_background #8B4021
inactive_tab_foreground #E8DCC2
tab_bar_background      #065299

background_opacity 0.90

draw_minimal_borders yes
active_border_color   #8B4021
inactive_border_color #a3cdd9

url_color                #153A1B
