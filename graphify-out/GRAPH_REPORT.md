# Graph Report - openvddk  (2026-11-12)

## Corpus Check
- 318 files · ~287,280 words
- Verdict: corpus is large enough that graph structure adds value.
- Unclassified: 15 file(s) not represented in the graph (top: (none) 11, .map 1, .in 1)

## Summary
- 2262 nodes · 6311 edges · 139 communities (96 shown, 43 thin omitted)
- Extraction: 86% EXTRACTED · 14% INFERRED · 0% AMBIGUOUS · INFERRED: 870 edges (avg confidence: 0.83)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- Go Admin Bundle and Journal
- Go Config Collection
- C ABI Headers and Layout
- C Shim Runtime
- Bundle Redaction Tests
- Error Kinds and Syscalls
- C Conformance Harness
- Dynamic Loading and Hashing
- govmomi vSphere Objects
- TLS and NBD Sessions
- ELF Debug Inspection
- Fake Host Test Doubles
- CABI Error Exports
- NBD-0002 Async Read Faults
- Go Slice and Action Helpers
- HotAdd Worker Boot Order
- Source Disk Options
- govmomi Fault Types
- VDDK 8 Reference Decisions
- HotAdd Transport Decisions
- Connection Lifecycle
- Journal and Attachment Tests
- Async Finish and Wipe
- HotAdd Qualification Catalogue
- VixDiskLib Info and Blocks
- Disk Allocation Accounting
- govmomi Task Fakes
- Config and Benchmarks
- NBD Disk Read Path
- Fuzz Parser Tests
- Host Identity Accessors
- Memory Reader Helpers
- HotAdd Recovery Semantics
- HotAdd Device Read Behavior
- NBD Transport List Rules
- govmomi VM Controllers
- Connect and BIOS UUID Checks
- TLS Refusal Handling
- Transport and ReadAsync Rules
- ConnectEx and Diagnostic Bundle
- Crash Consistency and Safety
- Metadata Emit Path
- Chunked Read Concurrency
- Descriptor Parsing
- Reference Transcripts and Builds
- ABI Manifest Generation
- Allocation Block Model
- Gated Device Reader
- HotAdd Candidate Selection
- Migratekit NBD Pipeline
- Registry and Locking
- Internal Package Map
- Library Swap Test Kit
- VixDisk Info Helpers
- NBD Multi-Connection Limits
- Binary Kit and Worker Setup
- govmomi Simulator Fixtures
- NBD Open Error Codes
- Host Boot Identity
- Architecture and ABI Status
- Allocation Maps via NFC
- Release Check Matrices
- NFC Service Fallback
- Contract and Governance Policies
- NBD Cipher and Fault Checks
- IO Delivery Completion
- C/Go ABI Boundary
- Clean-Room Contribution Rules
- Consumer Callbacks and Config
- NFC Sessions and Buffers
- Init Lifecycle Observations
- NFC Access Control
- Host Not-Connected Handling
- Vix Errors and Transports
- Skipz Compression Observations
- Trace Diff Tooling
- Contributing and DCO
- ABI Artifacts and Build Container
- Changed Block Tracking
- HotAdd Source Disk Writes
- Parent Path Parsing
- UUID Parsing
- Clean-Room Implementation Policy
- NFC Timeout Configuration
- Trace Message Tools
- Independent Disk Reads
- IO Gate Behavior
- HotAdd Negative Cases
- NFC Reads Over TLS
- HCTL Device Parsing
- Selftest Shell Helpers
- Implementation Language Decisions
- Build Platform Decisions
- Logging Decisions
- HotAdd Attach Time
- HotAdd NFS Placement
- HotAdd Read Throughput
- Transport List Observations
- HotAdd Crash Script
- HotAdd Observe Script
- Header Stamp Script
- HotAdd Many-Disk Attach
- HotAdd Random Read Bench
- vCenter Privilege Requirements
- NBD First Read Observations
- Devkit Shell Script
- Evalkit Shell Script
- PrepareForAccess Calls
- Callback Re-entry Rules
- Cross-Cutting Packages
- Encoded Handle Decision
- vSphere Target Decision
- Reads During Reconfigure
- HotAdd Storage Failures
- VixDiskLib Call Tracing
- Changed-Area Image Checks
- HTTPS Connection Stress
- Shared BIOS UUID Check
- Proxy Residue Script
- Run Script
- Fuzz Script
- ListTransportModes API
- QueryAllocatedBlocks API
- ReadMetadata API
- License Decision
- ABI Declaration Decision
- Namespace Decision
- Artifact Naming Decision
- No Hosted CI Decision
- Module Root

## God Nodes (most connected - your core abstractions)
1. `VixError` - 56 edges
2. `Open()` - 55 edges
3. `VixDiskLibHandle` - 54 edges
4. `record()` - 45 edges
5. `code()` - 39 edges
6. `setup()` - 38 edges
7. `main()` - 38 edges
8. `Disk` - 34 edges
9. `LocalHost` - 30 edges
10. `source()` - 28 edges

## Surprising Connections (you probably didn't know these)
- `BufSizeIn64KB buffer size key` --semantically_similar_to--> `Slow storage keys and sessions`  [INFERRED] [semantically similar]
  docs/observations/NBD-0027-sessions-nfc-buffers-and-async-read-ahead.md → evalkit/KNOWN-DIFFERENCES.md
- `nfc ReadTimeoutMs and RequestTimeoutMs keys` --semantically_similar_to--> `OpenVDDK configuration keys`  [INFERRED] [semantically similar]
  docs/observations/NBD-0028-vmware-config-keys-observed.md → evalkit/README.md
- `Lost NFC connection during read returns 14009` --semantically_similar_to--> `VMware library SIGPIPE on silent host`  [INFERRED] [semantically similar]
  evalkit/KNOWN-DIFFERENCES.md → docs/observations/NBD-0028-vmware-config-keys-observed.md
- `Missing snapshot returns 13003` --semantically_similar_to--> `Silent NBD switch for missing snapshot`  [INFERRED] [semantically similar]
  evalkit/KNOWN-DIFFERENCES.md → docs/observations/NBD-0029-vddk803-rechecks-on-67.md
