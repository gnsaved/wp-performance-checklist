# wp-config.php snippets (paste ABOVE: "That's all, stop editing!")

## Disable file editing in wp-admin (recommended)
define('DISALLOW_FILE_EDIT', true);

## Lock down plugin/theme install & updates (ONLY for controlled environments)
# define('DISALLOW_FILE_MODS', true);

## Limit post revisions (optional)
define('WP_POST_REVISIONS', 10);

## Increase autosave interval (optional)
define('AUTOSAVE_INTERVAL', 120);
