project('curl', 'c', license:'curl')

cc = meson.get_compiler('c')

lib_curl_deps = []

curl_sources = [
 'src/slist_wc.c',
 'src/tool_binmode.c',
 'src/tool_bname.c',
 'src/tool_cb_dbg.c',
 'src/tool_cb_hdr.c',
 'src/tool_cb_prg.c',
 'src/tool_cb_rea.c',
 'src/tool_cb_see.c',
 'src/tool_cb_wrt.c',
 'src/tool_cfgable.c',
 'src/tool_convert.c',
 'src/tool_dirhie.c',
 'src/tool_doswin.c',
 'src/tool_easysrc.c',
 'src/tool_filetime.c',
 'src/tool_formparse.c',
 'src/tool_getparam.c',
 'src/tool_getpass.c',
 'src/tool_help.c',
 'src/tool_helpers.c',
 'src/tool_hugehelp.c',
 'src/tool_homedir.c',
 'src/tool_libinfo.c',
 'src/tool_main.c',
 'src/tool_metalink.c',
 'src/tool_msgs.c',
 'src/tool_operate.c',
 'src/tool_operhlp.c',
 'src/tool_panykey.c',
 'src/tool_paramhlp.c',
 'src/tool_parsecfg.c',
 'src/tool_setopt.c',
 'src/tool_sleep.c',
 'src/tool_strdup.c',
 'src/tool_urlglob.c',
 'src/tool_util.c',
 'src/tool_vms.c',
 'src/tool_writeout.c',
 'src/tool_xattr.c',

 'lib/strtoofft.c',
 'lib/nonblock.c',
 'lib/warnless.c',
 'lib/curl_ctype.c'
]

