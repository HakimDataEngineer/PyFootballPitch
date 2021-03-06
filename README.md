# PyFootballPitch
functions to draw a football pitch in various available styles for matplotlib and bokeh


### Matplotlib

the drawpitch() function for matplotlib allows you to input your own specified pitch
size. So it's easy to adjust the standard 105x68meters pitch.

create a figure and an axis object before invoking
<b>ax = drawpitch(ax)</b>

    
    
    def drawpitch(ax, hspan = [-52.5, 52.5], vspan = [-34, 34],\
                linecolor = '#525252', facecolor = '#f0f0f0', arcs = True, \
                lw = 1.5, x_offset = [4,4], y_offset = [4,4], style_id = None,
                grass_cutting = False):
    '''
    '''
    -----
    Draws a pitch (default horizontal) on an axes object with width 105m and height 68m
    -----
    If you are using StatsBomb Data with a 120x80yard pitch, use:
    measure = 'SBData'
    -----
    If you are using any other pitch size, set measure to yards or metres
    for correct pitch markings and
    hspan = [left, right] // eg. for SBData this is: hspan = [0, 120]
    vspan = [bottom, top] //
    to adjust the plot to your needs.
    -----
    orientation: 'horizontal' or 'vertical'
    -----
    Choose a Style with
    style_id = 1...8
    you can also set linecolor, lw (linewidth), and facecolor individually.
    -----
    default arcs = True; False to not draw the penalty box arcs.
    -----
    use x_offset and y_offset to extend the plot further past the pitch
    or also to just draw half the pitch
    -----



### Bokeh:

for the bokeh function, invoke
<b>p = draw_pitch()</b> - the function creates the figure for you.

    def draw_pitch(width = 700, height = 500, fill_color = '#B3DE69', fill_alpha = 0.5,
               line_color = 'grey', line_alpha = 1,
               arcs = True):
   
               
    -----
    Draws and returns a pitch on a Bokeh figure object with width 105m and height 68m
    p = drawpitch()
    -----
    If you are using StatsBomb Data with a 120x80yard pitch, use:
    measure = 'SB'
    -----
    If you are using Opta Data, use:
    measure = 'Opta'
    -----
    If you are using any other pitch size, set measure to yards or metres
    for correct pitch markings and
    hspan = [left, right] // eg. for SBData this is: hspan = [0, 120]
    vspan = [bottom, top] //
    to adjust the plot to your needs.
    -----
    set arcs = False to not draw the penaltybox arcs
    '''
