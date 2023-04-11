# kubectl-delete-all

## Description

This is a kubectl plugin that deletes all resources inside a namespace. It first checks if the resource has any finalizer and removes the finalizer before deleting the resource. Finally, it does the same for the namespace as well.

This plugin is useful for cleaning up a namespace that contains resources that are stuck in terminating state due to finalizers.

## Installation

To install this plugin, follow these steps:

Download the kubectl-delete-all file from this repository

Make it executable: chmod +x kubectl-delete-all

Move it to a directory that's in your PATH variable: mv kubectl-delete-all /usr/local/bin/

## Usage

To use this plugin, run the following command:

kubectl delete-all <namespace>

Replace `<namespace>` with the name of the namespace you want to delete.

For example:

kubectl delete-all test

This will delete all resources and the namespace named test.

## License

This project is licensed under the MIT License - see the LICENSE file for details.