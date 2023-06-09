# Emacster
Emacs Multiple Session Manager + Android Termux Emacs  GUI :
 **Emacster**: Master / Manager of many Emacs&apos;s .

Emacs can be asked to start a Server that listens on either a local UNIX
domain socket (the default), OR on a TCP Socket .

On Android, there is Termux, and Emacs for Termux; in order to use it,
you must switch to the Termux window and run the 'emacs' command
in the terminal window.
On Windows, there is Emacs for Windows, and MSYS2 / Cygwin bash shell,
and Emacs can also listen on a TCP socket for Elisp code to run, and of course
on ("UNIX" : (Linux / BSD / Solaris / AIX ...)) POSIX platforms, 
Emacs can be run natively without a bash shell or other environment being necessary.
It would also be possible for an Android or Windows GUI application to Depend On
Termux and Termux Emacs being installed (Android), or on Emacs for Windows being
installed (Windows), or on just native Emacs being installed (Linux/UNIX), and to run
it in Batch Mode on demand.

**Emacster** provides the ability to issue  local or remote Termux/bash or Bash Shell
or SSH commands to start up Emacs Servers in Batch Mode on demand, OR to issue 
commands to existing local or remote SSH connected devices running Emacs Servers
over UNIX or TCP  sockets, managing public key  generation and exchange for remote hosts differently
for different supported platforms with **libssh2** and **OpenSSL** for (Linux / Android / Windows),
to start up and Manage Emacs sessions, and to send Emacs Lisp (ELISP) expressions that 
create / destroy / modify (Edit)  Emacs Buffers in those instances, and can Display
lists of Buffers, Buffers, and WebKit HTML Renderings of HTML Buffers, if **lib${X}WebKit**
is installed, to enable WYSIWYG HTML5 Editing , and which is able to start up / shutdown / query
the status of those running instances , query their buffer lists, etc.

Emacster will detect when  Multiple Users are editing the same buffer and will make the Shared Emacs
Session use Locking and Guided Patch Merging to permit safe multiple user editing sessions.

If Dependencies: Emacs+Termux + picolisp (Android) or Emacs+MSYS2 + SBCL (Windows) or 
Emacs + [SBCL](https://sbcl.org) (UNIX), or lib${X}WebKit 
or libssh2 or libxml2 or OpenSSL or bash shell or coreutils or tar / grep / sed / xz is not installed, 
Emacster will provide a [FLTK](https://fltk.org) GUI to guide their Installation.

On Linux, Emacster will be written mainly in ELISP + [picolisp](https://picolisp.com) ,with a C/C++ Library,
on Windows or other UNIX, picolisp will be replaced by SBCL Common LISP,  and 
on all platforms Emacster will use [FLTK](https://fltk.org/)  for its GUI components, however on Android
there will be an Android Java/Kotlin GUI Shell, and on Linux also it will use my SBCL Common LISP 
 [McCLIM](https://github.com/McCLIM/McCLIM) FLTK port work ; all these will be based around a 
common C/C++ library, **libEmacsSter.so**, buildable on all platforms .

A future extension will be a full-featured 'EmacsterHTTPD' implementation that uses **eww** to display
HTML5 and Mule Forms and provides CGI / HTML Submit Button processing support to provide a simple
HTTPD / HTTPS/TCP/(((TLS+SSL) or VPN) socket) or HTTP/(UNIX-domain socket) server, and full
integration with GIT and automatic SCM management of multi-user edited files, and a Chat Message facility
with Teams or Google Chat / WebRTC integration for users who have buffers of the same file loaded.