libcurl_sources = [
 'lib/amigaos.c',
 'lib/asyn-ares.c',
 'lib/asyn-thread.c',
 'lib/base64.c',
 'lib/conncache.c',
 'lib/connect.c',
 'lib/content_encoding.c',
 'lib/cookie.c',
 'lib/curl_addrinfo.c',
 'lib/curl_ctype.c',
 'lib/curl_des.c',
 'lib/curl_endian.c',
 'lib/curl_fnmatch.c',
 'lib/curl_gethostname.c',
 'lib/curl_gssapi.c',
 'lib/curl_memrchr.c',
 'lib/curl_multibyte.c',
 'lib/curl_ntlm_core.c',
 'lib/curl_ntlm_wb.c',
 'lib/curl_path.c',
 'lib/curl_range.c',
 'lib/curl_rtmp.c',
 'lib/curl_sasl.c',
 'lib/curl_sspi.c',
 'lib/curl_threads.c',
 'lib/dict.c',
 'lib/doh.c',
 'lib/dotdot.c',
 'lib/easy.c',
 'lib/escape.c',
 'lib/file.c',
 'lib/fileinfo.c',
 'lib/formdata.c',
 'lib/ftp.c',
 'lib/ftplistparser.c',
 'lib/getenv.c',
 'lib/getinfo.c',
 'lib/gopher.c',
 'lib/hash.c',
 'lib/hmac.c',
 'lib/hostasyn.c',
 'lib/hostcheck.c',
 'lib/hostip.c',
 'lib/hostip4.c',
 'lib/hostip6.c',
 'lib/hostsyn.c',
 'lib/http.c',
 'lib/http2.c',
 'lib/http_chunks.c',
 'lib/http_digest.c',
 'lib/http_negotiate.c',
 'lib/http_ntlm.c',
 'lib/http_proxy.c',
 'lib/idn_win32.c',
 'lib/if2ip.c',
 'lib/imap.c',
 'lib/inet_ntop.c',
 'lib/inet_pton.c',
 'lib/krb5.c',
 'lib/ldap.c',
 'lib/llist.c',
 'lib/md4.c',
 'lib/md5.c',
 'lib/memdebug.c',
 'lib/mime.c',
 'lib/mprintf.c',
 'lib/multi.c',
 'lib/netrc.c',
 'lib/nonblock.c',
 'lib/non-ascii.c',
 'lib/nwlib.c',
 'lib/nwos.c',
 'lib/openldap.c',
 'lib/parsedate.c',
 'lib/pingpong.c',
 'lib/pipeline.c',
 'lib/pop3.c',
 'lib/progress.c',
 'lib/psl.c',
 'lib/rand.c',
 'lib/rtsp.c',
 'lib/security.c',
 'lib/select.c',
 'lib/sendf.c',
 'lib/setopt.c',
 'lib/sha256.c',
 'lib/share.c',
 'lib/slist.c',
 'lib/smb.c',
 'lib/smtp.c',
 'lib/socks.c',
 'lib/socks_gssapi.c',
 'lib/socks_sspi.c',
 'lib/speedcheck.c',
 'lib/splay.c',
 'lib/ssh.c',
 'lib/ssh-libssh.c',
 'lib/strcase.c',
 'lib/strdup.c',
 'lib/strerror.c',
 'lib/strtok.c',
 'lib/strtoofft.c',
 'lib/system_win32.c',
 'lib/telnet.c',
 'lib/tftp.c',
 'lib/timeval.c',
 'lib/transfer.c',
 'lib/url.c',
 'lib/urlapi.c',
 'lib/version.c',
 'lib/warnless.c',
 'lib/wildcard.c',
 'lib/x509asn1.c',

 'lib/vauth/cleartext.c',
 'lib/vauth/cram.c',
 'lib/vauth/digest.c',
 'lib/vauth/digest_sspi.c',
 'lib/vauth/krb5_gssapi.c',
 'lib/vauth/krb5_sspi.c',
 'lib/vauth/ntlm.c',
 'lib/vauth/ntlm_sspi.c',
 'lib/vauth/oauth2.c',
 'lib/vauth/spnego_gssapi.c',
 'lib/vauth/spnego_sspi.c',
 'lib/vauth/vauth.c',

 'lib/vtls/cyassl.c',
 'lib/vtls/darwinssl.c',
 'lib/vtls/gskit.c',
 'lib/vtls/gtls.c',
 'lib/vtls/mbedtls.c',
 'lib/vtls/mesalink.c',
 'lib/vtls/nss.c',
 'lib/vtls/openssl.c',
 'lib/vtls/polarssl.c',
 'lib/vtls/polarssl_threadlock.c',
 'lib/vtls/schannel.c',
 'lib/vtls/schannel_verify.c',
 'lib/vtls/vtls.c'

 ]

inc = include_directories('include', 'lib')

conf_data = configuration_data()
conf_data.set('BUILDING_LIBCURL', '1')
conf_data.set('CURL_CA_BUNDLE','"auto"')
conf_data.set('HAVE_LONGLONG', '1')
conf_data.set_quoted('OS', host_machine.system())

conf_data.set('HAVE_STRUCT_TIMEVAL', cc.has_type('struct timeval', prefix : '''#include<time.h>
#include<sys/time.h>
'''))

conf_data.set('HAVE_BOOL_T', cc.has_type('bool', prefix : '''
#include <sys/types.h>
#include <stdbool.h>
'''))

if host_machine.system() == 'linux' or host_machine.system() == 'darwin'
    send_recv_types = ['int', 'void*', 'size_t', 'int', 'ssize_t', 'const']
    conf_data.set('HAVE_RECV', '1')
    conf_data.set('HAVE_SEND', '1')
    res = cc.run('''
    #include <sys/types.h>
    #include <unistd.h>
    #include <fcntl.h>
    int
    main ()
    {
          /* O_NONBLOCK source test */
          int flags = 0;
          if(0 != fcntl(0, F_SETFL, flags | O_NONBLOCK))
	      return 1;
          return 0;
    }
    ''')
    if res.compiled() and res.returncode() == 0
      conf_data.set('HAVE_FCNTL_O_NONBLOCK','1')
    endif
