echo "Linux link test file" > original.txt
- I created the original file to use for the hard link and symbolic link experiment.

ln original.txt hardlink.txt
- I created a hard link and confirmed it shares the same inode as the original.

ln -s original.txt symlink.txt
- I created a symbolic link that points to the original file path.

ls -li
- I listed files with inode information to compare link behavior.

stat original.txt hardlink.txt symlink.txt
- I gathered metadata showing inode, permissions, and link count for each file.

cat original.txt
cat hardlink.txt
cat symlink.txt
- I verified that all three names resolved to the same file contents before deleting the original.

rm original.txt
- I removed the original file name to test how hard and symbolic links behave.

ls -li
- I confirmed that hardlink.txt still exists and symlink.txt still points to the deleted file.

cat hardlink.txt
- I verified the hard link still provides file contents after the original is deleted.

cat symlink.txt
- I confirmed the symbolic link is broken after the original file is removed.
