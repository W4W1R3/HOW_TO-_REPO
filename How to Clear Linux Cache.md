# Clear Linux Cache (Memory, Swap and Buffer)

Memory cache is a component of the system’s RAM that stores frequently accessed data, allowing for faster retrieval and reduced load times. When a program or file is accessed, the system checks the cache before retrieving data from the slower storage devices like hard drives or SSDs. This process improves overall system performance and responsiveness.

However, as time goes by, the cache can become filled with unnecessary or outdated data, leading to reduced system efficiency. In such cases, clearing the memory cache can help regain lost performance.
Benefits of Clearing Memory Cache

    Improved System Performance: Clearing memory cache frees up system resources, allowing for more efficient data processing and faster application launch times.
    Enhanced Responsiveness: A cleaner memory cache reduces the time it takes for the system to access data, leading to a more responsive user experience.
    Reduced Memory Usage: By removing unnecessary data from the cache, the system can allocate more memory to critical processes and applications.
    Troubleshooting: Clearing memory cache can help resolve issues related to slow performance or application crashes resulting from cache corruption. 

How to Clear Memory Cache in Linux

Caution: Before proceeding, it is essential to note that clearing memory cache may cause unsaved data to be lost. Ensure you have saved all your work before attempting to clear the cache.

Clearing the memory cache in Linux involves flushing the cache and freeing up memory for other processes. While the cache is automatically managed by the kernel, you can manually clear it when needed. Here’s how you can do it:
1. Clear PageCache:

The PageCache, also known as the disk cache, is a memory cache that stores frequently accessed disk data. It reduces the need for the system to access slower storage devices, such as hard drives or SSDs, and helps speed up read and write operations. When the system accesses a file or program, it first checks the PageCache before moving to the disk. Clearing the PageCache can help improve system performance and free up memory.

To clear PageCache only, run the following commands in the terminal:

`sudo sync && echo 1 | sudo tee /proc/sys/vm/drop_caches `

2. Clear Dentries and Inodes:

Dentries (short for “directory entries”) cache stores information about the directory structure, while the inodes cache stores metadata about files, such as file permissions, ownership, and size. These caches help speed up file system operations and reduce the overhead associated with frequent file access. Clearing the dentries and inodes caches can help resolve file system-related issues and improve system performance.

To clear dentries and inodes only, run the following commands in the terminal:

`sudo sync && echo 2 | sudo tee /proc/sys/vm/drop_caches `

3. Clear Dentries, Inodes, and PageCache:

If you want to clear both dentries and inodes caches along with the PageCache, you can do so by running the following commands:

`sudo sync && echo 3 | sudo tee /proc/sys/vm/drop_caches `

Note that clearing these caches may cause unsaved data to be lost. Ensure you have saved all your work before attempting to clear the cache. Additionally, it’s important to remember that Linux automatically manages these caches for optimal performance. Clearing them manually is typically only necessary for troubleshooting or specific performance issues.
How to Clear Swap Cache in Linux

To “clear” the swap cache, you need to disable the swap space, which will force the system to move swapped-out pages back into the main memory. Then, you can re-enable swap space if necessary. Here’s how to do it:
1. Disable swap space:

Before proceeding, ensure that you have enough free memory to accommodate the swap data. You can check the available memory using the free command:

`free -h `

To disable the swap space, run the following command:

`sudo swapoff -a `

This command will move all the data from swap space back into the main memory, effectively “clearing” the swap cache.
2. Re-enable swap space

If you want to re-enable swap space, run the following command:

`sudo swapon -a `

This process will disable and re-enable the swap space, effectively clearing the swap cache. However, keep in mind that doing this frequently is not recommended, as it may cause performance issues. The system is designed to manage swap space automatically for optimal performance.
Automating Cache Clearing with a Cron Job

To automate cache clearing, you can create a cron job that runs at regular intervals:

`sudo crontab -e `

Add the following line to the crontab file, replacing ‘interval’ with the desired frequency (e.g., ‘*/60 * * * *’ for every hour):

`*/60 * * * *  sync && echo 3 | sudo tee /proc/sys/vm/drop_caches`


Save the file and exit. The cron job will now clear the memory cache at the specified interval.
Conclusion

Clearing memory cache in Linux can significantly improve system performance and efficiency.

By understanding the benefits of cache management and employing the methods described above, you can optimize your Linux system and ensure a more responsive user experience. Remember to exercise caution and save your work before clearing memory cache to prevent data loss.