- `session_open()` --calls--> `VixDiskLib_InitEx()`  [INFERRED]
  devkit/examples/common.h → cabi/shim.c

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **HotAdd transaction lifecycle** — contract_hotadd_state_machine, contract_hotadd_journal, contract_hotadd_recovery, contract_hotadd_cleanup, contract_proxy_identification, contract_device_identity [INFERRED 0.85]
- **Ordered transport list and fallback** — contract_hotadd, contract_nbdssl, contract_nbd, contract_san, contract_transport_fallback [EXTRACTED 1.00]
- **Data integrity outranks bug-for-bug compatibility** — contract_data_integrity_priority, contract_data_corruption_policy, contract_unsupported_fail_explicit, contract_deviation_policy [INFERRED 0.75]
- **HotAdd attach-read-detach pipeline** — architecture_hotadd_transaction, architecture_internal_hotadd, architecture_internal_linuxdev, architecture_hotadd_recovery, security_hotadd_host_safety [EXTRACTED 1.00]
- **ABI verification gates** — compatibility_vixdisklib_8_0_3, compatibility_status_levels, testing_abi_gate, testing_conformance_harness, abi_transcript_cases [EXTRACTED 1.00]
- **Clean-room provenance policy** — contributing_clean_room_rule, docs_clean_room_method, docs_clean_room_sources, docs_clean_room_exclusions, provenance_evidence_categories [EXTRACTED 1.00]
- **Read-ahead design decisions (window, single-reader release, run-based ramp)** — docs_decisions_d_0017_readahead_tolerates_reordering, docs_decisions_d_0019_readahead_releases_behind_single_reader, docs_decisions_d_0020_readahead_grows_with_the_run [INFERRED 0.85]
- **HotAdd proxy identity and safe cleanup** — docs_decisions_d_0014_hotadd_implementation, docs_decisions_d_0016_proxies_without_disk_ids, docs_decisions_d_0018_shared_bios_uuid_refuses_hotadd, docs_security_review_0_7_0_hotadd_close_deletes_device_by_name, docs_security_review_0_7_0_recovery_deletes_journal_redo_paths [INFERRED 0.85]
- **NFC session count, buffer size and host NFC memory limit** — docs_tuning_nbd_sessions, docs_tuning_nfc_buffer_size, docs_tuning_host_nfc_memory_limit, docs_security_review_0_7_4_multi_session_close_waits_per_session [INFERRED 0.85]
- **Reference-parity failure handling** — docs_decisions_d_0021_log_line_format, docs_decisions_d_0023_negative_cases, docs_decisions_d_0028_read_failures, docs_decisions_d_0032_permission_refusals [INFERRED 0.75]
- **QueryAllocatedBlocks answer sources over HotAdd** — docs_decisions_d_0035_allocated_blocks_from_vcenter, docs_decisions_d_0036_allocated_blocks_over_nfc, docs_decisions_d_0035_allocated_blocks_from_vcenter_changed_areas, docs_decisions_d_0036_allocated_blocks_over_nfc_host_map [INFERRED 0.85]
- **NBD and NBDSSL rollout on main** — docs_decisions_d_0037_nbd_on_main_hotadd_on_branch, docs_decisions_d_0039_transport_listing_and_fallback, docs_decisions_d_0040_four_reader_nbd_rate_accepted, docs_decisions_d_0044_hotadd_branch_retired [INFERRED 0.75]
- **VDDK 8.0.3 reference library evidence** — docs_decisions_d_0046_vddk_803_only_reference, docs_observations_abi_0001_reference_elf_identity, docs_observations_hotadd_0001_reference_hotadd_vsphere7, docs_observations_hotadd_0004_readasync_over_hotadd [INFERRED 0.75]
- **HotAdd read path and read-ahead** — docs_observations_hotadd_0001_reference_hotadd_vsphere7, docs_observations_hotadd_0004_readasync_over_hotadd, docs_observations_hotadd_0005_nbdkit_and_readahead, docs_observations_hotadd_0010_200gb_library_swap_test, docs_observations_hotadd_0011_multithreaded_readers [INFERRED 0.75]
- **NFC session and buffer configuration** — docs_decisions_d_0045_several_nfc_sessions_per_disk, docs_decisions_d_0048_nfc_buffers_and_async_read_ahead, docs_decisions_d_0049_more_vmware_keys_honoured, docs_decisions_d_0051_openvddk_key_prefix_documented, docs_decisions_d_0052_direct_esxi_connections [INFERRED 0.75]
- **Worker reset with a source disk attached: recovery** — docs_observations_hotadd_0027_worker_reset_with_a_disk_attached, docs_observations_hotadd_0032_worker_restart_protected, docs_observations_hotadd_0024_administrative_program [INFERRED 0.75]
- **Read-ahead behaviour on latency and memory paths** — docs_observations_hotadd_0012_device_reads_per_read_call, docs_observations_hotadd_0016_thread_matrix_ram_path, docs_observations_hotadd_0017_extent_reads_with_gaps, docs_observations_hotadd_0018_nfs_v3_path [INFERRED 0.75]
- **Refusal rather than guessing a device or VM identity** — docs_observations_hotadd_0014_duplicate_bios_uuid, docs_observations_hotadd_0015_same_disk_two_processes, docs_observations_hotadd_0033_proxy_mac_change [INFERRED 0.75]
- **NFS source outage: worker crash versus no vCPU hold on ESXi 8** — docs_observations_hotadd_0038_source_datastore_outage_proxy_kernel_crash_on_outage, docs_observations_hotadd_0038_source_datastore_outage_hardlockup_panic_setting, docs_observations_hotadd_0039_datastore_outage_vsphere_80_no_vcpu_hold_on_esxi8, docs_observations_hotadd_0038_source_datastore_outage_cleanup_after_crash_asymmetry [INFERRED 0.75]
- **HotAdd release checks from 0.6.24 to 0.6.26** — docs_observations_hotadd_0046_hotadd_on_vsphere_67, docs_observations_hotadd_0047_hotadd_on_vsphere_67_and_70, docs_observations_hotadd_0048_host_disconnected_while_attached, docs_observations_hotadd_0049_robustness_and_identification_fix, docs_observations_hotadd_0050_release_0625_measured, docs_observations_hotadd_0051_independent_disks_and_rdm, docs_observations_hotadd_0052_release_0626_measured [EXTRACTED 1.00]
- **LVM check in the HotAdd library** — docs_observations_hotadd_0036_live_iso_worker_lvm_activates_source_vg, docs_observations_hotadd_0058_lvm_check_under_load_lvmconfig_check_cost, docs_observations_hotadd_0058_lvm_check_under_load_lvmconfig_memo [INFERRED 0.75]
- **Reference clear-text NBD fallback when NBDSSL was asked for** — docs_observations_nbd_0002_async_faults_consumers_clear_text_after_killed_run, docs_observations_nbd_0004_virt_v2v_negative_tests_clear_text_inspection_opens, docs_observations_nbd_0008_vsphere_67_functional_closure_two_readers_clear_text [INFERRED 0.85]
- **VDDK 7.0.3 and 8.0.3 references compared with the candidate across vSphere labs** — docs_observations_nbd_0005_vsphere_67, docs_observations_nbd_0010_vsphere_67_and_70, docs_observations_nbd_0017_developer_kit_and_vddk7_programs [EXTRACTED 1.00]
- **Failed Open error codes matched to reference except snapshot not found** — docs_observations_nbd_0003_negative_open_metadata_snapshot_not_found_opens_file, docs_observations_nbd_0011_nbd_matrix_matrix_lab_b, docs_observations_nbd_0018_release_0700_measured_release_0700_regression [INFERRED 0.75]
- **NBDSSL decryption without AES instructions** — docs_observations_nbd_0023_nbdssl_without_aes_instructions_go_portable_aes, docs_observations_nbd_0023_nbdssl_without_aes_instructions_esxi_aes_only_ciphers, docs_observations_nbd_0023_nbdssl_without_aes_instructions_tls12_aes128_offer, evalkit_known_differences_nbdssl_aes_warning [INFERRED 0.85]
- **skipz zero elision on the wire** — docs_observations_nbd_0024_migratekit_measured_on_the_wire_skipz_zero_elision, docs_observations_net_0004_skipz_over_nfc_skipz_request_flag, docs_observations_net_0004_skipz_over_nfc_skipz_code3_pieces, docs_observations_net_0004_skipz_over_nfc_strict_skipz_decoding [INFERRED 0.85]
- **Levers for throughput from slow datastores** — docs_observations_nbd_0027_sessions_nfc_buffers_and_async_read_ahead_buf_size_key, docs_observations_nbd_0027_sessions_nfc_buffers_and_async_read_ahead_one_buffer_at_a_time, docs_observations_nbd_0023_nbdssl_without_aes_instructions_multi_session_candidate, docs_observations_nbd_0026_one_or_several_connections_slow_datastore_multi_conn_mode [INFERRED 0.75]

