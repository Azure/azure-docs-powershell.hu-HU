---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347634"
---
# <span data-ttu-id="5d641-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="5d641-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="5d641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d641-102">SYNOPSIS</span></span>
<span data-ttu-id="5d641-103">Új veszélyforrás-felderítési engedélyezési lista létrehozása az Azure tűzfal-házirendhez</span><span class="sxs-lookup"><span data-stu-id="5d641-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="5d641-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d641-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d641-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d641-105">DESCRIPTION</span></span>
<span data-ttu-id="5d641-106">A **New-AzFirewallPolicyThreatIntelWhitelist** parancsmag létrehoz egy veszélyforrás-intel whitelist objektumot, amely Azure tűzfalházi házirend létrehozásakor és beállításakor használható.</span><span class="sxs-lookup"><span data-stu-id="5d641-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="5d641-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d641-107">EXAMPLES</span></span>

### <span data-ttu-id="5d641-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="5d641-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="5d641-109">Ebben a példában egy veszélyforrásra vonatkozó intel whitelistát hoz létre, amely egy bejegyzés FQDN-whitelistját és egy ip-cím whitelistát tartalmaz két bejegyzésből.</span><span class="sxs-lookup"><span data-stu-id="5d641-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="5d641-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d641-110">PARAMETERS</span></span>

### <span data-ttu-id="5d641-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d641-111">-DefaultProfile</span></span>
<span data-ttu-id="5d641-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d641-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d641-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="5d641-113">-FQDN</span></span>
<span data-ttu-id="5d641-114">The FQDNs of the Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="5d641-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="5d641-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="5d641-115">-IpAddress</span></span>
<span data-ttu-id="5d641-116">A Threat Intel Whitelist IP-címei</span><span class="sxs-lookup"><span data-stu-id="5d641-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="5d641-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d641-117">CommonParameters</span></span>
<span data-ttu-id="5d641-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d641-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d641-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d641-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d641-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d641-120">INPUTS</span></span>

### <span data-ttu-id="5d641-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d641-121">None</span></span>

## <span data-ttu-id="5d641-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d641-122">OUTPUTS</span></span>

### <span data-ttu-id="5d641-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="5d641-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="5d641-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d641-124">NOTES</span></span>

## <span data-ttu-id="5d641-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d641-125">RELATED LINKS</span></span>
