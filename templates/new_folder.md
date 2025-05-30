<%*
const currentFile = tp.file.path(true);
const currentFolder = currentFile.substring(0, currentFile.lastIndexOf("/"));

const newFolderName = await tp.system.prompt("Enter new folder name:");
if (newFolderName) {
  const fullPath = `${currentFolder}/${newFolderName}`;
  await app.vault.createFolder(fullPath);
  new Notice(`Folder created: ${fullPath}`);
}
%>