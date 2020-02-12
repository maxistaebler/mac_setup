# Mac Setup

_Dieses Dokument beschreibt die benötigten Schritte um einen neuen Mac aufzusetzen_

## Homebrew

Um später folgende Installationen zu vereinfachen wird zuerst `homebrew` installiert.  
Auf dieser Seite [Link](https://brew.sh/index_de) kann die neueste Version von `homebrew` runtergeladen werden

**Folgenden Befehl im Terminal ausführen**
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## iTerm2 installieren & konfigurieren

_iTerm2_ ist ähnlich zum vorinstallierten _Terminal_ kann aber viel detaillierter konfiguriert werden.  
Die gesamte Installation kann [hier](https://gist.github.com/kevin-smets/8568070) nochmal nachgelesen werden.

**Download iTerm2**

Die neueste Version _iterm2_ kann [hier](https://www.iterm2.com) runtergalden werden.  
(Installation ist selbsterklärend)

**ZSH**

_ZSH_ ist eine andere (bessere) Shell und kann mit _curl_ installiert werden.  
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

**Powerlevel9000k**  

_Powerlevel9000k_ ist das beste Theme für ZSH.  
Mit folgendem Befehl wird das Theme automatisch in den passenden Ordner `~/.oh-my-zsh/custom/themes/` installiert.
```
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```  
Nachdem die Installation abgeschlossen ist kann man das default Theme ändern:  
In `~/.zshrc` die Zeile `ZSH_THEME="powerlevel9k/powerlevel9k"` auf das entsprechende Theme anpassen.

**Powerline Fonts**

Um eine saubere Darstellung zu ermöglichen müssen noch weitere Schriften installiert werden.  
Die einfachste Version ist mit folgenden Befehlen:
```
# clone
git clone https://github.com/powerline/fonts.git --depth=1
# install
cd fonts
./install.sh
# clean-up a bit
cd ..
rm -rf fonts
```

**Nach der Installation:**  
Nur die Schriften zu installieren reicht nicht!! Man muss noch in den Einstellungen von iTerm2 die entsprechenden Schriften unter _Preferences-Profile-Text_ auswählen.  
Von mir wird hier standardmäßig `Source Code Pro` gewählt.

**Farbschema anpassen**
Im default-Ordner `mac-setup`findet man im `iTerm2` Ordner eine Datei names `material-design-colors.itermcolors`.  
Diese datei muss noch über _Preferences-Profile-Colors_ importiert und ausgewählt werden.

## Python

Installieren mit Homebrew:  
```
brew install python
```  
Danach muss nur noch folgender _alias_ gesetzt werden: `alias python='python3'`.