## Communities (139 total, 43 thin omitted)

### Community 0 - "Go Admin Bundle and Journal"
Cohesion: 0.06
Nodes (40): program(), TestUserAgent(), UserAgent(), init(), FuzzEngine(), ioReply(), Register(), Codes() (+32 more)

### Community 1 - "Go Config Collection"
Cohesion: 0.06
Nodes (58): init(), collectConfig(), nbdSettings, canonical(), Empty(), Config, knownOwnKey(), Load() (+50 more)

### Community 2 - "C ABI Headers and Layout"
Cohesion: 0.04
Nodes (34): log_msg(), now(), read_password(), usage(), VixDiskLibAdapterType, VixDiskLibBlock, VixDiskLibConnectParam, VixDiskLibConnectParamsState (+26 more)

### Community 3 - "C Shim Runtime"
Cohesion: 0.08
Nodes (60): call_with_va_list(), flatten(), init_common(), ovx_c_alloc_blocklist(), ovx_c_emit(), set_callbacks(), VixDiskLib_AllocateConnectParams(), VixDiskLib_Attach() (+52 more)

### Community 4 - "Bundle Redaction Tests"
Cohesion: 0.06
Nodes (53): TestBundleArchive(), TestBundleRedaction(), TestBundleSkipsPlantedLogs(), TestReadPassword(), TestUsageAndExitCodes(), cmdBundle(), collectDevices(), collectJournal() (+45 more)

### Community 5 - "Error Kinds and Syscalls"
Cohesion: 0.13
Nodes (61): VixError, kind(), main(), cb_probe_done(), slot_issue(), write_probe(), main(), rec() (+53 more)

### Community 6 - "C Conformance Harness"
Cohesion: 0.07
Nodes (59): case_connect_local(), case_connect_null_out(), case_connect_preinit(), case_connectex_bad_transport(), case_connectex_local(), case_errtext_free_null(), case_errtext_locale(), case_errtext_postinit() (+51 more)

### Community 7 - "Dynamic Loading and Hashing"
Cohesion: 0.09
Nodes (47): block(), builtin_final(), builtin_init(), builtin_update(), sha256_backend(), sha256_final(), sha256_hex(), sha256_init() (+39 more)

### Community 8 - "govmomi vSphere Objects"
Cohesion: 0.07
Nodes (19): FuzzLVMConfig(), acceptsAll(), ExecRunner(), Protection, parseLVMConfig(), LVMMemo, Ticket, isNotFound() (+11 more)

### Community 9 - "TLS and NBD Sessions"
Cohesion: 0.07
Nodes (44): openNBDSession(), FuzzRuns(), Dial(), Options, pinnedTLS(), Runs(), checkData(), diskByte() (+36 more)

### Community 10 - "ELF Debug Inspection"
Cohesion: 0.07
Nodes (40): Expectation, Export, Facts, Function, gateResult, goInitPlan, goInitState, Link (+32 more)

### Community 11 - "Fake Host Test Doubles"
Cohesion: 0.07
Nodes (12): fakeHost, position, atPosition(), deviceKey(), discover(), diskAtPosition(), Reader, sharedPV() (+4 more)

