---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186406"
---
# <span data-ttu-id="66481-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="66481-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="66481-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66481-102">SYNOPSIS</span></span>
<span data-ttu-id="66481-103">Új veszélyforrásokat érintő intelligencia whitelist létrehozása az Azure tűzfal házirendjéhez</span><span class="sxs-lookup"><span data-stu-id="66481-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="66481-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66481-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66481-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66481-105">DESCRIPTION</span></span>
<span data-ttu-id="66481-106">A **New-AzFirewallPolicyThreatIntelWhitelist** parancsmag létrehoz egy veszélyforrás Intel whitelist objektumot, amelyet az Azure tűzfal-házirend létrehozásakor vagy beállításakor használhat.</span><span class="sxs-lookup"><span data-stu-id="66481-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="66481-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66481-107">EXAMPLES</span></span>

### <span data-ttu-id="66481-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="66481-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="66481-109">Ebben a példában egy olyan veszélyforrást hoz létre az Intel whitelist, amely egyetlen bejegyzésből és egy IP-címmel rendelkező, két bejegyzésből álló IP-címmel rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="66481-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="66481-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66481-110">PARAMETERS</span></span>

### <span data-ttu-id="66481-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66481-111">-DefaultProfile</span></span>
<span data-ttu-id="66481-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66481-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66481-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="66481-113">-FQDN</span></span>
<span data-ttu-id="66481-114">A Threat Intel whitelist (teljes tartománynevek)</span><span class="sxs-lookup"><span data-stu-id="66481-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66481-115">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="66481-115">-IpAddress</span></span>
<span data-ttu-id="66481-116">Az Intel-whitelist veszélyforrás IP-címei</span><span class="sxs-lookup"><span data-stu-id="66481-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66481-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66481-117">CommonParameters</span></span>
<span data-ttu-id="66481-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66481-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66481-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="66481-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66481-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66481-120">INPUTS</span></span>

### <span data-ttu-id="66481-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="66481-121">None</span></span>

## <span data-ttu-id="66481-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66481-122">OUTPUTS</span></span>

### <span data-ttu-id="66481-123">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="66481-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="66481-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66481-124">NOTES</span></span>

## <span data-ttu-id="66481-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66481-125">RELATED LINKS</span></span>
