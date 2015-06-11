# iTerm Nudge
## What Is It?
Allows you to manipulate iTerm from the command line, even if you're in an ssh session or within tmux.

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
		iterm_nudge --background hffffff

	--profile
		Changes the profile to the supplied name.

	--cursor
		Changes the cursor.

		Use the following codes:
		0: Block
		1: Vertical bar
		2: Underline

	--force
		Use this to output the escape codes even if \$TERM_PROGRAM isn't
		set to iTerm. Useful if you're in an ssh session, but you weren't able
		to pass through TERM_PROGRAM from the client.

	Run the command without any arguments to discover if you're in an iTerm or not.
	E.g.:

	iterm_nudge && echo "You're in an iTerm session" || echo "You're not running iTerm :("
