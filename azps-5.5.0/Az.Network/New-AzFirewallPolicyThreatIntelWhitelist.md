---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156898"
---
# <span data-ttu-id="cac77-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="cac77-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="cac77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cac77-102">SYNOPSIS</span></span>
<span data-ttu-id="cac77-103">Új veszélyforrás-felderítési engedélyezési lista létrehozása az Azure tűzfal-házirendhez</span><span class="sxs-lookup"><span data-stu-id="cac77-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="cac77-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cac77-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac77-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cac77-105">DESCRIPTION</span></span>
<span data-ttu-id="cac77-106">A **New-AzFirewallPolicyThreatIntelWhitelist** parancsmag létrehoz egy veszélyforrásokkal kapcsolatos intel whitelist objektumot, amely azure tűzfalházi házirend létrehozásakor és beállításakor használható.</span><span class="sxs-lookup"><span data-stu-id="cac77-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="cac77-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cac77-107">EXAMPLES</span></span>

### <span data-ttu-id="cac77-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cac77-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="cac77-109">Ebben a példában egy veszélyforrásra vonatkozó intel whitelistát hoz létre, amely egy bejegyzés FQDN-whitelistját és egy ip-cím whitelistát tartalmaz két bejegyzésből.</span><span class="sxs-lookup"><span data-stu-id="cac77-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="cac77-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cac77-110">PARAMETERS</span></span>

### <span data-ttu-id="cac77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac77-111">-DefaultProfile</span></span>
<span data-ttu-id="cac77-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cac77-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cac77-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="cac77-113">-FQDN</span></span>
<span data-ttu-id="cac77-114">The FQDNs of the Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="cac77-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="cac77-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="cac77-115">-IpAddress</span></span>
<span data-ttu-id="cac77-116">A Threat Intel Whitelist IP-címei</span><span class="sxs-lookup"><span data-stu-id="cac77-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="cac77-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac77-117">CommonParameters</span></span>
<span data-ttu-id="cac77-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac77-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac77-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cac77-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac77-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cac77-120">INPUTS</span></span>

### <span data-ttu-id="cac77-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="cac77-121">None</span></span>

## <span data-ttu-id="cac77-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cac77-122">OUTPUTS</span></span>

### <span data-ttu-id="cac77-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="cac77-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="cac77-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cac77-124">NOTES</span></span>

## <span data-ttu-id="cac77-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cac77-125">RELATED LINKS</span></span>
