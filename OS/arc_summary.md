# At 64GB arc size ( bytes)
```json
------------------------------------------------------------------------
ZFS Subsystem Report                            Wed May 17 15:03:43 2023
Linux 5.15.107-1-pve                                         2.1.11-pve1
Machine: pve (x86_64)                                        2.1.11-pve1

ARC status:                                                      HEALTHY
        Memory throttle count:                                         0

ARC size (current):                                    98.7 %   62.0 GiB
        Target size (adaptive):                       100.0 %   62.9 GiB
        Min size (hard limit):                          6.2 %    3.9 GiB
        Max size (high water):                           16:1   62.9 GiB
        Most Frequently Used (MFU) cache size:         95.5 %   58.9 GiB
        Most Recently Used (MRU) cache size:            4.5 %    2.7 GiB
        Metadata cache size (hard limit):              75.0 %   47.2 GiB
        Metadata cache size (current):                 11.4 %    5.4 GiB
        Dnode cache size (hard limit):                 10.0 %    4.7 GiB
        Dnode cache size (current):                     1.1 %   54.2 MiB

ARC hash breakdown:
        Elements max:                                               1.2M
        Elements current:                              98.1 %       1.2M
        Collisions:                                               404.3k
        Chain max:                                                     4
        Chains:                                                    38.0k

ARC misc:
        Deleted:                                                    1.5M
        Mutex misses:                                                122
        Eviction skips:                                              294
        Eviction skips due to L2 writes:                               0
        L2 cached evictions:                                     0 Bytes
        L2 eligible evictions:                                 321.1 GiB
        L2 eligible MFU evictions:                     44.3 %  142.2 GiB
        L2 eligible MRU evictions:                     55.7 %  178.9 GiB
        L2 ineligible evictions:                                11.9 GiB

ARC total accesses (hits + misses):                               108.6M
        Cache hit ratio:                               98.1 %     106.5M
        Cache miss ratio:                               1.9 %       2.1M
        Actual hit ratio (MFU + MRU hits):             97.5 %     105.8M
        Data demand efficiency:                        99.3 %      12.1M
        Data prefetch efficiency:                      36.1 %       2.8M

Cache hits by cache type:
        Most frequently used (MFU):                    83.4 %      88.9M
        Most recently used (MRU):                      15.9 %      17.0M
        Most frequently used (MFU) ghost:               0.2 %     253.9k
        Most recently used (MRU) ghost:                 0.3 %     338.0k
        Anonymously used:                               0.1 %      84.8k

Cache hits by data type:
        Demand data:                                   11.3 %      12.0M
        Prefetch data:                                  0.9 %       1.0M
        Demand metadata:                               87.7 %      93.4M
        Prefetch metadata:                              0.2 %     162.6k

Cache misses by data type:
        Demand data:                                    4.1 %      85.3k
        Prefetch data:                                 85.2 %       1.8M
        Demand metadata:                                1.6 %      32.5k
        Prefetch metadata:                              9.2 %     191.1k

DMU prefetch efficiency:                                            8.6M
        Hit ratio:                                     54.9 %       4.7M
        Miss ratio:                                    45.1 %       3.9M

L2ARC not detected, skipping section

Solaris Porting Layer (SPL):
        spl_hostid                                                     0
        spl_hostid_path                                      /etc/hostid
        spl_kmem_alloc_max                                       1048576
        spl_kmem_alloc_warn                                        65536
        spl_kmem_cache_kmem_threads                                    4
        spl_kmem_cache_magazine_size                                   0
        spl_kmem_cache_max_size                                       32
        spl_kmem_cache_obj_per_slab                                    8
        spl_kmem_cache_reclaim                                         0
        spl_kmem_cache_slab_limit                                  16384
        spl_max_show_tasks                                           512
        spl_panic_halt                                                 0
        spl_schedule_hrtimeout_slack_us                                0
        spl_taskq_kick                                                 0
        spl_taskq_thread_bind                                          0
        spl_taskq_thread_dynamic                                       1
        spl_taskq_thread_priority                                      1
        spl_taskq_thread_sequential                                    4

Tunables:
        dbuf_cache_hiwater_pct                                        10
        dbuf_cache_lowater_pct                                        10
        dbuf_cache_max_bytes                        18446744073709551615
        dbuf_cache_shift                                               5
        dbuf_metadata_cache_max_bytes               18446744073709551615
        dbuf_metadata_cache_shift                                      6
        dmu_object_alloc_chunk_shift                                   7
        dmu_prefetch_max                                       134217728
        ignore_hole_birth                                              1
        l2arc_exclude_special                                          0
        l2arc_feed_again                                               1
        l2arc_feed_min_ms                                            200
        l2arc_feed_secs                                                1
        l2arc_headroom                                                 2
        l2arc_headroom_boost                                         200
        l2arc_meta_percent                                            33
        l2arc_mfuonly                                                  0
        l2arc_noprefetch                                               1
        l2arc_norw                                                     0
        l2arc_rebuild_blocks_min_l2size                       1073741824
        l2arc_rebuild_enabled                                          1
        l2arc_trim_ahead                                               0
        l2arc_write_boost                                        8388608
        l2arc_write_max                                          8388608
        metaslab_aliquot                                         1048576
        metaslab_bias_enabled                                          1
        metaslab_debug_load                                            0
        metaslab_debug_unload                                          0
        metaslab_df_max_search                                  16777216
        metaslab_df_use_largest_segment                                0
        metaslab_force_ganging                                  16777217
        metaslab_fragmentation_factor_enabled                          1
        metaslab_lba_weighting_enabled                                 1
        metaslab_preload_enabled                                       1
        metaslab_unload_delay                                         32
        metaslab_unload_delay_ms                                  600000
        send_holes_without_birth_time                                  1
        spa_asize_inflation                                           24
        spa_config_path                             /etc/zfs/zpool.cache
        spa_load_print_vdev_tree                                       0
        spa_load_verify_data                                           1
        spa_load_verify_metadata                                       1
        spa_load_verify_shift                                          4
        spa_slop_shift                                                 5
        vdev_file_logical_ashift                                       9
        vdev_file_physical_ashift                                      9
        vdev_removal_max_span                                      32768
        vdev_validate_skip                                             0
        zap_iterate_prefetch                                           1
        zfetch_array_rd_sz                                       1048576
        zfetch_max_distance                                     67108864
        zfetch_max_idistance                                    67108864
        zfetch_max_sec_reap                                            2
        zfetch_max_streams                                             8
        zfetch_min_distance                                      4194304
        zfetch_min_sec_reap                                            1
        zfs_abd_scatter_enabled                                        1
        zfs_abd_scatter_max_order                                     10
        zfs_abd_scatter_min_size                                    1536
        zfs_admin_snapshot                                             0
        zfs_allow_redacted_dataset_mount                               0
        zfs_arc_average_blocksize                                   8192
        zfs_arc_dnode_limit                                            0
        zfs_arc_dnode_limit_percent                                   10
        zfs_arc_dnode_reduce_percent                                  10
        zfs_arc_evict_batch_limit                                     10
        zfs_arc_eviction_pct                                         200
        zfs_arc_grow_retry                                             0
        zfs_arc_lotsfree_percent                                      10
        zfs_arc_max                                                    0
        zfs_arc_meta_adjust_restarts                                4096
        zfs_arc_meta_limit                                             0
        zfs_arc_meta_limit_percent                                    75
        zfs_arc_meta_min                                               0
        zfs_arc_meta_prune                                         10000
        zfs_arc_meta_strategy                                          1
        zfs_arc_min                                                    0
        zfs_arc_min_prefetch_ms                                        0
        zfs_arc_min_prescient_prefetch_ms                              0
        zfs_arc_p_dampener_disable                                     1
        zfs_arc_p_min_shift                                            0
        zfs_arc_pc_percent                                             0
        zfs_arc_prune_task_threads                                     1
        zfs_arc_shrink_shift                                           0
        zfs_arc_shrinker_limit                                     10000
        zfs_arc_sys_free                                               0
        zfs_async_block_max_blocks                  18446744073709551615
        zfs_autoimport_disable                                         1
        zfs_btree_verify_intensity                                     0
        zfs_checksum_events_per_second                                20
        zfs_commit_timeout_pct                                         5
        zfs_compressed_arc_enabled                                     1
        zfs_condense_indirect_commit_entry_delay_ms                    0
        zfs_condense_indirect_obsolete_pct                            25
        zfs_condense_indirect_vdevs_enable                             1
        zfs_condense_max_obsolete_bytes                       1073741824
        zfs_condense_min_mapping_bytes                            131072
        zfs_dbgmsg_enable                                              1
        zfs_dbgmsg_maxsize                                       4194304
        zfs_dbuf_state_index                                           0
        zfs_ddt_data_is_special                                        1
        zfs_deadman_checktime_ms                                   60000
        zfs_deadman_enabled                                            1
        zfs_deadman_failmode                                        wait
        zfs_deadman_synctime_ms                                   600000
        zfs_deadman_ziotime_ms                                    300000
        zfs_dedup_prefetch                                             0
        zfs_default_bs                                                 9
        zfs_default_ibs                                               17
        zfs_delay_min_dirty_percent                                   60
        zfs_delay_scale                                           500000
        zfs_delete_blocks                                          20480
        zfs_dirty_data_max                                    4294967296
        zfs_dirty_data_max_max                                4294967296
        zfs_dirty_data_max_max_percent                                25
        zfs_dirty_data_max_percent                                    10
        zfs_dirty_data_sync_percent                                   20
        zfs_disable_ivset_guid_check                                   0
        zfs_dmu_offset_next_sync                                       1
        zfs_embedded_slog_min_ms                                      64
        zfs_expire_snapshot                                          300
        zfs_fallocate_reserve_percent                                110
        zfs_flags                                                      0
        zfs_free_bpobj_enabled                                         1
        zfs_free_leak_on_eio                                           0
        zfs_free_min_time_ms                                        1000
        zfs_history_output_max                                   1048576
        zfs_immediate_write_sz                                     32768
        zfs_initialize_chunk_size                                1048576
        zfs_initialize_value                        16045690984833335022
        zfs_keep_log_spacemaps_at_export                               0
        zfs_key_max_salt_uses                                  400000000
        zfs_livelist_condense_new_alloc                                0
        zfs_livelist_condense_sync_cancel                              0
        zfs_livelist_condense_sync_pause                               0
        zfs_livelist_condense_zthr_cancel                              0
        zfs_livelist_condense_zthr_pause                               0
        zfs_livelist_max_entries                                  500000
        zfs_livelist_min_percent_shared                               75
        zfs_lua_max_instrlimit                                 100000000
        zfs_lua_max_memlimit                                   104857600
        zfs_max_async_dedup_frees                                 100000
        zfs_max_log_walking                                            5
        zfs_max_logsm_summary_length                                  10
        zfs_max_missing_tvds                                           0
        zfs_max_nvlist_src_size                                        0
        zfs_max_recordsize                                       1048576
        zfs_metaslab_find_max_tries                                  100
        zfs_metaslab_fragmentation_threshold                          70
        zfs_metaslab_max_size_cache_sec                             3600
        zfs_metaslab_mem_limit                                        25
        zfs_metaslab_segment_weight_enabled                            1
        zfs_metaslab_switch_threshold                                  2
        zfs_metaslab_try_hard_before_gang                              0
        zfs_mg_fragmentation_threshold                                95
        zfs_mg_noalloc_threshold                                       0
        zfs_min_metaslabs_to_flush                                     1
        zfs_multihost_fail_intervals                                  10
        zfs_multihost_history                                          0
        zfs_multihost_import_intervals                                20
        zfs_multihost_interval                                      1000
        zfs_multilist_num_sublists                                     0
        zfs_no_scrub_io                                                0
        zfs_no_scrub_prefetch                                          0
        zfs_nocacheflush                                               0
        zfs_nopwrite_enabled                                           1
        zfs_object_mutex_size                                         64
        zfs_obsolete_min_time_ms                                     500
        zfs_override_estimate_recordsize                               0
        zfs_pd_bytes_max                                        52428800
        zfs_per_txg_dirty_frees_percent                               30
        zfs_prefetch_disable                                           0
        zfs_read_history                                               0
        zfs_read_history_hits                                          0
        zfs_rebuild_max_segment                                  1048576
        zfs_rebuild_scrub_enabled                                      1
        zfs_rebuild_vdev_limit                                  33554432
        zfs_reconstruct_indirect_combinations_max                   4096
        zfs_recover                                                    0
        zfs_recv_queue_ff                                             20
        zfs_recv_queue_length                                   16777216
        zfs_recv_write_batch_size                                1048576
        zfs_removal_ignore_errors                                      0
        zfs_removal_suspend_progress                                   0
        zfs_remove_max_segment                                  16777216
        zfs_resilver_disable_defer                                     0
        zfs_resilver_min_time_ms                                    3000
        zfs_scan_blkstats                                              0
        zfs_scan_checkpoint_intval                                  7200
        zfs_scan_fill_weight                                           3
        zfs_scan_ignore_errors                                         0
        zfs_scan_issue_strategy                                        0
        zfs_scan_legacy                                                0
        zfs_scan_max_ext_gap                                     2097152
        zfs_scan_mem_lim_fact                                         20
        zfs_scan_mem_lim_soft_fact                                    20
        zfs_scan_strict_mem_lim                                        0
        zfs_scan_suspend_progress                                      0
        zfs_scan_vdev_limit                                      4194304
        zfs_scrub_min_time_ms                                       1000
        zfs_send_corrupt_data                                          0
        zfs_send_no_prefetch_queue_ff                                 20
        zfs_send_no_prefetch_queue_length                        1048576
        zfs_send_queue_ff                                             20
        zfs_send_queue_length                                   16777216
        zfs_send_unmodified_spill_blocks                               1
        zfs_slow_io_events_per_second                                 20
        zfs_spa_discard_memory_limit                            16777216
        zfs_special_class_metadata_reserve_pct                        25
        zfs_sync_pass_deferred_free                                    2
        zfs_sync_pass_dont_compress                                    8
        zfs_sync_pass_rewrite                                          2
        zfs_sync_taskq_batch_pct                                      75
        zfs_traverse_indirect_prefetch_limit                          32
        zfs_trim_extent_bytes_max                              134217728
        zfs_trim_extent_bytes_min                                  32768
        zfs_trim_metaslab_skip                                         0
        zfs_trim_queue_limit                                          10
        zfs_trim_txg_batch                                            32
        zfs_txg_history                                              100
        zfs_txg_timeout                                                5
        zfs_unflushed_log_block_max                               131072
        zfs_unflushed_log_block_min                                 1000
        zfs_unflushed_log_block_pct                                  400
        zfs_unflushed_log_txg_max                                   1000
        zfs_unflushed_max_mem_amt                             1073741824
        zfs_unflushed_max_mem_ppm                                   1000
        zfs_unlink_suspend_progress                                    0
        zfs_user_indirect_is_special                                   1
        zfs_vdev_aggregate_trim                                        0
        zfs_vdev_aggregation_limit                               1048576
        zfs_vdev_aggregation_limit_non_rotating                   131072
        zfs_vdev_async_read_max_active                                 3
        zfs_vdev_async_read_min_active                                 1
        zfs_vdev_async_write_active_max_dirty_percent                 60
        zfs_vdev_async_write_active_min_dirty_percent                 30
        zfs_vdev_async_write_max_active                               10
        zfs_vdev_async_write_min_active                                2
        zfs_vdev_cache_bshift                                         16
        zfs_vdev_cache_max                                         16384
        zfs_vdev_cache_size                                            0
        zfs_vdev_default_ms_count                                    200
        zfs_vdev_default_ms_shift                                     29
        zfs_vdev_initializing_max_active                               1
        zfs_vdev_initializing_min_active                               1
        zfs_vdev_max_active                                         1000
        zfs_vdev_max_auto_ashift                                      14
        zfs_vdev_min_auto_ashift                                       9
        zfs_vdev_min_ms_count                                         16
        zfs_vdev_mirror_non_rotating_inc                               0
        zfs_vdev_mirror_non_rotating_seek_inc                          1
        zfs_vdev_mirror_rotating_inc                                   0
        zfs_vdev_mirror_rotating_seek_inc                              5
        zfs_vdev_mirror_rotating_seek_offset                     1048576
        zfs_vdev_ms_count_limit                                   131072
        zfs_vdev_nia_credit                                            5
        zfs_vdev_nia_delay                                             5
        zfs_vdev_open_timeout_ms                                    1000
        zfs_vdev_queue_depth_pct                                    1000
        zfs_vdev_raidz_impl cycle [fastest] original scalar sse2 ssse3 avx2
        zfs_vdev_read_gap_limit                                    32768
        zfs_vdev_rebuild_max_active                                    3
        zfs_vdev_rebuild_min_active                                    1
        zfs_vdev_removal_max_active                                    2
        zfs_vdev_removal_min_active                                    1
        zfs_vdev_scheduler                                        unused
        zfs_vdev_scrub_max_active                                      3
        zfs_vdev_scrub_min_active                                      1
        zfs_vdev_sync_read_max_active                                 10
        zfs_vdev_sync_read_min_active                                 10
        zfs_vdev_sync_write_max_active                                10
        zfs_vdev_sync_write_min_active                                10
        zfs_vdev_trim_max_active                                       2
        zfs_vdev_trim_min_active                                       1
        zfs_vdev_write_gap_limit                                    4096
        zfs_vnops_read_chunk_size                                1048576
        zfs_wrlog_data_max                                    8589934592
        zfs_zevent_len_max                                           512
        zfs_zevent_retain_expire_secs                                900
        zfs_zevent_retain_max                                       2000
        zfs_zil_clean_taskq_maxalloc                             1048576
        zfs_zil_clean_taskq_minalloc                                1024
        zfs_zil_clean_taskq_nthr_pct                                 100
        zil_maxblocksize                                          131072
        zil_min_commit_timeout                                      5000
        zil_nocacheflush                                               0
        zil_replay_disable                                             0
        zil_slog_bulk                                             786432
        zio_deadman_log_all                                            0
        zio_dva_throttle_enabled                                       1
        zio_requeue_io_start_cut_in_line                               1
        zio_slow_io_ms                                             30000
        zio_taskq_batch_pct                                           80
        zio_taskq_batch_tpq                                            0
        zvol_inhibit_dev                                               0
        zvol_major                                                   230
        zvol_max_discard_blocks                                    16384
        zvol_prefetch_bytes                                       131072
        zvol_request_sync                                              0
        zvol_threads                                                  32
        zvol_volmode                                                   1

VDEV cache disabled, skipping section

ZIL committed transactions:                                         3.8M
        Commit requests:                                          594.7k
        Flushes to stable storage:                                501.9k
        Transactions to SLOG storage pool:            0 Bytes          0
        Transactions to non-SLOG storage pool:        8.3 GiB     182.8k

```

# change
```bash
touch /etc/modprobe.d/zfs.conf
nano /etc/modprobe.d/zfs.conf
```
lower arc size to 16GB
```json
# Setting up ZFS ARC size on Ubuntu as per our needs
# Set Max ARC size => 16GB == 17179869184 Bytes
options zfs zfs_arc_max=17179869184
 
# Set Min ARC size => 1GB == 1073741824
options zfs zfs_arc_min=1073741824
```
apply and reboot
```bash
update-initramfs -u -k all
reboot
```