### Community 12 - "CABI Error Exports"
Cohesion: 0.16
Nodes (35): cause(), code(), goString(), initialized(), notSupported(), ovx_go_access(), ovx_go_check_repair(), ovx_go_cleanup() (+27 more)

### Community 13 - "NBD-0002 Async Read Faults"
Cohesion: 0.05
Nodes (25): NBD-0002 Async reads, network faults and real consumers over NBD and NBDSSL, NBD-0003 Failed Open and disk metadata over NBD and NBDSSL, NBD-0004 virt-v2v under faults over NBD and NBDSSL, nbdkit retry filter reopens disk up to 5 times with 2 to 32 s backoff, NBD-0005 HotAdd, NBD and NBDSSL on vSphere 6.7, NBD-0006 NBD and NBDSSL on vSphere 8.0.3, vSphere 8.0.3 functional suite: reads, failed Open codes and faults match 7.0 and 6.7, NBD-0007 Four readers at once: causes investigated; vCenter session lost during read (+17 more)

### Community 14 - "Go Slice and Action Helpers"
Cohesion: 0.10
Nodes (27): Action, Entry, Options, Plan, faultpoint(), contains(), dsJoin(), findAttached() (+19 more)

### Community 15 - "HotAdd Worker Boot Order"
Cohesion: 0.06
Nodes (38): HOTADD-0036 worker without its own disk, booted from a live ISO, CD-ROM or network boot must stay first in boot order, Live-ISO lvm2 with event activation activates the source volume group on attach, HOTADD-0038 source NFS datastore stops answering during a read (S3), Candidate cleans up after a worker crash with a disk attached; reference does not, Worker kernel panics on NMI hard lockup while ESXi holds its vCPUs during NFS outage, HOTADD-0039 NFS datastore outage under HotAdd read on vSphere 8.0 (S3b), ESXi 8.0.3 does not hold worker vCPUs during NFS outage; the read simply waits (+30 more)

### Community 16 - "Source Disk Options"
Cohesion: 0.18
Nodes (38): SourceDisk, Open(), journalFiles(), newHost(), setup(), source(), TestAssessMatchesRecover(), TestAttachErrorAfterEffectIsRolledBack() (+30 more)

### Community 17 - "govmomi Fault Types"
Cohesion: 0.08
Nodes (26): firstMissing(), TestInChain(), TestIndependentBackings(), TestRDMChain(), TestSelectLink(), chainLinks(), chainPaths(), diskBacking() (+18 more)

### Community 18 - "VDDK 8 Reference Decisions"
Cohesion: 0.08
Nodes (27): D-0046 VDDK 8.0.3 only reference, D-0047 links under VDDK 7 names as workaround, D-0050 HotAdd LVM check remembered, ABI-0001 reference ELF identity (VDDK 8.0.3), VDDK 8.0.3 libvixDiskLib: 46 exported VixDiskLib_ functions, 13 version nodes, GLIBC_2.16 max, ABI-0002 VDDK 7.0.3 compared with 8.0.3, VDDK 7.0.3 differs from 8.0.3 in client-version ceiling and InitEx after Exit (SIGABRT), ARG-0001 argument validation and error text (+19 more)

### Community 19 - "HotAdd Transport Decisions"
Cohesion: 0.07
Nodes (25): D-0003 HotAdd first; SAN unsupported by design, D-0012 Library swap test, D-0014 HotAdd implementation, D-0016 HotAdd on proxies without disk IDs, D-0017 Read-ahead tolerates reordered requests inside its window, D-0018 A shared BIOS UUID refuses HotAdd, as the reference does, D-0019 Read-ahead releases what lies behind a single reader, D-0020 A single reader's look-ahead grows with its sequential run (+17 more)

### Community 20 - "Connection Lifecycle"
Cohesion: 0.09
Nodes (17): Connection, hasMode(), namesSAN(), nbdsslToNBD(), open(), openHotAdd(), ParseModes(), openNBD() (+9 more)

### Community 21 - "Journal and Attachment Tests"
Cohesion: 0.14
Nodes (26): TestWriteAttachments(), TestWriteJournal(), captureLog(), TestDiskStatisticsAtClose(), TestDiskStatisticsWithoutReads(), withoutPrefix(), TestConcurrent(), TestLifecycle() (+18 more)

### Community 22 - "Async Finish and Wipe"
Cohesion: 0.16
Nodes (21): Cleanup(), EndAccess(), PrepareForAccess(), withSession(), ReadAsync(), TestReadAsyncEndingAtOnceCallsBackBeforeReturning(), Wait(), codeErr() (+13 more)

### Community 23 - "HotAdd Qualification Catalogue"
Cohesion: 0.08
Nodes (23): D-0023 HotAdd negative cases, D-0026 HotAdd qualification catalogue, Binding qualification catalogue closes HotAdd, D-0027 Read-only by design, D-0028 Failed read answers, EIO from device maps to VIX_E_FILE_ERROR (7), D-0029 Kit carries admin program, openvddk-admin recovery and diagnostic program (+15 more)

### Community 24 - "VixDiskLib Info and Blocks"
Cohesion: 0.18
Nodes (19): VixDiskLib_FreeInfo(), VixDiskLib_GetInfo(), main(), usage(), main(), on_done(), usage(), conn_opt() (+11 more)

### Community 25 - "Disk Allocation Accounting"
Cohesion: 0.11
Nodes (9): allocation, Disk, inflight, metadata, readStats, mibPerSec(), readLine(), engine (+1 more)

### Community 26 - "govmomi Task Fakes"
Cohesion: 0.12
Nodes (9): fakePlatform, AttachSpec, DetachSpec, newPlatform(), AttachConfigSpec(), DetachConfigSpec(), diskMode(), waitTask() (+1 more)

### Community 27 - "Config and Benchmarks"
Cohesion: 0.18
Nodes (16): TestSingleReaderExtentsWithSmallGaps(), alignedBuffer(), New(), BenchmarkRandomSmallReads(), newMem(), TestBuffersAreAligned(), TestCloseWaitsForReadsInFlight(), TestConcurrentReaders() (+8 more)

