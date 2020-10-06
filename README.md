# ansible-truenas

Ansible module for configuring TrueNAS (Enterprise and Core) 12+ via v2.0 API. Requires API key to be setup in TrueNAS beforehand. Does not currently support TrueNAS 11, FreeNAS, or user-based authentication. Please note that the following totals don't directly correlate to project progress. The module builds on top of the API in an idempotent fashion, so one play may use multiple API commands. This is more of an estimation of how usable the module is.

Currently implemented from https://www.truenas.com/docs/hub/additional-topics/api/rest_api.html:

:negative_squared_cross_mark: AcmeDnsAuthenticator: 0/6

:negative_squared_cross_mark: Activedirectory: 0/9

:negative_squared_cross_mark: Afp: 0/3

:negative_squared_cross_mark: Alert: 0/5

:negative_squared_cross_mark: AlertClasses: 0/2

:negative_squared_cross_mark: AlertService: 0/7

:negative_squared_cross_mark: ApiKey: 0/5

:negative_squared_cross_mark: Auth: 0/4

:negative_squared_cross_mark: AuthTwoFactor: 0/5

:negative_squared_cross_mark: Boot: 0/8

:negative_squared_cross_mark: BootEnv: 0/7

:negative_squared_cross_mark: Certificate: 0/11

:negative_squared_cross_mark: CertificateAuthority: 0/7

:negative_squared_cross_mark: Cloudsync: 0/14

:negative_squared_cross_mark: CloudsyncCredentials: 0/6

:negative_squared_cross_mark: Config: 0/1

:negative_squared_cross_mark: Core: 0/14

:negative_squared_cross_mark: Cronjob: 0/6

:negative_squared_cross_mark: Device: 0/1

:negative_squared_cross_mark: Disk: 0/13

:negative_squared_cross_mark: Dns: 0/1

:negative_squared_cross_mark: DynDns: 0/3

:negative_squared_cross_mark: Ec2: 0/5

:negative_squared_cross_mark: Enclosure: 0/4

:negative_squared_cross_mark: Failover: 0/15

:negative_squared_cross_mark: Fcport: 0/3

:negative_squared_cross_mark: Filesystem: 0/10

:negative_squared_cross_mark: Ftp: 0/2

:negative_squared_cross_mark: Group: 0/7

:negative_squared_cross_mark: Idmap: 0/9

:negative_squared_cross_mark: Initshutdownscript: 0/5

:negative_squared_cross_mark: Interface: 0/17

:negative_squared_cross_mark: Ipmi: 0/6

:negative_squared_cross_mark: IscsiAuth: 0/5

:negative_squared_cross_mark: IscsiExtent: 0/6

:negative_squared_cross_mark: IscsiGlobal: 0/4

:negative_squared_cross_mark: IscsiIinitiator: 0/5

:negative_squared_cross_mark: IscsiPortal: 0/5

:negative_squared_cross_mark: IscsiTargetExtent: 0/5

:negative_squared_cross_mark: Jail: 0/23

:negative_squared_cross_mark: Kerberos: 0/2

:negative_squared_cross_mark: KerberosKeytab: 0/6

:negative_squared_cross_mark: KerberosRealm: 0/5

:negative_squared_cross_mark: KeychainCredential: 0/9

:negative_squared_cross_mark: Kmip: 0/5

:negative_squared_cross_mark: Ldap: 0/5

:negative_squared_cross_mark: Lldp: 0/3

:negative_squared_cross_mark: Mail: 0/3

:negative_squared_cross_mark: Multipath: 0/2

:negative_squared_cross_mark: NetworkConfiguration: 0/2

:negative_squared_cross_mark: NetworkGeneral: 0/1

:negative_squared_cross_mark: Nfs: 0/3

:negative_squared_cross_mark: OpenvpnClient: 0/4

:negative_squared_cross_mark: OpenvpnServer: 0/6

:negative_squared_cross_mark: Plugin: 0/10

:negative_squared_cross_mark: Pool: 0/31

:negative_squared_cross_mark: PoolDataset: 0/18

:negative_squared_cross_mark: PoolDatasetUserprop: 0/5

:negative_squared_cross_mark: PoolResilver: 0/2

:negative_squared_cross_mark: PoolScrub: 0/6

:negative_squared_cross_mark: PoolSnapshottask: 0/6

:negative_squared_cross_mark: Replication: 0/12

:negative_squared_cross_mark: Reporting: 0/4

:negative_squared_cross_mark: Route: 0/2

:negative_squared_cross_mark: Rsyncd: 0/2

:negative_squared_cross_mark: Rsyncmod: 0/5

:negative_squared_cross_mark: Rsynctask: 0/6

:negative_squared_cross_mark: S3: 0/3

:negative_squared_cross_mark: Sensor: 0/1

:negative_squared_cross_mark: Service: 0/9

:negative_squared_cross_mark: Sharing: 0/2

:negative_squared_cross_mark: SharingAfp: 0/5

:negative_squared_cross_mark: SharingNfs: 0/6

:negative_squared_cross_mark: SharingSmb: 0/6

:negative_squared_cross_mark: SharingWebdav: 0/5

:negative_squared_cross_mark: Smart: 0/2

:negative_squared_cross_mark: Smarttest: 0/7

:negative_squared_cross_mark: Smb: 0/7

:negative_squared_cross_mark: SmbSharesec: 0/7

:negative_squared_cross_mark: Snmp: 0/2

:negative_squared_cross_mark: Ssh: 0/3

:negative_squared_cross_mark: Staticroute: 0/5

:negative_squared_cross_mark: Stats: 0/3

:negative_squared_cross_mark: Support: 0/7

:negative_squared_cross_mark: System: 0/13

:negative_squared_cross_mark: SystemAdvanced: 0/4

:negative_squared_cross_mark: SystemGeneral: 0/12

:negative_squared_cross_mark: SystemNtpserver: 0/6

:negative_squared_cross_mark: SystemDataset: 0/2

:negative_squared_cross_mark: Taskpath: 0/2

:negative_squared_cross_mark: Tftp: 0/2

:negative_squared_cross_mark: Truecommand: 0/2

:negative_squared_cross_mark: Truenas: 0/8

:negative_squared_cross_mark: Tunable: 0/6

:negative_squared_cross_mark: Update: 0/9

:negative_squared_cross_mark: Ups: 0/4

:negative_squared_cross_mark: User: 0/11

:negative_squared_cross_mark: Vm: 0/23

:negative_squared_cross_mark: VmDevice: 0/10

:negative_squared_cross_mark: Vmware: 0/9

:negative_squared_cross_mark: Webdav: 0/2

:negative_squared_cross_mark: WebuiImage: 0/3

:negative_squared_cross_mark: ZfsSnapshot: 0/7




:heavy_check_mark: - Completed

:warning: - In-progress

:negative_squared_cross_mark: - Not started