elif host_machine.system() == 'windows'
    send_recv_types = ['SOCKET', 'char *', 'int', 'int', 'int', 'const']
    conf_data.set('HAVE_RECV', '1')
    conf_data.set('HAVE_SEND', '1')
endif

foreach function:['RECV','SEND']
    foreach arg:[1,2,3,4]
        conf_data.set('@0@_TYPE_ARG@1@'.format(function,arg),send_recv_types[arg])
    endforeach
    conf_data.set('@0@_TYPE_RETV'.format(function),send_recv_types[4])
endforeach
conf_data.set('SEND_QUAL_ARG2',send_recv_types[5])


headers = {
	'HAVE_ALLOCA_H':'alloca.h',
	'HAVE_ARPA_INET_H':'arpa/inet.h',
	'HAVE_ARPA_TFTP_H':'arpa/tftp.h',
	'HAVE_ASSERT_H':'assert.h',
	'HAVE_CRYPTO_H':'crypto.h',
	'HAVE_DES_H':'des.h',
	'HAVE_DLFCN_H':'dlfcn.h',
	'HAVE_ERRNO_H':'errno.h',
	'HAVE_ERR_H':'err.h',
	'HAVE_FCNTL_H':'fcntl.h',
	'HAVE_GSSAPI_GSSAPI_GENERIC_H':'gssapi/gssapi_generic.h',
	'HAVE_GSSAPI_GSSAPI_H':'gssapi/gssapi.h',
	'HAVE_GSSAPI_GSSAPI_KRB5_H':'gssapi/gssapi_krb5.h',
	'HAVE_IDN_FREE_H':'idn-free.h',
	'HAVE_IFADDRS_H':'ifaddrs.h',
	'HAVE_INTTYPES_H':'inttypes.h',
	'HAVE_IO_H':'io.h',
	'HAVE_KRB_H':'krb.h',
	'HAVE_LBER_H':'lber.h',
	'HAVE_LDAPSSL_H':'ldapssl.h',
	'HAVE_LDAP_H':'ldap.h',
	'HAVE_LDAP_SSL_H':'ldap_ssl.h',
	'HAVE_LIBGEN_H':'libgen.h',
	'HAVE_LIBSSH2_H':'libssh2.h',
	'HAVE_LOCALE_H':'locale.h',
	'HAVE_MALLOC_H':'malloc.h',
	'HAVE_MEMORY_H':'memory.h',
	'HAVE_NETDB_H':'netdb.h',
	'HAVE_NETINET_IN_H':'netinet/in.h',
	'HAVE_NETINET_TCP_H':'netinet/tcp.h',
	'HAVE_NET_IF_H':'net/if.h',
	'HAVE_OPENSSL_CRYPTO_H':'openssl/crypto.h',
	'HAVE_OPENSSL_ENGINE_H':'openssl/engine.h',
	'HAVE_OPENSSL_ERR_H':'openssl/err.h',
	'HAVE_OPENSSL_PEM_H':'openssl/pem.h',
	'HAVE_OPENSSL_PKCS12_H':'openssl/pkcs12.h',
	'HAVE_OPENSSL_RSA_H':'openssl/rsa.h',
	'HAVE_OPENSSL_SSL_H':'openssl/ssl.h',
	'HAVE_OPENSSL_X509_H':'openssl/x509.h',
	'HAVE_PEM_H':'pem.h',
	'HAVE_POLL_H':'poll.h',
	'HAVE_PTHREAD_H':'pthread.h',
	'HAVE_PWD_H':'pwd.h',
	'HAVE_RSA_H':'rsa.h',
	'HAVE_SETJMP_H':'setjmp.h',
	'HAVE_SGTTY_H':'sgtty.h',
	'HAVE_SSL_H':'ssl.h',
	'HAVE_STDBOOL_H':'stdbool.h',
	'HAVE_STDINT_H':'stdint.h',
	'HAVE_STDIO_H':'stdio.h',
	'HAVE_STDLIB_H':'stdlib.h',
	'HAVE_STRINGS_H':'strings.h',
	'HAVE_STRING_H':'string.h',
	'HAVE_SYS_FILIO_H':'sys/filio.h',
	'HAVE_SYS_IOCTL_H':'sys/ioctl.h',
	'HAVE_SYS_PARAM_H':'sys/param.h',
	'HAVE_SYS_POLL_H':'sys/poll.h',
	'HAVE_SYS_RESOURCE_H':'sys/resource.h',
	'HAVE_SYS_SELECT_H':'sys/select.h',
	'HAVE_SYS_SOCKET_H':'sys/socket.h',
	'HAVE_SYS_SOCKIO_H':'sys/sockio.h',
	'HAVE_SYS_STAT_H':'sys/stat.h',
	'HAVE_SYS_TIME_H':'sys/time.h',
	'HAVE_SYS_TYPES_H':'sys/types.h',
	'HAVE_SYS_UIO_H':'sys/uio.h',
	'HAVE_SYS_UN_H':'sys/un.h',
	'HAVE_SYS_UTIME_H':'sys/utime.h',
	'HAVE_TERMIOS_H':'termios.h',
	'HAVE_TERMIO_H':'termio.h',
	'HAVE_TIME_H':'time.h',
	'HAVE_TLD_H':'tld.h',
	'HAVE_UNISTD_H':'unistd.h',
	'HAVE_UTIME_H':'utime.h',
	'HAVE_WINBER_H':'winber.h',
	'HAVE_WINDOWS_H':'windows.h',
	'HAVE_WINLDAP_H':'winldap.h',
	'HAVE_WINSOCK2_H':'winsock2.h',
	'HAVE_WINSOCK_H':'winsock.h',
	'HAVE_WS2TCPIP_H':'ws2tcpip.h',
	'HAVE_X509_H':'x509.h',
	'HAVE_PROCESS_H':'process.h',
	'HAVE_ZLIB_H':'zlib.h'
	}

