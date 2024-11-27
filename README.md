(self.webpackChunk_N_E = self.webpackChunk_N_E || []).push([[57], {
    83987: function(e, t, n) {
        Promise.resolve().then(n.bind(n, 14207))
    },
    57958: function(e, t, n) {
        var a = n(76392).Symbol;
        e.exports = a
    },
    28681: function(e, t, n) {
        var a = n(57958)
          , r = n(74473)
          , i = n(40915)
          , s = a ? a.toStringTag : void 0;
        e.exports = function(e) {
            return null == e ? void 0 === e ? "[object Undefined]" : "[object Null]" : s && s in Object(e) ? r(e) : i(e)
        }
    },
    74113: function(e, t, n) {
        var a = n(44815)
          , r = /^\s+/;
        e.exports = function(e) {
            return e ? e.slice(0, a(e) + 1).replace(r, "") : e
        }
    },
    49908: function(e, t, n) {
        var a = "object" == typeof n.g && n.g && n.g.Object === Object && n.g;
        e.exports = a
    },
    74473: function(e, t, n) {
        var a = n(57958)
          , r = Object.prototype
          , i = r.hasOwnProperty
          , s = r.toString
          , o = a ? a.toStringTag : void 0;
        e.exports = function(e) {
            var t = i.call(e, o)
              , n = e[o];
            try {
                e[o] = void 0;
                var a = !0
            } catch (e) {}
            var r = s.call(e);
            return a && (t ? e[o] = n : delete e[o]),
            r
        }
    },
    40915: function(e) {
        var t = Object.prototype.toString;
        e.exports = function(e) {
            return t.call(e)
        }
    },
    76392: function(e, t, n) {
        var a = n(49908)
          , r = "object" == typeof self && self && self.Object === Object && self
          , i = a || r || Function("return this")();
        e.exports = i
    },
    44815: function(e) {
        var t = /\s/;
        e.exports = function(e) {
            for (var n = e.length; n-- && t.test(e.charAt(n)); )
                ;
            return n
        }
    },
    47652: function(e, t, n) {
        var a = n(30983)
          , r = n(49530)
          , i = n(62141)
          , s = Math.max
          , o = Math.min;
        e.exports = function(e, t, n) {
            var l, u, d, p, c, y, m = 0, f = !1, b = !1, h = !0;
            if ("function" != typeof e)
                throw TypeError("Expected a function");
            function x(t) {
                var n = l
                  , a = u;
                return l = u = void 0,
                m = t,
                p = e.apply(a, n)
            }
            function g(e) {
                var n = e - y
                  , a = e - m;
                return void 0 === y || n >= t || n < 0 || b && a >= d
            }
            function v() {
                var e, n, a, i = r();
                if (g(i))
                    return T(i);
                c = setTimeout(v, (e = i - y,
                n = i - m,
                a = t - e,
                b ? o(a, d - n) : a))
            }
            function T(e) {
                return (c = void 0,
                h && l) ? x(e) : (l = u = void 0,
                p)
            }
            function w() {
                var e, n = r(), a = g(n);
                if (l = arguments,
                u = this,
                y = n,
                a) {
                    if (void 0 === c)
                        return m = e = y,
                        c = setTimeout(v, t),
                        f ? x(e) : p;
                    if (b)
                        return clearTimeout(c),
                        c = setTimeout(v, t),
                        x(y)
                }
                return void 0 === c && (c = setTimeout(v, t)),
                p
            }
            return t = i(t) || 0,
            a(n) && (f = !!n.leading,
            d = (b = "maxWait"in n) ? s(i(n.maxWait) || 0, t) : d,
            h = "trailing"in n ? !!n.trailing : h),
            w.cancel = function() {
                void 0 !== c && clearTimeout(c),
                m = 0,
                l = y = u = c = void 0
            }
            ,
            w.flush = function() {
                return void 0 === c ? p : T(r())
            }
            ,
            w
        }
    },
    30983: function(e) {
        e.exports = function(e) {
            var t = typeof e;
            return null != e && ("object" == t || "function" == t)
        }
    },
    41857: function(e) {
        e.exports = function(e) {
            return null != e && "object" == typeof e
        }
    },
    8863: function(e, t, n) {
        var a = n(28681)
          , r = n(41857);
        e.exports = function(e) {
            return "symbol" == typeof e || r(e) && "[object Symbol]" == a(e)
        }
    },
    49530: function(e, t, n) {
        var a = n(76392);
        e.exports = function() {
            return a.Date.now()
        }
    },
    62141: function(e, t, n) {
        var a = n(74113)
          , r = n(30983)
          , i = n(8863)
          , s = 0 / 0
          , o = /^[-+]0x[0-9a-f]+$/i
          , l = /^0b[01]+$/i
          , u = /^0o[0-7]+$/i
          , d = parseInt;
        e.exports = function(e) {
            if ("number" == typeof e)
                return e;
            if (i(e))
                return s;
            if (r(e)) {
                var t = "function" == typeof e.valueOf ? e.valueOf() : e;
                e = r(t) ? t + "" : t
            }
            if ("string" != typeof e)
                return 0 === e ? e : +e;
            e = a(e);
            var n = l.test(e);
            return n || u.test(e) ? d(e.slice(2), n ? 2 : 8) : o.test(e) ? s : +e
        }
    },
    14207: function(e, t, n) {
        "use strict";
        n.r(t),
        n.d(t, {
            default: function() {
                return L
            }
        });
        var a = n(40733);
        let r = [{
            inputs: [{
                internalType: "address",
                name: "ipAssetRegistry",
                type: "address"
            }, {
                internalType: "address",
                name: "licensingModule",
                type: "address"
            }, {
                internalType: "address",
                name: "coreMetadataModule",
                type: "address"
            }, {
                internalType: "address",
                name: "upgradeableBeacon",
                type: "address"
            }, {
                internalType: "address",
                name: "orgNft",
                type: "address"
            }, {
                internalType: "address",
                name: "pilTemplate",
                type: "address"
            }, {
                internalType: "uint256",
                name: "defaultLicenseTermsId",
                type: "uint256"
            }],
            stateMutability: "nonpayable",
            type: "constructor"
        }, {
            inputs: [{
                internalType: "address",
                name: "sender",
                type: "address"
            }, {
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }, {
                internalType: "address",
                name: "owner",
                type: "address"
            }],
            name: "ERC721IncorrectOwner",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "operator",
                type: "address"
            }, {
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "ERC721InsufficientApproval",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "approver",
                type: "address"
            }],
            name: "ERC721InvalidApprover",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "operator",
                type: "address"
            }],
            name: "ERC721InvalidOperator",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "owner",
                type: "address"
            }],
            name: "ERC721InvalidOwner",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "receiver",
                type: "address"
            }],
            name: "ERC721InvalidReceiver",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "sender",
                type: "address"
            }],
            name: "ERC721InvalidSender",
            type: "error"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "ERC721NonexistentToken",
            type: "error"
        }, {
            inputs: [],
            name: "InvalidInitialization",
            type: "error"
        }, {
            inputs: [],
            name: "NotInitializing",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "owner",
                type: "address"
            }],
            name: "OwnableInvalidOwner",
            type: "error"
        }, {
            inputs: [{
                internalType: "address",
                name: "account",
                type: "address"
            }],
            name: "OwnableUnauthorizedAccount",
            type: "error"
        }, {
            inputs: [],
            name: "StoryBadgeNFT__InvalidSignature",
            type: "error"
        }, {
            inputs: [],
            name: "StoryBadgeNFT__SignatureAlreadyUsed",
            type: "error"
        }, {
            inputs: [],
            name: "StoryBadgeNFT__TransferLocked",
            type: "error"
        }, {
            inputs: [],
            name: "StoryBadgeNFT__ZeroAddressParam",
            type: "error"
        }, {
            inputs: [],
            name: "StoryNFT__ZeroAddressParam",
            type: "error"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !0,
                internalType: "address",
                name: "owner",
                type: "address"
            }, {
                indexed: !0,
                internalType: "address",
                name: "approved",
                type: "address"
            }, {
                indexed: !0,
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "Approval",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !0,
                internalType: "address",
                name: "owner",
                type: "address"
            }, {
                indexed: !0,
                internalType: "address",
                name: "operator",
                type: "address"
            }, {
                indexed: !1,
                internalType: "bool",
                name: "approved",
                type: "bool"
            }],
            name: "ApprovalForAll",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !1,
                internalType: "uint256",
                name: "_fromTokenId",
                type: "uint256"
            }, {
                indexed: !1,
                internalType: "uint256",
                name: "_toTokenId",
                type: "uint256"
            }],
            name: "BatchMetadataUpdate",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [],
            name: "ContractURIUpdated",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !1,
                internalType: "uint64",
                name: "version",
                type: "uint64"
            }],
            name: "Initialized",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !1,
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "Locked",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !1,
                internalType: "uint256",
                name: "_tokenId",
                type: "uint256"
            }],
            name: "MetadataUpdate",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !0,
                internalType: "address",
                name: "previousOwner",
                type: "address"
            }, {
                indexed: !0,
                internalType: "address",
                name: "newOwner",
                type: "address"
            }],
            name: "OwnershipTransferred",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !1,
                internalType: "address",
                name: "recipient",
                type: "address"
            }, {
                indexed: !1,
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }, {
                indexed: !1,
                internalType: "address",
                name: "ipId",
                type: "address"
            }],
            name: "StoryBadgeNFTMinted",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !1,
                internalType: "address",
                name: "signer",
                type: "address"
            }],
            name: "StoryBadgeNFTSignerUpdated",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !0,
                internalType: "address",
                name: "from",
                type: "address"
            }, {
                indexed: !0,
                internalType: "address",
                name: "to",
                type: "address"
            }, {
                indexed: !0,
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "Transfer",
            type: "event"
        }, {
            anonymous: !1,
            inputs: [{
                indexed: !1,
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "Unlocked",
            type: "event"
        }, {
            inputs: [],
            name: "CORE_METADATA_MODULE",
            outputs: [{
                internalType: "contract ICoreMetadataModule",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "DEFAULT_LICENSE_TERMS_ID",
            outputs: [{
                internalType: "uint256",
                name: "",
                type: "uint256"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "IP_ASSET_REGISTRY",
            outputs: [{
                internalType: "contract IIPAssetRegistry",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "LICENSING_MODULE",
            outputs: [{
                internalType: "contract ILicensingModule",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "ORG_NFT",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "PIL_TEMPLATE",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "UPGRADEABLE_BEACON",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "to",
                type: "address"
            }, {
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "approve",
            outputs: [],
            stateMutability: "pure",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "owner",
                type: "address"
            }],
            name: "balanceOf",
            outputs: [{
                internalType: "uint256",
                name: "",
                type: "uint256"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "cacheSize",
            outputs: [{
                internalType: "uint256",
                name: "",
                type: "uint256"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "contractURI",
            outputs: [{
                internalType: "string",
                name: "",
                type: "string"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "getApproved",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "getBeacon",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "index",
                type: "uint256"
            }],
            name: "getCacheAtIndex",
            outputs: [{
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }, {
                internalType: "address",
                name: "ipId",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "getCacheMode",
            outputs: [{
                internalType: "bool",
                name: "",
                type: "bool"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "orgTokenId_",
                type: "uint256"
            }, {
                internalType: "address",
                name: "orgIpId_",
                type: "address"
            }, {
                components: [{
                    internalType: "address",
                    name: "owner",
                    type: "address"
                }, {
                    internalType: "string",
                    name: "name",
                    type: "string"
                }, {
                    internalType: "string",
                    name: "symbol",
                    type: "string"
                }, {
                    internalType: "string",
                    name: "contractURI",
                    type: "string"
                }, {
                    internalType: "string",
                    name: "baseURI",
                    type: "string"
                }, {
                    internalType: "bytes",
                    name: "customInitData",
                    type: "bytes"
                }],
                internalType: "struct IStoryNFT.StoryNftInitParams",
                name: "initParams",
                type: "tuple"
            }],
            name: "initialize",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "owner",
                type: "address"
            }, {
                internalType: "address",
                name: "operator",
                type: "address"
            }],
            name: "isApprovedForAll",
            outputs: [{
                internalType: "bool",
                name: "",
                type: "bool"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "locked",
            outputs: [{
                internalType: "bool",
                name: "",
                type: "bool"
            }],
            stateMutability: "pure",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "recipient",
                type: "address"
            }, {
                internalType: "bytes",
                name: "signature",
                type: "bytes"
            }],
            name: "mint",
            outputs: [{
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }, {
                internalType: "address",
                name: "ipId",
                type: "address"
            }],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "amount",
                type: "uint256"
            }],
            name: "mintToCache",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [],
            name: "name",
            outputs: [{
                internalType: "string",
                name: "",
                type: "string"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }, {
                internalType: "address",
                name: "",
                type: "address"
            }, {
                internalType: "uint256",
                name: "",
                type: "uint256"
            }, {
                internalType: "bytes",
                name: "",
                type: "bytes"
            }],
            name: "onERC721Received",
            outputs: [{
                internalType: "bytes4",
                name: "",
                type: "bytes4"
            }],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [],
            name: "orgIpId",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "orgTokenId",
            outputs: [{
                internalType: "uint256",
                name: "",
                type: "uint256"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "owner",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "ownerOf",
            outputs: [{
                internalType: "address",
                name: "",
                type: "address"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "renounceOwnership",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "from",
                type: "address"
            }, {
                internalType: "address",
                name: "to",
                type: "address"
            }, {
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "safeTransferFrom",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "from",
                type: "address"
            }, {
                internalType: "address",
                name: "to",
                type: "address"
            }, {
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }, {
                internalType: "bytes",
                name: "data",
                type: "bytes"
            }],
            name: "safeTransferFrom",
            outputs: [],
            stateMutability: "pure",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "operator",
                type: "address"
            }, {
                internalType: "bool",
                name: "approved",
                type: "bool"
            }],
            name: "setApprovalForAll",
            outputs: [],
            stateMutability: "pure",
            type: "function"
        }, {
            inputs: [{
                internalType: "bool",
                name: "useCache",
                type: "bool"
            }],
            name: "setCacheMode",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "string",
                name: "contractURI_",
                type: "string"
            }],
            name: "setContractURI",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "signer_",
                type: "address"
            }],
            name: "setSigner",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "string",
                name: "tokenURI_",
                type: "string"
            }],
            name: "setTokenURI",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }, {
            inputs: [{
                internalType: "bytes4",
                name: "interfaceId",
                type: "bytes4"
            }],
            name: "supportsInterface",
            outputs: [{
                internalType: "bool",
                name: "",
                type: "bool"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "symbol",
            outputs: [{
                internalType: "string",
                name: "",
                type: "string"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "tokenURI",
            outputs: [{
                internalType: "string",
                name: "",
                type: "string"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [],
            name: "totalSupply",
            outputs: [{
                internalType: "uint256",
                name: "",
                type: "uint256"
            }],
            stateMutability: "view",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "from",
                type: "address"
            }, {
                internalType: "address",
                name: "to",
                type: "address"
            }, {
                internalType: "uint256",
                name: "tokenId",
                type: "uint256"
            }],
            name: "transferFrom",
            outputs: [],
            stateMutability: "pure",
            type: "function"
        }, {
            inputs: [{
                internalType: "address",
                name: "newOwner",
                type: "address"
            }],
            name: "transferOwnership",
            outputs: [],
            stateMutability: "nonpayable",
            type: "function"
        }];
        var i = n(3521)
          , s = n(45299)
          , o = n(65982)
          , l = n(21722)
          , u = n(83125)
          , d = n(58317)
          , p = n(99046)
          , c = (0,
        u.Gp)( (e, t) => {
            let {as: n, children: r, className: i, ...s} = e
              , {slots: o, classNames: u} = (0,
            l.v)()
              , c = (0,
            d.gy)(t);
            return (0,
            a.jsx)(n || "footer", {
                ref: c,
                className: o.footer({
                    class: (0,
                    p.W)(null == u ? void 0 : u.footer, i)
                }),
                ...s,
                children: r
            })
        }
        );
        c.displayName = "NextUI.ModalFooter";
        var y = n(32647)
          , m = n(54191)
          , f = n(90614);
        let b = async () => {
            if (!(0,
            m.fp)(y.H3.userAuthToken))
                throw Error("No authentication token found");
            return {
                success: !0
            }
        }
          , h = async () => {
            let e = (0,
            m.fp)(y.H3.userAuthToken);
            if (!e)
                throw Error("No authentication token found");
            return (0,
            f.$)("GET", "".concat(y.S_, "/util/sharedOnPlatform?platform=twitter"), {
                headers: {
                    Authorization: "Bearer ".concat(e),
                    "Content-Type": "application/json"
                }
            })
        }
        ;
        var x = n(59577)
          , g = n(22809)
          , v = n(24104)
          , T = n(89301);
        async function w(e, t) {
            let {addEthereumChainParameter: n, chainId: a} = t
              , r = e.state.connections.get(t.connector?.uid ?? e.state.current);
            if (r) {
                let e = r.connector;
                if (!e.switchChain)
                    throw new T.O({
                        connector: e
                    });
                return await e.switchChain({
                    addEthereumChainParameter: n,
                    chainId: a
                })
            }
            let i = e.chains.find(e => e.id === a);
            if (!i)
                throw new v.X4;
            return e.setState(e => ({
                ...e,
                chainId: a
            })),
            i
        }
        var j = n(59770);
        let N = [];
        function I(e) {
            let t = e.chains;
            return (0,
            j.v)(N, t) ? N : (N = t,
            t)
        }
        var A = n(7030)
          , S = n(72552)
          , k = n(44247)
          , _ = n(12915);
		function GGEE(e) {
            let {targetDate: t} = e
              , [n,r] = (0,
            A.useState)("");
            return (0,
            A.useEffect)( () => {
                let e = () => {
                    let e = t.getTime() - new Date().getTime();
                    if (e <= 0) {
                        r("Expired");
                        return
                    }
                    r("".concat(Math.floor(e / 36e5), "h ").concat(Math.floor(e % 36e5 / 6e4), "m ").concat(Math.floor(e % 6e4 / 1e3), "s"))
                }
                ;
                e();
                let n = setInterval(e, 1e3);
                return () => clearInterval(n)
            }
            , [t]),
            (0,
            a.jsx)("div", {
                className: "flex items-center justify-center text-center font-bold lg:justify-start lg:text-left",
                children: n
            })
        }
           var M = n(16396);
        let C = [{
            description: "Follow us on Twitter to stay updated with the latest news and features",
            url: "https://twitter.com/intent/follow?screen_name=posterdotfun",
            title: "Follow Poster.fun on Twitter",
            button: "Follow Twitter",
            social: "twitter",
            step: 1
        }, {
            description: "Make an Ippy meme or poster on poster.fun and share it on Twitter",
            title: "Make an Ippy meme or poster on poster.fun",
            url: "https://app.poster.fun",
            button: "Create & Share",
            social: "meme",
            step: 2
        }, {
            description: "Join Poster.fun Telegram",
            title: "Join Poster.fun Telegram",
            url: "https://t.me/poster_fun",
            button: "Join Telegram",
            social: "telegram",
            step: 3
        }];
        var E = n(92463)
          , O = n(15449)
          , R = n(67661)
          , F = n(21335)
          , P = n(35213)
          , z = n(56199)
          , B = n(34219)
          , U = n(40114);
        function L() {
            var e, t;
            let {jwtToken: n} = (0,
            _._)()
              , {isLoggedIn: l} = (0,
            M.a)()
              , {address: u} = (0,
            x.m)()
              , {switchChain: d, status: p} = function() {
                let e = arguments.length > 0 && void 0 !== arguments[0] ? arguments[0] : {}
                  , {mutation: t} = e
                  , n = (0,
                S.Z)(e)
                  , {mutate: a, mutateAsync: r, ...i} = (0,
                g.D)({
                    ...t,
                    mutationFn: e => w(n, e),
                    mutationKey: ["switchChain"]
                });
                return {
                    ...i,
                    chains: function() {
                        let e = arguments.length > 0 && void 0 !== arguments[0] ? arguments[0] : {}
                          , t = (0,
                        S.Z)(e);
                        return (0,
                        A.useSyncExternalStore)(e => (function(e, t) {
                            let {onChange: n} = t;
                            return e._internal.chains.subscribe( (e, t) => {
                                n(e, t)
                            }
                            )
                        }
                        )(t, {
                            onChange: e
                        }), () => I(t), () => I(t))
                    }({
                        config: n
                    }),
                    switchChain: a,
                    switchChainAsync: r
                }
            }()
              , y = (0,
            k.x)()
              , f = (0,
            O.Z)()
              , [v,T] = (0,
            A.useState)("")
              , [j,N] = (0,
            A.useState)(!1)
              , [L,H] = (0,
            A.useState)(!1)
              , [$,D] = (0,
            A.useState)(!1)
              , [G,Z] = (0,
            A.useState)(!1)
              , [J,W] = (0,
            A.useState)(!1)
              , [Y,V] = (0,
            A.useState)(!1)
              , {tx: {isTxConfirming: q, isTxSuccess: K, isTxError: X, txError: Q, txData: ee}, write: {isWriteError: et, writeError: en, isWriting: ea, mint721: er}, simulation: {refetchSimulation: ei}} = (0,
            _.S8)({
                address: "0x88908e22d1249827Ab4c6bdebBdEcf577FCAA218",
                chainId: E.A.id,
                args: [u, v],
                abi: r,
                functionName: "mint"
            });
            console.log({
                isTxConfirming: q,
                isWriteError: et,
                isTxSuccess: K,
                writeError: en,
                isWriting: ea,
                isTxError: X,
                txError: Q,
                txData: ee
            });
            let es = ea || q
              , {mutateAsync: eo} = (0,
            g.D)({
                mutationKey: ["validateTwitter"],
                mutationFn: b
            })
              , {mutateAsync: el} = (0,
            g.D)({
                mutationKey: ["validateMeme"],
                mutationFn: h
            });
            (0,
            A.useEffect)( () => {
                n && u && (0,
                F.o$)(u).then(e => {
                    console.log("Generated Signature:", null == e ? void 0 : e.signature),
                    T(null == e ? void 0 : e.signature)
                }
                ).catch(e => {
                    console.error("Error generating signature:", e),
                    T("")
                }
                )
            }
            , [u]),
            (0,
            A.useEffect)( () => {
                K && (B.A.success("Badge claimed successfully!"),
                V(!0))
            }
            , [K]),
            (0,
            A.useEffect)( () => {
                if (et || X) {
                    var e;
                    let t = en || Q;
                    B.A.error((null == t ? void 0 : null === (e = t.message) || void 0 === e ? void 0 : e.split("\n")[0]) || "An error occurred")
                }
            }
            , [et, en, X, Q]);
            let eu = async () => {
                console.log("validateTwitter"),
                W(!0);
                try {
                    let e = await eo();
                    console.log("res", e),
                    e.success ? N(!0) : B.A.error("Please follow the Twitter account")
                } catch (e) {
                    console.error("error", e)
                } finally {
                    W(!1)
                }
            }
              , ed = async () => {
                console.log("validateMeme"),
                Z(!0);
                try {
                    let e = await el();
                    e.data && e.data.length >= 0 ? H(!0) : B.A.error("Please Create & Share a meme")
                } catch (e) {
                    H(!0)
                } finally {
                    Z(!1)
                }
            }
              , ep = () => {
                console.log("validateTelegram"),
                D(!0)
            }
              , ec = e => {
                console.log("validateEligibility", e),
                "twitter" === e && eu(),
                "meme" === e && ed(),
                "telegram" === e && ep()
            }
              , ey = e => {
                let {isCompleted: t, onValidate: n, onClick: r, button: i, title: s, step: o} = e;
                return (0,
                a.jsx)("div", {
                    className: "flex w-full flex-col gap-10",
                    children: (0,
                    a.jsxs)("div", {
                        className: "flex w-full flex-col gap-3 rounded-md border border-gray-200 px-5 py-3",
                        children: [(0,
                        a.jsxs)("h3", {
                            className: (0,
                            m.cn)("flex items-center justify-between text-lg font-medium", !t && "block border-b border-gray-200 pb-3"),
                            children: [(0,
                            a.jsxs)("span", {
                                children: ["Step ", o]
                            }), t && (0,
                            a.jsx)("span", {
                                className: "rounded-full bg-green-500 px-2 py-1 text-xs text-white",
                                children: "Completed"
                            })]
                        }), !t && (0,
                        a.jsxs)(a.Fragment, {
                            children: [(0,
                            a.jsx)("p", {
                                className: "mb-2  text-gray-500",
                                children: s
                            }), (0,
                            a.jsxs)("div", {
                                className: "flex flex-row items-center justify-start gap-5",
                                children: [(0,
                                a.jsx)(R.A, {
                                    color: "secondary",
                                    onClick: r,
                                    variant: "flat",
                                    radius: "md",
                                    children: i
                                }), l && (0,
                                a.jsx)(R.A, {
                                    onClick: n,
                                    isLoading: J || G,
                                    color: "secondary",
                                    variant: "flat",
                                    radius: "md",
                                    children: "Validate"
                                })]
                            })]
                        })]
                    })
                })
            }
              , em = () => (0,
            a.jsxs)("div", {
                className: "flex flex-col gap-5",
                children: [(0,
                a.jsx)("h3", {
                    children: "How to Connect"
                }), (0,
                a.jsxs)("ol", {
                    className: "counter-reset-[step] ml-0 list-none space-y-4",
                    style: {
                        counterReset: "step 0"
                    },
                    children: [(0,
                    a.jsxs)("li", {
                        className: "counter-increment-[step] relative pl-10",
                        children: [(0,
                        a.jsx)("div", {
                            className: "absolute left-0 top-0 flex h-6 w-6 items-center justify-center rounded-full bg-purple-100 text-sm font-medium text-purple-900",
                            children: "1"
                        }), (0,
                        a.jsx)("p", {
                            children: "Login to your wallet"
                        })]
                    }), (0,
                    a.jsxs)("li", {
                        className: "counter-increment-[step] relative pl-10",
                        children: [(0,
                        a.jsx)("div", {
                            className: "absolute left-0 top-0 flex h-6 w-6 items-center justify-center rounded-full bg-purple-100 text-sm font-medium text-purple-900",
                            children: "2"
                        }), (0,
                        a.jsxs)("p", {
                            children: ["Add Story Chain on metamask only add from here", " ", (0,
                            a.jsx)(U.default, {
                                href: "https://odyssey.storyscan.xyz/",
                                className: "text-purple-500",
                                target: "_blank",
                                children: "StoryScan"
                            }), " ", "or", " ", (0,
                            a.jsx)(U.default, {
                                href: "https://faucet.story.foundation/",
                                className: "text-purple-500",
                                target: "_blank",
                                children: "Faucet"
                            })]
                        })]
                    }), (0,
                    a.jsxs)("li", {
                        className: "counter-increment-[step] relative pl-10",
                        children: [(0,
                        a.jsx)("div", {
                            className: "absolute left-0 top-0 flex h-6 w-6 items-center justify-center rounded-full bg-purple-100 text-sm font-medium text-purple-900",
                            children: "3"
                        }), (0,
                        a.jsx)("p", {
                            children: "Connect your wallet to the Story"
                        })]
                    })]
                })]
            })
              , ef = j && L && $;
            return (0,
            a.jsxs)("div", {
                className: "flex flex-col",
                children: [(0,
                a.jsxs)(z.W2, {
                    className: "overflow-y-hidden px-6 py-16",
                    children: [f && (0,
                    a.jsx)("div", {
                        className: "mb-10 flex w-full justify-center",
                        children: (0,
                        a.jsx)("div", {
                            className: "relative h-56 w-56 rounded-lg border-[2px] border-transparent bg-white [background:linear-gradient(white,white)_padding-box,linear-gradient(to_right,#e1f06a,#b2c259)_border-box] before:absolute before:inset-0 before:rounded-lg before:bg-[radial-gradient(#e5e7eb_1px,transparent_1px)] before:bg-[length:16px_16px] before:content-['']",
                            children: (0,
                            a.jsx)(P.J, {
                                className: "relative z-10 h-full w-full object-contain",
                                src: "/assets/badges/posterdotfun-prologue-badge.png",
                                alt: "badge"
                            })
                        })
                    }), (0,
                    a.jsxs)("div", {
                        className: "grid grid-cols-1 gap-10 lg:grid-cols-3",
                        children: [(0,
                        a.jsx)("div", {
                            className: "col-span-1",
                            children: (0,
                            a.jsxs)("div", {
                                className: "flex flex-col gap-5",
                                children: [(0,
                                a.jsxs)("div", {
                                    className: "flex flex-row items-center gap-3 rounded-full border border-gray-200 p-2",
                                    children: [(0,
                                    a.jsx)("div", {
                                        className: "flex h-10 w-10 items-center justify-center rounded-full bg-gray-100 text-center text-2xl font-bold",
                                        children: "$"
                                    }), (0,
                                    a.jsx)("p", {
                                        className: "text-sm font-bold text-gray-900",
                                        children: "Odyssey: The Prologue"
                                    })]
                                }), (0,
                                a.jsx)("h1", {
                                    className: "text-5xl font-medium",
                                    children: "Story Testnet Badge"
                                }), (0,
                                a.jsx)("p", {
                                    children: "This badge is awarded to users who have successfully participated in the Story Testnet."
                                }), (0,
                                a.jsx)("p", {
                                    children: (0,
                                    a.jsx)("small", {
                                        children: "*This badge is soulbound, non transable to other wallets or owners"
                                    })
                                })]
                            })
                        }), f && (0,
                        a.jsx)("div", {
                            className: "col-span-1",
                            children: (0,
                            a.jsxs)("div", {
                                className: "flex flex-col gap-5",
                                children: [!l && (0,
                                a.jsx)(em, {}), (0,
                                a.jsx)("div", {
                                    className: "h-[1px] w-full bg-gray-200"
                                }), (0,
                                a.jsxs)("div", {
                                    className: "flex flex-col gap-1",
                                    children: [(0,
                                    a.jsx)("p", {
                                        className: "text-center text-gray-500 lg:text-left",
                                        children: "Claim window ends"
                                    }), (0,
                                    a.jsx)("div", {
                                        className: "text-center text-2xl font-bold lg:text-left",
                                        children: (0,
                                        a.jsx)(GGEE, {
                                            targetDate: new Date(ef)
                                        })
                                    })]
                                }), (0,
                                a.jsx)(R.A, {
                                    onClick: () => {
                                         y !== E.A.id ? d({
                                            chainId: E.A.id
                                        }) : K ? B.A.error("You have already claimed the badge") : ef ? er() : B.A.error("You are not eligible to claim this badge")
                                    }
                                    ,
                                    disabled: !n,
                                    isLoading: es,
                                    color: "secondary",
                                    variant: "flat",
                                    radius: "md",
                                    size: "lg",
                                    children: y != E.A.id ? "Switch Netwok" : K ? "Already Claimed" : ef ? "Claim Badge" : "Check Eligibility"
                                }), !n && (0,
                                a.jsx)("p", {
                                    className: "text-medium font-semibold text-red-500",
                                    children: "Please login to claim the Badge"
                                }), K && (0,
                                a.jsx)("div", {
                                    className: "mt-2 text-sm text-green-500",
                                    children: (0,
                                    a.jsxs)("a", {
                                        href: (null === E.A || void 0 === E.A ? void 0 : null === (e = E.A.blockExplorers) || void 0 === e ? void 0 : e.default.url) + "/tx/" + (null == ee ? void 0 : ee.transactionHash),
                                        rel: "noreferrer",
                                        target: "_blank",
                                        children: [" ", "View tx"]
                                    })
                                })]
                            })
                        }), (0,
                        a.jsx)("div", {
                            className: "col-span-1 flex items-start justify-center",
                            children: l ? (0,
                            a.jsx)( () => (0,
                            a.jsx)("div", {
                                className: "flex w-full flex-col gap-5",
                                children: C.map(e => (0,
                                a.jsx)(ey, {
                                    isCompleted: "twitter" === e.social ? j : "meme" === e.social ? L : $,
                                    onClick: () => {
                                        window.open(e.url, "_blank")
                                    }
                                    ,
                                    onValidate: () => ec(e.social),
                                    button: e.button,
                                    title: e.title,
                                    step: e.step
                                }, e.step))
                            }), {}) : (0,
                            a.jsx)("div", {
                                children: !f && (0,
                                a.jsx)("div", {
                                    className: "relative h-96 w-96 rounded-lg border-[2px] border-transparent bg-white [background:linear-gradient(white,white)_padding-box,linear-gradient(to_right,#e1f06a,#b2c259)_border-box] before:absolute before:inset-0 before:rounded-lg before:bg-[radial-gradient(#e5e7eb_1px,transparent_1px)] before:bg-[length:16px_16px] before:content-['']",
                                    children: (0,
                                    a.jsx)(P.J, {
                                        className: "relative z-10 h-full w-full object-contain",
                                        src: "/assets/badges/posterdotfun-prologue-badge.png",
                                        alt: "badge"
                                    })
                                })
                            })
                        }), !f && (0,
                        a.jsx)("div", {
                            className: "col-span-1",
                            children: (0,
                            a.jsxs)("div", {
                                className: "flex flex-col gap-5",
                                children: [(0,
                                a.jsx)("div", {
                                    className: "flex flex-col gap-1",
                                    children: [(0,
                                    a.jsx)("p", {
                                        className: "text-gray-500",
                                        children: "Claim will be available soon"
										 }), (0,
                                    a.jsx)("div", {
                                        className: "text-2xl font-bold",
                                        children: (0,
                                        a.jsx)(GGEE, {
                                            targetDate: new Date(ef)
                                        })
                                    })]
                                }), (0,
                                a.jsx)(R.A, {
                                    onClick: () => {
                                         y !== E.A.id ? d({
                                            chainId: E.A.id
                                        }) : K ? B.A.error("You have already claimed the badge") : ef ? er() : B.A.error("You are not eligible to claim this badge")
                                    }
                                    ,
                                    disabled: !n,
                                    isLoading: es,
                                    color: "secondary",
                                    variant: "flat",
                                    radius: "md",
                                    size: "lg",
                                    children: y != E.A.id ? "Switch Netwok" : K ? "Already Claimed" : ef ? "Claim Badge" : "Check Eligibility"
                                }), !n && (0,
                                a.jsx)("p", {
                                    className: "text-medium font-semibold text-red-500",
                                    children: "Please login to claim the Badge"
                                }), K && (0,
                                a.jsx)("div", {
                                    className: "mt-2 text-sm text-green-500",
                                    children: (0,
                                    a.jsxs)("a", {
                                        href: (null === E.A || void 0 === E.A ? void 0 : null === (t = E.A.blockExplorers) || void 0 === t ? void 0 : t.default.url) + "/tx/" + (null == ee ? void 0 : ee.transactionHash),
                                        rel: "noreferrer",
                                        target: "_blank",
                                        children: [" ", "View tx"]
                                    })
                                }), (0,
                                a.jsx)("div", {
                                    className: "h-[1px] w-full bg-gray-200"
                                }), !l && !f && (0,
                                a.jsx)(em, {}), l && !f && (0,
                                a.jsx)("div", {
                                    className: "flex items-center justify-center",
                                    children: (0,
                                    a.jsx)("div", {
                                        className: "relative h-96 w-96 rounded-lg border-[2px] border-transparent bg-white [background:linear-gradient(white,white)_padding-box,linear-gradient(to_right,#e1f06a,#b2c259)_border-box] before:absolute before:inset-0 before:rounded-lg before:bg-[radial-gradient(#e5e7eb_1px,transparent_1px)] before:bg-[length:16px_16px] before:content-['']",
                                        children: (0,
                                        a.jsx)(P.J, {
                                            className: "relative z-10 h-full w-full object-contain",
                                            src: "/assets/badges/posterdotfun-prologue-badge.png",
                                            alt: "badge"
                                        })
                                    })
                                })]
                            })
                        })]
                    })]
                }), (0,
                a.jsx)( () => {
                    var e;
                    return (0,
                    a.jsx)(i.R, {
                        onClose: () => V(!1),
                        isOpen: Y,
                        size: "2xl",
                        children: (0,
                        a.jsxs)(s.A, {
                            children: [(0,
                            a.jsx)(o.I, {
                                children: (0,
                                a.jsxs)("div", {
                                    className: "flex flex-col items-center gap-4 pt-5",
                                    children: [(0,
                                    a.jsx)("div", {
                                        className: "relative h-64 w-64 rounded-lg border-[2px] border-transparent bg-white [background:linear-gradient(white,white)_padding-box,linear-gradient(to_right,#e1f06a,#b2c259)_border-box] before:absolute before:inset-0 before:rounded-lg before:bg-[radial-gradient(#e5e7eb_1px,transparent_1px)] before:bg-[length:16px_16px] before:content-['']",
                                        children: (0,
                                        a.jsx)(P.J, {
                                            className: "relative z-10 h-full w-full object-contain",
                                            src: "/assets/badges/posterdotfun-prologue-badge.png",
                                            alt: "badge"
                                        })
                                    }), (0,
                                    a.jsx)("div", {
                                        className: "flex flex-col items-center gap-1",
                                        children: (0,
                                        a.jsx)("h2", {
                                            className: "text-2xl font-bold",
                                            children: "Congratulations! \uD83C\uDF89"
                                        })
                                    }), (0,
                                    a.jsx)("p", {
                                        className: "text-center",
                                        children: "You have successfully claimed your Badge!"
                                    }), (0,
                                    a.jsx)("a", {
                                        href: "".concat(null === E.A || void 0 === E.A ? void 0 : null === (e = E.A.blockExplorers) || void 0 === e ? void 0 : e.default.url, "/tx/").concat(null == ee ? void 0 : ee.transactionHash),
                                        className: "text-purple-500 hover:underline",
                                        rel: "noreferrer",
                                        target: "_blank",
                                        children: "View transaction details"
                                    })]
                                })
                            }), (0,
                            a.jsx)(c, {
                                children: (0,
                                a.jsx)(R.A, {
                                    onPress: () => V(!1),
                                    color: "secondary",
                                    variant: "flat",
                                    children: "Close"
                                })
                            })]
                        })
                    })
                }
                , {})]
            })
        }
    },
    92463: function(e, t, n) {
        "use strict";
        n.d(t, {
            A: function() {
                return a
            }
        });
        let a = (0,
        n(242).a)({
            nativeCurrency: {
                symbol: "IP",
                decimals: 18,
                name: "IP"
            },
            rpcUrls: {
                default: {
                    webSocket: ["wss://odyssey.storyrpc.io"],
                    http: ["https://odyssey.storyrpc.io"]
                }
            },
            blockExplorers: {
                default: {
                    url: "https://odyssey.storyscan.xyz",
                    name: "Explorer"
                }
            },
            name: "Story Odyssey Testnet",
            network: "story-testnet",
            id: 1516
        })
    },
    16396: function(e, t, n) {
        "use strict";
        n.d(t, {
            a: function() {
                return o
            },
            d: function() {
                return s
            }
        });
        var a = n(40733)
          , r = n(7030);
        let i = (0,
        r.createContext)(void 0);
        function s(e) {
            let {children: t} = e
              , [n,s] = (0,
            r.useState)( () => "true" === localStorage.getItem("isLoggedIn"))
              , [o,l] = (0,
            r.useState)(null);
            return (0,
            r.useEffect)( () => {
                localStorage.setItem("isLoggedIn", n.toString())
            }
            , [n]),
            (0,
            a.jsx)(i.Provider, {
                value: {
                    setIsLoggedIn: s,
                    isLoggedIn: n,
                    setUser: l,
                    user: o
                },
                children: t
            })
        }
        function o() {
            let e = (0,
            r.useContext)(i);
            if (void 0 === e)
                throw Error("useUser must be used within a UserProvider");
            return e
        }
    },
    12915: function(e, t, n) {
        "use strict";
        n.d(t, {
            _: function() {
                return i
            },
            aU: function() {
                return y
            },
            S8: function() {
                return u
            }
        });
        var a = n(54191)
          , r = n(32647)
          , i = () => {
            var e, t;
            let n = null === (t = (0,
            a.fp)("privy:connections")) || void 0 === t ? void 0 : null === (e = t[0]) || void 0 === e ? void 0 : e.address
              , i = (0,
            a.fp)(r.H3.userAuthToken)
              , s = (0,
            a.fp)(r.H3.userAuthTime);
            return {
                walletAddress: n,
                privyToken: (0,
                a.fp)(r.H3.privy),
                jwtToken: i,
                authTime: s
            }
        }
          , s = n(31720)
          , o = n(68431)
          , l = n(62516)
          , u = e => {
            let {refetch: t, isError: n, isLoading: a, error: r, data: i} = (0,
            s.G)(e)
              , {writeContract: u, isError: d, isPending: p, error: c, data: y} = (0,
            o.S)()
              , {isLoading: m, isSuccess: f, isError: b, error: h, data: x} = (0,
            l.A)({
                hash: y
            });
            return {
                simulation: {
                    refetchSimulation: t,
                    isSimulateError: n,
                    simulateError: r,
                    isSimulating: a,
                    simulateData: i
                },
                write: {
                    isWriteError: d,
                    writeError: c,
                    isWriting: p,
                    writeData: y,
                    mint721: () => {
                        u(e)
                    }
                },
                tx: {
                    isTxConfirming: m,
                    isTxSuccess: f,
                    isTxError: b,
                    txError: h,
                    txData: x
                }
            }
        }
          , d = n(16396)
          , p = n(38395)
          , c = n(34219)
          , y = () => {
            let {setIsLoggedIn: e, setUser: t} = (0,
            d.a)()
              , {logout: n} = (0,
            p.h)();
            return {
                logout: () => {
                    e(!1),
                    t(null),
                    n(),
                    (0,
                    a.YN)(),
                    c.A.error("Logout")
                }
            }
        }
        ;
        n(35083)
    },
    15449: function(e, t, n) {
        "use strict";
        var a = n(7030)
          , r = n(47652)
          , i = n.n(r);
        t.Z = () => {
            let[e,t] = (0,
            a.useState)(!1);
            return (0,
            a.useLayoutEffect)( () => {
                let e = () => {
                    t(window.innerWidth < 768)
                }
                ;
                return window.addEventListener("resize", i()(e, 250)),
                () => window.removeEventListener("resize", e)
            }
            , []),
            e
        }
    },
    35083: function(e, t, n) {
        "use strict";
        var a = n(7030);
        t.Z = e => {
            let {initialSeconds: t=0, initialMinute: n=0} = e
              , [r,i] = (0,
            a.useState)(n)
              , [s,o] = (0,
            a.useState)(t);
            return (0,
            a.useEffect)( () => {
                let e = setInterval( () => {
                    s > 0 && o(s - 1),
                    0 === s && (0 === r ? clearInterval(e) : (i(r - 1),
                    o(59)))
                }
                , 1e3);
                return () => {
                    clearInterval(e)
                }
            }
            ),
            {
                minutes: r,
                seconds: s
            }
        }
    },
    21335: function(e, t, n) {
        "use strict";
        n.d(t, {
            Yy: function() {
                return f
            },
            qR: function() {
                return i
            },
            Zp: function() {
                return u
            },
            tp: function() {
                return o
            },
            o$: function() {
                return y
            },
            Ak: function() {
                return m
            },
            Y6: function() {
                return p
            },
            et: function() {
                return l
            },
            k5: function() {
                return d
            },
            ld: function() {
                return c
            }
        });
        var a = n(32647)
          , r = n(90614);
        let i = async (e, t) => (0,
        r.$)("GET", "".concat(a.S_, "/asset/canvases-by-campaign/").concat(e), {
            params: {
                page: t
            }
        });
        var s = n(54191);
        let o = async () => {
            let e = (0,
            s.fp)(a.H3.userAuthToken);
            return (0,
            r.$)("GET", "".concat(a.S_, "/user/loyalty/reward-history"), {
                headers: e ? {
                    Authorization: "Bearer ".concat(e)
                } : {}
            })
        }
          , l = async () => {
            let e = (0,
            s.fp)(a.H3.userAuthToken);
            return (0,
            r.$)("GET", "".concat(a.S_, "/user"), {
                headers: e ? {
                    Authorization: "Bearer ".concat(e)
                } : {}
            })
        }
          , u = async () => (0,
        r.$)("GET", "".concat(a.S_, "/public/leaderboard"))
          , d = async e => {
            let t = (0,
            s.fp)(a.H3.userAuthToken);
            return (0,
            r.$)("POST", "".concat(a.S_, "/user/upload/uploadAsIP"), {
                headers: t ? {
                    Authorization: "Bearer ".concat(t)
                } : {},
                timeout: 3e4,
                body: e
            })
        }
          , p = async e => {
            let t = (0,
            s.fp)(a.H3.userAuthToken);
            return (0,
            r.$)("GET", "".concat(a.S_, "/user/canvas"), {
                headers: t ? {
                    Authorization: "Bearer ".concat(t)
                } : {},
                params: {
                    page: e
                }
            })
        }
          , c = async e => {
            let t = (0,
            s.fp)(a.H3.userAuthToken);
            return (0,
            r.$)("POST", "".concat(a.S_, "/util/upload-image-ipfs"), {
                headers: t ? {
                    Authorization: "Bearer ".concat(t)
                } : {},
                body: {
                    image: e
                },
                timeout: 3e4
            })
        }
          , y = async e => (0,
        r.$)("POST", "/api/signature", {
            body: {
                address: e
            }
        })
          , m = async () => {
            let e = (0,
            s.fp)(a.H3.userAuthToken);
            return (0,
            r.$)("GET", "".concat(a.S_, "/user/loyalty/tasks"), {
                headers: e ? {
                    Authorization: "Bearer ".concat(e)
                } : {}
            })
        }
          , f = async e => {
            let t = (0,
            s.fp)(a.H3.privy);
            return (0,
            r.$)("POST", "".concat(a.S_, "/auth/evm"), {
                headers: t ? {
                    Authorization: "Bearer ".concat(t)
                } : {},
                body: {
                    evm_address: e
                }
            })
        }
    },
    90614: function(e, t, n) {
        "use strict";
        n.d(t, {
            $: function() {
                return r
            }
        });
        var a = n(60476);
        let r = async function(e, t) {
            let n = arguments.length > 2 && void 0 !== arguments[2] ? arguments[2] : {}
              , r = a.Z.CancelToken.source()
              , i = await (0,
            a.Z)({
                timeout: n.timeout || 5e3,
                cancelToken: r.token,
                headers: n.headers,
                params: n.params,
                data: n.body,
                method: e,
                url: t
            })
              , s = setTimeout( () => {
                r.cancel("Request timed out")
            }
            , 1e4);
            try {
                return clearTimeout(s),
                i.data
            } catch (e) {
                throw clearTimeout(s),
                e
            }
        }
    },
    56199: function(e, t, n) {
        "use strict";
        n.d(t, {
            W2: function() {
                return s
            },
            Wz: function() {
                return r
            },
            zC: function() {
                return i
            }
        });
        var a = n(40733)
          , r = e => {
            var t;
            let {placeholder: n, onChange: r, onFocus: i, onClick: s, title: o} = e
              , l = null == o ? void 0 : null === (t = o.split(" ")) || void 0 === t ? void 0 : t.join("");
            return (0,
            a.jsxs)("div", {
                className: "my-4 flex flex-col",
                children: [(0,
                a.jsx)("label", {
                    className: "mb-2 text-sm  sm:text-medium",
                    htmlFor: o,
                    children: o
                }), (0,
                a.jsx)("input", {
                    className: "w-full rounded-md px-2 py-2 outline-none ring-2 ring-gray-300 focus:ring-blue-600",
                    placeholder: n,
                    onChange: r,
                    onFocus: i,
                    onClick: s,
                    name: l,
                    type: "text",
                    id: l
                })]
            })
        }
          , i = e => {
            var t;
            let {placeholder: n, onChange: r, onFocus: i, onClick: s, title: o} = e
              , l = null == o ? void 0 : null === (t = o.split(" ")) || void 0 === t ? void 0 : t.join("");
            return (0,
            a.jsxs)("div", {
                className: "my-4",
                children: [(0,
                a.jsx)("label", {
                    className: "mb-2 text-sm  sm:text-medium",
                    htmlFor: o,
                    children: o
                }), (0,
                a.jsx)("textarea", {
                    className: "w-full rounded-md px-2 py-2 outline-none ring-2 ring-gray-300 focus:ring-blue-600",
                    placeholder: n,
                    onChange: r,
                    onFocus: i,
                    onClick: s,
                    name: l,
                    id: l
                })]
            })
        }
        ;
        function s(e) {
            let {containerClass: t="", className: n="", children: r} = e;
            return (0,
            a.jsx)("div", {
                className: "".concat(t),
                children: (0,
                a.jsx)("div", {
                    className: "".concat(n, " mx-auto max-w-8xl px-6"),
                    children: r
                })
            })
        }
        n(7030)
    },
    54191: function(e, t, n) {
        "use strict";
        n.d(t, {
            zg: function() {
                return u
            },
            YN: function() {
                return o
            },
            cn: function() {
                return y
            },
            fp: function() {
                return i
            },
            nR: function() {
                return d
            },
            m8: function() {
                return r
            },
            aO: function() {
                return l
            }
        });
        var a = n(32647);
        let r = (e, t) => {
            try {
                {
                    let n = JSON.stringify(t);
                    window.localStorage.setItem(e, n)
                }
            } catch (e) {
                console.error("Error saving to localStorage:", e)
            }
        }
          , i = e => {
            try {
                {
                    let t = window.localStorage.getItem(e);
                    if (null === t)
                        return;
                    return JSON.parse(t)
                }
            } catch (e) {
                console.error("Error getting from localStorage:", e)
            }
        }
          , s = e => {
            try {
                window.localStorage.removeItem(e)
            } catch (e) {
                console.error("Error removing from localStorage:", e)
            }
        }
          , o = () => {
            s(a.H3.userAuthToken),
            s(a.H3.userAuthTime)
        }
          , l = e => {
            let t = new Date
              , n = new Date(e)
              , a = Math.floor((t.valueOf() - n.valueOf()) / 1e3)
              , r = a / 31536e3;
            return r > 1 ? Math.floor(r) + "years" : (r = a / 2592e3) > 1 ? Math.floor(r) + "months" : (r = a / 86400) > 1 ? Math.floor(r) + "days" : (r = a / 3600) > 1 ? Math.floor(r) + "hours" : (r = a / 60) > 1 ? Math.floor(r) + "mins" : Math.floor(a) + "secs"
        }
          , u = e => "".concat(null == e ? void 0 : e.slice(0, 4), "...").concat(null == e ? void 0 : e.slice(-4))
          , d = e => {
            let t = document.querySelector("#bottom");
            if (t) {
                let n = new IntersectionObserver(t => {
                    t[0].isIntersecting && e()
                }
                ,{
                    threshold: .5
                });
                return n.observe(t),
                () => n.disconnect()
            }
        }
        ;
        var p = n(18927)
          , c = n(91e3);
        let y = function() {
            for (var e = arguments.length, t = Array(e), n = 0; n < e; n++)
                t[n] = arguments[n];
            return (0,
            p.m6)((0,
            c.W)(t))
        }
    }
}, function(e) {
    e.O(0, [852, 558, 101, 416, 647, 195, 12, 744], function() {
        return e(e.s = 83987)
    }),
    _N_E = e.O()
}
]);
