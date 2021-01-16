---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342750"
---
# <span data-ttu-id="48937-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="48937-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="48937-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48937-102">SYNOPSIS</span></span>
<span data-ttu-id="48937-103">Új veszélyforrás-felderítési engedélyezési lista létrehozása az Azure tűzfalhoz</span><span class="sxs-lookup"><span data-stu-id="48937-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="48937-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="48937-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48937-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="48937-105">DESCRIPTION</span></span>
<span data-ttu-id="48937-106">A **New-AzFirewallThreatIntelWhitelist** parancsmag létrehoz egy veszélyforrás-intel whitelist objektumot, amely azure tűzfal létrehozásakor és beállításakor használható.</span><span class="sxs-lookup"><span data-stu-id="48937-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="48937-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="48937-107">EXAMPLES</span></span>

### <span data-ttu-id="48937-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="48937-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="48937-109">Ebben a példában egy veszélyforrásokkal kapcsolatos intel whitelistát hoz létre, amely tartalmazza a két bejegyzésből és egy IP-cím whitelistát két bejegyzésből.</span><span class="sxs-lookup"><span data-stu-id="48937-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="48937-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48937-110">PARAMETERS</span></span>

### <span data-ttu-id="48937-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48937-111">-DefaultProfile</span></span>
<span data-ttu-id="48937-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48937-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48937-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="48937-113">-FQDN</span></span>
<span data-ttu-id="48937-114">The FQDNs of the Threat Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="48937-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="48937-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="48937-115">-IpAddress</span></span>
<span data-ttu-id="48937-116">A Threat Intel Whitelist IP-címei</span><span class="sxs-lookup"><span data-stu-id="48937-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="48937-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48937-117">CommonParameters</span></span>
<span data-ttu-id="48937-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48937-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48937-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48937-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48937-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48937-120">INPUTS</span></span>

### <span data-ttu-id="48937-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="48937-121">None</span></span>

## <span data-ttu-id="48937-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48937-122">OUTPUTS</span></span>

### <span data-ttu-id="48937-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="48937-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="48937-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="48937-124">NOTES</span></span>

## <span data-ttu-id="48937-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48937-125">RELATED LINKS</span></span>

[<span data-ttu-id="48937-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48937-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="48937-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48937-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="48937-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="48937-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)