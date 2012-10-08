import sublime, sublime_plugin
import string

class WordCountListener(sublime_plugin.EventListener):
	def on_selection_modified(self, view):
		regs = view.sel()
		word_status = ""
		word_count = len(string.split(view.substr(regs[0])))
		if(word_count > 0):
			word_status = str(word_count) + " words selected"
		view.set_status("Words", word_status)