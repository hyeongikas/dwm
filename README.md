-----

# DWM

This repository contains "my" custom configuration files for various tools and applications.

## Contents

- [dwm](https://github.com/hyeongikas/dwm-main): My customized build of the dynamic window manager.
- [neofetch](https://github.com/hyeongikas/neofetch): Initial commit, May 29, 2024
- [nvim](https://github.com/hyeongikas/nvim): Initial commit, May 29, 2024
- [power10k](https://github.com/hyeongikas/power10k): Initial commit, May 29, 2024
- [simple status](https://github.com/hyeongikas/simple_status): Initial commit, May 29, 2024
- [st](https://github.com/hyeongikas/st-main): Initial commit, May 29, 2024
- .xinitrc

## Cheat Sheet for DWM

Below is a cheat sheet for managing windows in DWM:

```c
static Key keys[] = {
	/* modifier                     key        function        argument */
	{ MODKEY,                       XK_l,      setmfact,       {.f = +0.05} },
	{ MODKEY,                       XK_k,      focusstack,     {.i = -1 } },
	{ MODKEY,                       XK_j,      focusstack,     {.i = +1 } },
	{ MODKEY,                       XK_h,      setmfact,       {.f = -0.05} },
	{ MODKEY,                       XK_g,      togglebar,      {0} },
	{ MODKEY,                       XK_f,      zoom,           {0} },
	{ MODKEY,                       XK_d,      incnmaster,     {.i = -1 } },
	{ MODKEY,                       XK_s,      incnmaster,     {.i = +1 } },
	{ MODKEY,                       XK_q,      killclient,     {0} },
	{ MODKEY,                       XK_w,      setlayout,      {.v = &layouts[0]} },
	{ MODKEY,                       XK_e,      setlayout,      {.v = &layouts[1]} },
	{ MODKEY,                       XK_r,      setlayout,      {.v = &layouts[2]} },
	{ MODKEY|ShiftMask,             XK_r,      togglefloating, {0} },
	{ MODKEY,                       XK_t,      setlayout,      {0} },
	{ MODKEY,                       XK_space,  spawn,          {.v = roficmd } },
	{ MODKEY,                       XK_Return, spawn,          {.v = termcmd } },
	{ MODKEY,                       XK_Tab,    view,           {0} },
	{ MODKEY,                       XK_0,      view,           {.ui = ~0 } },
	{ MODKEY|ShiftMask,             XK_0,      tag,            {.ui = ~0 } },
	{ MODKEY,                       XK_comma,  focusmon,       {.i = -1 } },
	{ MODKEY,                       XK_period, focusmon,       {.i = +1 } },
	{ MODKEY|ShiftMask,             XK_comma,  tagmon,         {.i = -1 } },
	{ MODKEY|ShiftMask,             XK_period, tagmon,         {.i = +1 } },
	{ MODKEY,                       XK_minus,  setgaps,        {.i = -1 } },
	{ MODKEY,                       XK_equal,  setgaps,        {.i = +1 } },
	{ MODKEY|ShiftMask,             XK_equal,  setgaps,        {.i =  0 } },
	{ MODKEY,                       XK_F5,     xrdb,           {.v = NULL } },
	TAGKEYS(                        XK_1,                      0)
	TAGKEYS(                        XK_2,                      1)
	TAGKEYS(                        XK_3,                      2)
	TAGKEYS(                        XK_4,                      3)
	TAGKEYS(                        XK_5,                      4)
	TAGKEYS(                        XK_6,                      5)
	TAGKEYS(                        XK_7,                      6)
	TAGKEYS(                        XK_8,                      7)
	TAGKEYS(                        XK_9,                      8)
	{ MODKEY|ShiftMask,             XK_q,      quit,           {0} },
};
```

Explanation: This cheat sheet contains keybindings for various actions in DWM, such as resizing windows, switching between windows, and managing layouts.

## How to Install DWM with My Configuration

1. Clone the [dwm repository](https://github.com/hyeongikas/dwm-main):

```bash
git clone https://github.com/hyeongikas/dwm-main.git
```

2. Navigate to the dwm directory:

```bash
cd dwm-main
```

3. Build and install DWM:

```bash
make clean install
```

4. Modify the `config.h` file according to your preferences.

5. Restart your window manager.