foreach flag,header:headers
    if cc.has_header(header)
    	conf_data.set(flag, '1')
    endif
endforeach

functions = [
  ['alarm', '#include <unistd.h>', 'HAVE_ALARM'],
  ['basename', '#include <libgen.h>', 'HAVE_BASENAME'],
  ['__builtin_available', '', 'HAVE_BUILTIN_AVAILABLE'],
  ['clock_gettime','#include <time.h>','HAVE_CLOCK_GETTIME_MONOTONIC'],
  ['closesocket','#include <winsock.h>','HAVE_CLOSESOCKET'],
  ['poll','#include <sys/poll.h>','HAVE_POLL_FINE'],
  ['socket','#include <sys/socket.h>','HAVE_SOCKET']
]

foreach function:functions
  if cc.has_function(function[0], prefix : function[1])
    conf_data.set(function[2], 1)
  endif
endforeach

foreach type:['short', 'long', 'int', 'curl_off_t', 'size_t']
    conf_data.set('SIZEOF_@0@'.format(type.to_upper()), cc.sizeof(type, prefix: '#include "@0@/include/curl/system.h"'.format(meson.current_source_dir())))
endforeach

if get_option('CURL_DISABLE_LDAP')
  conf_data.set('CURL_DISABLE_LDAP','1')
else
  lib_curl_deps = lib_curl_deps + [cc.find_library('ldap')]
  lib_curl_deps = lib_curl_deps + [cc.find_library('lber')]
endif

configure_file(output : 'curl_config.h',
               configuration : conf_data)


libcurl = library('curl', libcurl_sources,
                   include_directories:inc,
                   c_args:['-DBUILDING_LIBCURL', '-DHAVE_CONFIG_H'],
                   dependencies: lib_curl_deps
                   )

libcurl_dep = declare_dependency(
                                link_with:libcurl,
                                include_directories:inc
                                )


curl = executable('curl', curl_sources,
                  dependencies: libcurl_dep,
                  c_args:['-DHAVE_CONFIG_H'],
                )