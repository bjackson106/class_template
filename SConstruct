import os
import platform

latex_env = Environment(tools=['default', 'pdflatex'])

latex_env.PrependENVPath("PATH", "/usr/local/texlive/2019/bin")
latex_env.Append(PDFLATEXFLAGS=['-halt-on-error', '-shell-escape', '-synctex=1'])
latex_env.Append(TEXINPUTS=[('../media')])

kwargs = {'variant_dir': 'build', 'duplicate':'y'}
Export('latex_env')
doc = SConscript('src/SConscript', **kwargs)

Install('dist', doc)
