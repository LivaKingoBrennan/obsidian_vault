<%*
const currentFile = tp.file.path(true); // Full path to current file
const currentFolder = currentFile.substring(0, currentFile.lastIndexOf("/"));

const newFileName = await tp.system.prompt("Enter new file name:");
if (newFileName) {
  const newFilePath = `${currentFolder}/${newFileName}.md`;
  await tp.file.create_new("", newFilePath);
}
%>