### Community 28 - "NBD Disk Read Path"
Cohesion: 0.13
Nodes (8): nbdDisk, nbdSession, closeNBDSession(), Reader, max64(), min64(), block, Source

### Community 29 - "Fuzz Parser Tests"
Cohesion: 0.11
Nodes (18): FuzzParse(), FuzzParseModes(), FuzzParseVMXSpec(), FuzzDecodeSkipZeros(), FuzzParseAllocationReply(), FuzzParseDDBReply(), FuzzParseIOPiece(), FuzzParseOpenReply() (+10 more)

### Community 30 - "Host Identity Accessors"
Cohesion: 0.16
Nodes (7): LocalHost, Platform, ProxyInfo, IdentifyProxy(), identifyProxy(), IdentifyProxyForAttach(), ProxyCandidates()

### Community 31 - "Memory Reader Helpers"
Cohesion: 0.11
Nodes (5): memReader, alignedBuffer(), lower(), preadFull(), Device

### Community 32 - "HotAdd Recovery Semantics"
Cohesion: 0.12
Nodes (18): HotAdd recovery at Open and Cleanup, HotAdd journaled attach/detach state machine, Tested applications nbdkit virt-v2v migratekit, Direct connections to ESXi host (0.7.4), Tested vSphere versions 6.7 to 9.1, VixDiskLib_Cleanup, VixDiskLib_Open, Compatibility matrix 0.7.4 (+10 more)

### Community 33 - "HotAdd Device Read Behavior"
Cohesion: 0.12
Nodes (10): HOTADD-0012 device reads per read call, HOTADD-0013 warm migration with a migration application, virt-v2v UEFI fallback loader missing for Debian 13, Warm migration passes write identical bytes in both libraries, HOTADD-0016 several threads on one disk on RAM-backed path, HOTADD-0017 extent reads with small gaps (CBT delta pattern), HOTADD-0018 the same 200 GiB disk on an NFS v3 array, HOTADD-0019 cold migration from and to an NFS array (+2 more)

### Community 34 - "NBD Transport List Rules"
Cohesion: 0.13
Nodes (14): NBD-0021 Every ordered transport list, Empty transport list versus NULL, san:san:hotadd process abort in VMware library, NET-0005 Reference on a direct ESXi connection, ha-nfc-service object on direct connection, ApiType HostAgent on direct connection, hotadd alone with reader not a VM of the server, Known differences from VixDiskLib 8.0.3 (+6 more)

### Community 35 - "govmomi VM Controllers"
Cohesion: 0.13
Nodes (12): Controller, State, FuzzJournalRecord(), ChooseSlot(), mayHaveAttached(), FuzzDatastorePath(), parentDir(), scsiController() (+4 more)

### Community 36 - "Connect and BIOS UUID Checks"
Cohesion: 0.25
Nodes (16): ovx_go_exit(), connectParams(), TestConnectRefusesSharedBIOSUUID(), TestConnectWithSharedBIOSUUIDAndOtherTransports(), Close(), Connect(), Disconnect(), ExitAll() (+8 more)

### Community 37 - "TLS Refusal Handling"
Cohesion: 0.23
Nodes (6): TestTLSRefusal(), classic(), dial(), Conn, tlsRefusal(), tlsState()

### Community 38 - "Transport and ReadAsync Rules"
Cohesion: 0.18
Nodes (13): Transports HotAdd NBDSSL NBD verification, VixDiskLib_ReadAsync, Transport list parsing rules for ConnectEx, VDDK 7 compatibility link workaround, NBD and NBDSSL qualification record, OpenVDDK 0.7.0 release notes, OpenVDDK 0.7.1 release notes, NBDSSL and NBD transports (ESXi NFC service, TCP 902) (+5 more)

### Community 39 - "ConnectEx and Diagnostic Bundle"
Cohesion: 0.14
Nodes (14): VixDiskLib_ConnectEx, Diagnostic bundle contents and secret redaction, openvddk-admin recovery and diagnostic tool, Recovery decisions leave forget detach finish refuse, docs/MESSAGES.md library message inventory, ConnectEx log messages (transports, sign-in, BIOS UUID), Message format OpenVDDK VixDiskLib prefix and function name (D-0021), Message levels LOG and WARN delivery without callbacks (D-0022) (+6 more)

### Community 40 - "Crash Consistency and Safety"
Cohesion: 0.23
Nodes (13): Linux HotAdd device identification, Diagnostic bundle, HotAdd failure injection, HotAdd transport, HotAdd cleanup, HotAdd durable journal, HotAdd qualification catalogue, HotAdd recovery (+5 more)

### Community 41 - "Metadata Emit Path"
Cohesion: 0.24
Nodes (9): delivered(), emit(), emitIn(), Fn, Redact(), TestRedact(), channel, Level (+1 more)

### Community 42 - "Chunked Read Concurrency"
Cohesion: 0.17
Nodes (3): Op, readChunks(), Spread

### Community 43 - "Descriptor Parsing"
Cohesion: 0.16
Nodes (8): Parse(), parseExtent(), FuzzParse(), TestDeltaAndSparse(), TestFixtureDescriptor(), unquote(), Descriptor, Extent

### Community 44 - "Reference Transcripts and Builds"
Cohesion: 0.19
Nodes (12): Transcript cases (symbols, init, args, connect), Recorded reference transcript (VDDK 8.0.3), Reproducible build (make repro, pinned EL8 container), Conformance harness (76 offline cases), HotAdd crash series (SIGKILL at 13 fault points), Differential tests against VMware reference, Fuzz targets (configuration, descriptors, paths, journal), Live lab test tiers (vSphere lab) (+4 more)

### Community 45 - "ABI Manifest Generation"
Cohesion: 0.14
Nodes (13): allowed_needed, functions, generation, links, max_glibc, reference, library, library_sha256 (+5 more)

### Community 46 - "Allocation Block Model"
Cohesion: 0.22
Nodes (9): Block, clipToChunks(), mergeBlocks(), blocksMiB(), TestClipToChunks(), TestClipToChunksEdges(), TestMergeBlocks(), modeLabel() (+1 more)

### Community 47 - "Gated Device Reader"
Cohesion: 0.22
Nodes (3): gatedReader, Device, Gate

