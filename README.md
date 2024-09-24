# SUBSTRING

For each artist, display:

The name of the artist.
The special code of the artist (name the column special_code).
The special code consists of the first two letters of the artist's first two name parts (name parts are separated by the space). All letters must be lowercase. As an example, the special code for Wolfgang Paalen is 'wopa'.

It is not necessary to modify the function behavior for names with no space.

SELECT
  name,
  LOWER(SUBSTRING(name, 1, 2) || SUBSTRING(SPLIT_PART(name, ' ', 2), 1, 2)) AS special_code
FROM artist;
