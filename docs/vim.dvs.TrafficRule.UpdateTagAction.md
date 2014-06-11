vim.dvs.TrafficRule.UpdateTagAction
===================================
inherits from [vim.dvs.TrafficRule.Action](docs/vim.dvs.TrafficRule.Action.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines network rule action to tag packets(qos,dscp) or    clear tags(clear qos, dscp tags) on packets.    One or both of qos and dscp may be specified.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| qosTag | int | true | None | QOS tag. IEEE 802.1p supports 3 bit Priority Code Point (PCP).    The valid values are between 0-7. Please refer the IEEE 802.1p    documentation for more details about what each value represents.    If qosTag is set to 0 then the tag on the packets will be cleared. |
| dscpTag | int | true | None | DSCP tag. The valid values for DSCP tag can be found in    'Differentiated Services Field Codepoints' section of IANA website.    The information can also be got from reading all of the below RFC:    RFC 2474, RFC 2597, RFC 3246, RFC 5865.    If the dscpTag is set to 0 then the dscp tag on packets will be cleared. |