### Community 48 - "HotAdd Candidate Selection"
Cohesion: 0.15
Nodes (9): HOTADD-0014 a second VM with the proxy BIOS UUID, HOTADD-0015 same disk opened by two processes, HOTADD-0024 administrative program on a lab worker, openvddk-admin journal, reconcile and cleanup recover orphaned attachments, HOTADD-0027 worker reset while a source disk is attached, Shared LVM PV UUID with a same-template source disk stops worker boot, HOTADD-0032 worker boots with a same-template source disk attached, LVM devices file naming own disk by ID, placed in initramfs, prevents duplicate-PV boot failure (+1 more)

### Community 49 - "Migratekit NBD Pipeline"
Cohesion: 0.19
Nodes (9): NBD-0022 NBDSSL and NBD through Migratekit pipeline, Migratekit pipeline with nbdkit vddk and nbdcopy, Reader VM without AES instructions, NBD-0023 NBDSSL without AES instructions, Log warning at Open when no AES instructions, Several NFC sessions per disk candidate, Read-ahead for sequential ReadAsync candidate, TLS 1.2 AES-128-GCM offer on CPU without AES (+1 more)

### Community 50 - "Registry and Locking"
Cohesion: 0.25
Nodes (7): Kind, Registry, FuzzDecode(), Decode(), Encode(), NewRegistry(), TestRejectsForeignValues()

### Community 51 - "Internal Package Map"
Cohesion: 0.17
Nodes (13): internal/hotadd attach/detach transaction and journal, internal/linuxdev SCSI/udev device correlation and block I/O, internal/vsphere govmomi session, snapshots, CBT, internal/readahead aligned parallel read-ahead, OpenVDDK 0.7.2 release notes, OpenVDDK 0.7.3 release notes, AES-128-GCM only offer on CPUs without AES instructions, Several NFC sessions per disk and VMware NFC keys honoured (+5 more)

### Community 52 - "Library Swap Test Kit"
Cohesion: 0.31
Nodes (11): Library swap test, vixcopy minimal C consumer, die(), fail(), field(), install_candidate(), inventory(), note() (+3 more)

### Community 53 - "VixDisk Info Helpers"
Cohesion: 0.22
Nodes (12): Info, GetInfo(), infoFrom(), infoFromChain(), infoFromChainErr(), FuzzInfoFromChain(), quietLog(), reader() (+4 more)

### Community 54 - "NBD Multi-Connection Limits"
Cohesion: 0.18
Nodes (8): NBD-0026 One or several connections from slow datastore, CloudStack built-in VMware import path, nbdkit multi-conn-mode and nbdcopy connections, NBD-0027 NFC sessions, buffers and read-ahead, BufSizeIn64KB buffer size key, 2 MiB x 16 buffers refused by host, 16-byte open-session message fields, Slow storage keys and sessions

### Community 55 - "Binary Kit and Worker Setup"
Cohesion: 0.17
Nodes (12): OpenVDDK binary kit README, Worker disk ID settings changed on first use, HotAdd worker VM requirements, Install via nbdkit libdir or file swap, Journal-based recovery after crash, Binary kit contents table, NBDSSL and NBD requirements, openvddk-admin recovery tool (+4 more)

### Community 56 - "govmomi Simulator Fixtures"
Cohesion: 0.21
Nodes (10): simulatorVMs(), TestLoginDetectsESXi(), firstDiskPath(), hexColon(), mustPort(), TestResolveRefusesIndependentDisk(), TestSessionsLeaveNoConnections(), TestThumbprintPinning() (+2 more)

### Community 57 - "NBD Open Error Codes"
Cohesion: 0.18
Nodes (7): nbdOpenCode(), TestNBDOpenCodeNoConnection(), CodeOf(), Code, errnoCode(), TestReadErrorCodes(), Error

### Community 59 - "Architecture and ABI Status"
Cohesion: 0.23
Nodes (11): Function status levels SUPPORTED PARTIAL PLANNED UNSUPPORTED-BY-DESIGN NOT-YET-INVESTIGATED, VixDiskLib 8.0.3 ABI (43 public functions), VixDiskLib_Create (NOT-YET-INVESTIGATED), VixDiskLib_GetConnectParams (PLANNED), VixDiskLib_InitEx, Developer kit examples (read-disk, disk-info, allocated-blocks, async-read), Developer guide (devkit/GUIDE.md), Developer kit README (+3 more)

### Community 60 - "Allocation Maps via NFC"
Cohesion: 0.18
Nodes (9): D-0035 Allocated blocks from vCenter, Allocation map from vCenter QueryChangedDiskAreas with change ID star, D-0036 Allocated blocks over NFC, Allocation query to the ESXi host over NFC, D-0037 NBD on main, HotAdd on branch, D-0039 Transport listing and fallback, Transports hotadd nbdssl nbd, fallback only within consumer list, D-0040 Four-reader NBD rate accepted (+1 more)

### Community 61 - "Release Check Matrices"
Cohesion: 0.20
Nodes (10): NBD-0030 Release checks of 0.7.3-rc1, 0.7.3-rc1 release check matrix, NBD-0031 Release checks of 0.7.4-rc1, CBT changed-area checks with expected hash, ESXi host removed from and re-added to vCenter, 0.7.4 release build aedcc19, Direct connection to standalone ESXi, Observation records index (+2 more)

### Community 62 - "NFC Service Fallback"
Cohesion: 0.33
Nodes (9): greetingListener(), internalContentAnswer(), TestNfcServiceFallback(), TestNfcTicketESXi(), TestNfcTicketUnknownServiceObject(), TestNfcTicketVCenter(), TestTicketWithoutThumbprintRefused(), ticketAnswer() (+1 more)

### Community 63 - "Contract and Governance Policies"
Cohesion: 0.20
Nodes (6): Public API compatibility ledger, OpenVDDK Normative Engineering Contract, Decision log (docs/decisions), Compatibility deviations from VDDK, Performance release gates, VixDiskLib C API

