---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 18946b74ea72ac3d5db2dd683657eda60b8eeec5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924690"
---
# <span data-ttu-id="0857b-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="0857b-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="0857b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0857b-102">SYNOPSIS</span></span>
<span data-ttu-id="0857b-103">Új veszélyforrás-felderítési engedélyezési lista létrehozása az Azure tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="0857b-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="0857b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0857b-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0857b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0857b-105">DESCRIPTION</span></span>
<span data-ttu-id="0857b-106">A **New-AzFirewallThreatIntelWhitelist** parancsmag létrehoz egy veszélyforrás-intel whitelist objektumot, amely azure tűzfal létrehozásakor és beállításakor használható.</span><span class="sxs-lookup"><span data-stu-id="0857b-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="0857b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0857b-107">EXAMPLES</span></span>

### <span data-ttu-id="0857b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0857b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="0857b-109">Ebben a példában egy veszélyforrásokkal kapcsolatos intel whitelistát hoz létre, amely tartalmazza a két bejegyzésből és egy IP-cím whitelistát két bejegyzésből.</span><span class="sxs-lookup"><span data-stu-id="0857b-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="0857b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0857b-110">PARAMETERS</span></span>

### <span data-ttu-id="0857b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0857b-111">-DefaultProfile</span></span>
<span data-ttu-id="0857b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0857b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0857b-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="0857b-113">-FQDN</span></span>
<span data-ttu-id="0857b-114">The FQDNs of the Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="0857b-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0857b-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="0857b-115">-IpAddress</span></span>
<span data-ttu-id="0857b-116">A Threat Intel Whitelist IP-címei</span><span class="sxs-lookup"><span data-stu-id="0857b-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0857b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0857b-117">CommonParameters</span></span>
<span data-ttu-id="0857b-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0857b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0857b-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0857b-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0857b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0857b-120">INPUTS</span></span>

### <span data-ttu-id="0857b-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="0857b-121">None</span></span>

## <span data-ttu-id="0857b-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0857b-122">OUTPUTS</span></span>

### <span data-ttu-id="0857b-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="0857b-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="0857b-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0857b-124">NOTES</span></span>

## <span data-ttu-id="0857b-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0857b-125">RELATED LINKS</span></span>

[<span data-ttu-id="0857b-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0857b-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="0857b-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0857b-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="0857b-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="0857b-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)