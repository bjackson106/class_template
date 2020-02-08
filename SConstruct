import os
import platform

latex_env = Environment(tools=['default', 'pdflatex'])

latex_env.PrependENVPath("PATH", "/usr/local/texlive/2019/bin")
latex_env.Append(PDFLATEXFLAGS=['-halt-on-error', '-shell-escape', '-synctex=1'])
latex_env.Append(TEXINPUTS=[('../media')])

Export('latex_env')
doc = SConscript('src/SConscript')

Install('dist', doc)