### Community 64 - "NBD Cipher and Fault Checks"
Cohesion: 0.20
Nodes (9): NBD-0025 Release checks of 0.7.2-rc1, Host refusing AES-128 offer test, Network faults during skipz read, skipz on Windows Server 2019 disk, virt-v2v -o null conversions as release check, NBD-0029 VDDK 8.0.3 rechecks on vSphere 6.7, HotAdd failed-Open error codes, virt-v2v conversions from vSphere 6.7 rechecked (+1 more)

### Community 65 - "IO Delivery Completion"
Cohesion: 0.18
Nodes (7): ioReadFull(), TestFailDuringDeliveryCompletesOnce(), FuzzParseAIOHeader(), FuzzReadLineRaw(), ParseAIOHeader(), readLineRaw(), skipZeros()

### Community 66 - "C/Go ABI Boundary"
Cohesion: 0.20
Nodes (7): cabi/exports.go cgo bridge, cabi/shim.c C ABI (43 exports), internal/core connection and disk objects, internal/handles encoded identifier registry, internal/lifecycle Init/InitEx/Exit state, internal/nfc NBD and NBDSSL protocol, internal/transport registry and fallback policy

### Community 67 - "Clean-Room Contribution Rules"
Cohesion: 0.27
Nodes (5): COMPATIBILITY.md ledger, docs/CLEAN-ROOM.md learning record, Source kinds used to learn reference behaviour, Technical evidence categories (CONTRACT section 50), Generated files and their generators

### Community 68 - "Consumer Callbacks and Config"
Cohesion: 0.20
Nodes (7): Consumer callbacks, OpenVDDK configuration namespace, Encoded-identifier handle registry, Log line format, Logging and message delivery, HotAdd read-ahead, Thread safety

### Community 69 - "NFC Sessions and Buffers"
Cohesion: 0.22
Nodes (5): D-0045 several NFC sessions per disk, D-0048 NFC buffers and async read-ahead, D-0049 more VMware documented configuration keys honoured, D-0051 OpenVDDK. key prefix documented, D-0052 direct connections to standalone ESXi

### Community 70 - "Init Lifecycle Observations"
Cohesion: 0.22
Nodes (5): LIFE-0001 Initialization lifecycle and pre-initialization behavior, ListTransportModes after Init returns file:san:hotadd:nbdssl:nbd, LOG-0001 External messages of reference and candidate in HotAdd workflows, Candidate log message inventory (LOG and WARN callbacks via logx), vCenter session events and client identification (VMware-client/8.0.3 vs govmomi default)

### Community 71 - "NFC Access Control"
Cohesion: 0.27
Nodes (7): NET-0001 Lab captures and access-control call basis, PrepareForAccess and EndAccess calls, NET-0002 Reference allocation query over NFC, AIO type 13 allocation query, Allocation bitmap read least significant bit first, NFC frame sequence on port 902, QueryAllocatedBlocks vCenter map fallback

### Community 72 - "Host Not-Connected Handling"
Cohesion: 0.33
Nodes (10): hostNotConnected(), fastRetry(), notConnectedTask(), TestHostNotConnectedDetected(), TestUntilHostConnectedGivesUpAtTheBound(), TestUntilHostConnectedRetriesThenSucceeds(), TestUntilHostConnectedSeesAnEarlierTryTakeEffect(), TestUntilHostConnectedStopsOnOtherErrors() (+2 more)

### Community 73 - "Vix Errors and Transports"
Cohesion: 0.25
Nodes (5): Vix error model, NBD transport, NBDSSL transport, NFC authentication and tickets, Read contract

### Community 74 - "Skipz Compression Observations"
Cohesion: 0.28
Nodes (8): Honour skipz compression candidate, NBD-0024 Migratekit full copies measured on the wire, Migratekit full copy received bytes, skipz reply piece encoding first capture, NET-0004 Reads with zeros left out (skipz) over NFC, skipz code 3 piece encoding, skipz read request code 3, Strict skipz decoding in 0.7.2 candidate

### Community 75 - "Trace Diff Tooling"
Cohesion: 0.44
Nodes (8): readKey, readVal, trace, cmdTraceDiff(), compareTraces(), diffLines(), parseTrace(), TestTraceDiff()

### Community 76 - "Contributing and DCO"
Cohesion: 0.29
Nodes (6): VixDiskLib_Write (UNSUPPORTED-BY-DESIGN), Developer Certificate of Origin sign-off, Licence headers on new source files, Pull request rules (one topic, template, maintainer merges), Pull request template and checklist, Private vulnerability reporting process

### Community 77 - "ABI Artifacts and Build Container"
Cohesion: 0.29
Nodes (7): ABI manifest, ABI artifact naming and SONAME, Binary kit (evalkit), Pinned AlmaLinux 8 build container, Developer kit (devkit), Reproducible builds, Symbol and ABI gate

### Community 78 - "Changed Block Tracking"
Cohesion: 0.29
Nodes (6): Changed Block Tracking, Migration application (first normative consumer), QueryAllocatedBlocks, Release maturity levels, Version 1.0 minimum production requirements, Warm migration contract

### Community 79 - "HotAdd Source Disk Writes"
Cohesion: 0.32
Nodes (7): HOTADD-0035 thick eager-zeroed source on VMFS and disk-changing functions, Reference accepts writes over read-write HotAdd that never reach the source, Reference reads remote disk metadata; candidate answered VIX_E_NOT_SUPPORTED, HOTADD-0037 GetMetadataKeys and ReadMetadata, disksignature key derived from MBR disk signature bytes 440-443, GetMetadataKeys and ReadMetadata output format and error codes, 0.6.24 metadata equals VDDK 8.0.3; VDDK 7.0.3 adds bios geometry keys

### Community 80 - "Parent Path Parsing"
Cohesion: 0.29
Nodes (7): parentPath(), FuzzParentPath(), TestParentPath(), buildMetadata(), TestBuildMetadata(), TestMetadataKeyList(), TestMetadataLeavesOutSESparseGrain()

### Community 81 - "UUID Parsing"
Cohesion: 0.38
Nodes (7): guestDevice(), FuzzUUIDs(), formatUUID(), parseUUID(), SMBIOSToVSphereUUID(), TestUUIDConversions(), WWIDForBackingUUID()

