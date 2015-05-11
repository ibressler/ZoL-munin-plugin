ZoL-munin-plugin
================

A Munin plugin for monitoring ZFS on Linux


How to configure
================
    cp zfs_stats_ /usr/local/bin/
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_l2efficiency
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_l2utilization
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_cachehitdtype
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_cachehitlist
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_efficiency
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_utilization
    ln -s /usr/local/bin/zfs_stats_ /etc/munin/plugins/zfs_stats_fragmentation

    cat <<EOF > /etc/munin/plugin-conf.d/zfs-stats
    [zfs_*]
    user root
    EOF

	/etc/init.d/munin-node restart
