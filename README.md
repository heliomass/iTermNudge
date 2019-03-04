# iTerm Nudge
## What Is It?
Allows you to manipulate [iTerm 2 v3](https://www.iterm2.com) from the command line, even if you're in an ssh session or within tmux.

## Usage
	--color
		Changes the terminal colour.

		Use one of the following letters followed by
		a standard hex colour code:

		g = foreground
		h = background
		i = bold color
		j = selection color
		k = selected text color
		l = cursor
		m = cursor text

		E.g. Turn the background white:
		iterm_nudge --color hffffff

	--profile
		Changes the profile to the supplied name.

		E.g. Change profile to "my profile":
		iterm_nudge --profile my_profile


	--cursor
		Changes the cursor.

		Use the following codes:
		0: Block
		1: Vertical bar
		2: Underline

		E.g. Change cursor to underline:
		iterm_nudge --cursor 2

	--annotate
		Adds an annotation.

		E.g. Add an annotation saying "Hello World!" (original, I know)
		iterm_nudge --annotate 'Hello World!'

	--badge
		Sets a badge

		E.g. Set a badge with the current directory:
		iterm_nudge --badge "$(pwd)"

	--clear_badge
		Clears the badge

		I.e.
		iterm_nudge --clear_badge
		(note, this will override the --badge argument if both are supplied)
		
	--tab-color
		Change the colour of the current tab. Ca be one of:

		    red, orange, yellow, green, blue, violet, gray

		If an invalid colour is provided, it will fail silently

	--tab-reset
		Reset the colour

	--force
		Use this to output the escape codes even if $TERM_PROGRAM isn't
		set to iTerm. Useful if you're in an ssh session, but you weren't able
		to pass through TERM_PROGRAM from the client. Does not require a second argument.

	Run the command without any arguments to discover if you're in an iTerm or not.
	E.g.:

	iterm_nudge && echo "You're in an iTerm session" || echo "You're not running iTerm :("

## Further Reading
iTerm 2 v3 escape code documentation [is here](https://www.iterm2.com/documentation-escape-codes.html)