### Community 82 - "Clean-Room Implementation Policy"
Cohesion: 0.29
Nodes (5): Clean published tree, Apache-2.0 license, Observation records, Broadcom VDDK 8.0.3 reference oracle, vSphere target matrix

### Community 83 - "NFC Timeout Configuration"
Cohesion: 0.33
Nodes (6): NBD-0028 VMware NFC configuration keys observed, nfc ReadTimeoutMs and RequestTimeoutMs keys, Socket options AIO type 9 message, tmpDirectory writes no file during reads, Lost NFC connection during read returns 14009, OpenVDDK configuration keys

### Community 85 - "Independent Disk Reads"
Cohesion: 0.47
Nodes (5): HOTADD-0051 independent disks and raw device mappings over every transport, main reads independent disks over NBD and NBDSSL, even at a snapshot where live data is returned, Virtual-mode RDM attached over HotAdd as independent_nonpersistent (dev15), HOTADD-0052 0.6.26 checked before release, 0.6.26 carries HotAdd security review fixes and an SBOM

### Community 86 - "IO Gate Behavior"
Cohesion: 0.53
Nodes (5): New(), TestClosedDeviceIgnored(), TestHoldDrainsAndLimits(), TestHoldTimesOut(), TestNoHoldNoLimit()

### Community 87 - "HotAdd Negative Cases"
Cohesion: 0.40
Nodes (4): HOTADD-0021 negative and failure cases, reference vs candidate, Guest device list taken before slot lock caused concurrent attach race, HOTADD-0028 virt-v2v VDDK input mode, virt-v2v default mode HotAdd of powered-off VM disks without snapshot works after 0.6.13

### Community 88 - "NFC Reads Over TLS"
Cohesion: 0.50
Nodes (3): NET-0003 Reference NBD read over NFC, Descriptor keys AIO type 11, Read AIO type 7 44-byte structure

### Community 89 - "HCTL Device Parsing"
Cohesion: 0.40
Nodes (4): FuzzParseHCTL(), ParseHCTL(), TestParseHCTL(), HCTL

### Community 90 - "Selftest Shell Helpers"
Cohesion: 0.60
Nodes (3): bad(), ok(), selftest.sh script

### Community 93 - "Logging Decisions"
Cohesion: 0.50
Nodes (3): D-0021 Log line format, D-0022 Messages without callbacks, Own log file when no callback takes a message

### Community 94 - "HotAdd Attach Time"
Cohesion: 0.83
Nodes (3): HOTADD-0034 attach time with ten disks being read, Attach time grows with disks already being read, ESXi reconfigure slows as more I/O is in flight on the worker disks

### Community 95 - "HotAdd NFS Placement"
Cohesion: 0.83
Nodes (3): HOTADD-0053 source VM on one ESXi host, worker on another (B6), NFS 4.1 gives no stun and no lock files with the worker on either host, NFS v3 lock timeout stuns the source VM at snapshot removal when worker is on another host

### Community 96 - "HotAdd Read Throughput"
Cohesion: 0.67
Nodes (3): HOTADD-0055 reads over HotAdd from delayed storage: threads, read size, read-ahead, Several threads on one HotAdd handle return correct data with both libraries, Several threads and larger reads raise throughput on delayed storage

### Community 97 - "Transport List Observations"
Cohesion: 0.67
Nodes (3): NBD-0019 Transport lists that name file or san, NBD-0020 Migratekit VMware to OpenStack migration with OpenVDDK, Migratekit full, incremental and cutover migration of Debian VM into Cinder with OpenVDDK

### Community 98 - "HotAdd Crash Script"
Cohesion: 1.00
Nodes (3): inventory(), settle(), hotadd-crash.sh script

### Community 99 - "HotAdd Observe Script"
Cohesion: 0.83
Nodes (3): inventory(), hotadd-observe.sh script, stamp()

## Ambiguous Edges - Review These
- `Killed reader leaves attachment; library Cleanup removes it` → `0.6.24 Cleanup fails after a killed reader and the disk stays attached`  [AMBIGUOUS]
  docs/observations/HOTADD-0049-robustness-and-identification-fix.md · relation: conceptually_related_to

## Knowledge Gaps
- **160 isolated node(s):** `github.com/openvddk/openvddk`, `VixDiskLib C API`, `HotAdd cleanup`, `Read contract`, `Log line format` (+155 more)
  These have ≤1 connection - possible missing edges or undocumented components. (Counts symbols only; 411 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **43 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `fakeHost` connect `TLS and NBD Sessions` to `Go Admin Bundle and Journal`, `Disk Allocation Accounting`, `Journal and Attachment Tests`, `IO Delivery Completion`?**
  _High betweenness centrality (0.009) - this node is a cross-community bridge._
- **Are the 37 inferred relationships involving `Open()` (e.g. with `.abandon()` and `.rollback()`) actually correct?**
  _`Open()` has 37 INFERRED edges - model-reasoned connections that need verification._
- **What connects `github.com/openvddk/openvddk`, `VixDiskLib C API`, `HotAdd cleanup` to the rest of the system?**
  _160 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Go Admin Bundle and Journal` be split into smaller, more focused modules?**
  _Cohesion score 0.05951758209822726 - nodes in this community are weakly interconnected._
- **Why does `Platform` connect `govmomi vSphere Objects` to `Go Admin Bundle and Journal`, `govmomi VM Controllers`, `Bundle Redaction Tests`, `Connection Lifecycle`, `govmomi Task Fakes`?**
  _High betweenness centrality (0.008) - this node is a cross-community bridge._
- **Should `Go Config Collection` be split into smaller, more focused modules?**
  _Cohesion score 0.05555555555555555 - nodes in this community are weakly interconnected._

### Low-confidence Hints
_AMBIGUOUS edges — the extractor was unsure. Verify before acting on these._

- **What is the exact relationship between `Killed reader leaves attachment; library Cleanup removes it` and `0.6.24 Cleanup fails after a killed reader and the disk stays attached`?**
  _Edge tagged AMBIGUOUS (relation: conceptually_related_to) - confidence is low._