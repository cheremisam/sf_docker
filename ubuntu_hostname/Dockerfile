FROM ubuntu:20.10 as builder

FROM scratch
COPY --from=builder /lib/x86_64-linux-gnu/libc.so.6 /lib/x86_64-linux-gnu/
COPY --from=builder /lib64/ld-linux-x86-64.so.2 /lib64/
COPY --from=builder /bin/hostname /bin/sh /bin/
CMD /bin/hostname


