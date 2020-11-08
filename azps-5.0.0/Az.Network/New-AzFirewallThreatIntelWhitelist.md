---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186405"
---
# <span data-ttu-id="ce170-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ce170-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="ce170-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce170-102">SYNOPSIS</span></span>
<span data-ttu-id="ce170-103">Új veszélyforrásokat érintő intelligencia whitelist létrehozása az Azure Firewall-hoz</span><span class="sxs-lookup"><span data-stu-id="ce170-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="ce170-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce170-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce170-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce170-105">DESCRIPTION</span></span>
<span data-ttu-id="ce170-106">A **New-AzFirewallThreatIntelWhitelist** parancsmag létrehoz egy veszélyforrás Intel whitelist objektumot, amelyet az Azure-tűzfal létrehozásakor vagy beállításakor használhat.</span><span class="sxs-lookup"><span data-stu-id="ce170-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="ce170-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ce170-107">EXAMPLES</span></span>

### <span data-ttu-id="ce170-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ce170-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="ce170-109">Ez a példa létrehoz egy veszélyforrást az Intel whitelist-ben, amely a két bejegyzésből és a két bejegyzésből álló IP-cím whitelistből áll.</span><span class="sxs-lookup"><span data-stu-id="ce170-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="ce170-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce170-110">PARAMETERS</span></span>

### <span data-ttu-id="ce170-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce170-111">-DefaultProfile</span></span>
<span data-ttu-id="ce170-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce170-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce170-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="ce170-113">-FQDN</span></span>
<span data-ttu-id="ce170-114">A Threat Intel whitelist (teljes tartománynevek)</span><span class="sxs-lookup"><span data-stu-id="ce170-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="ce170-115">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="ce170-115">-IpAddress</span></span>
<span data-ttu-id="ce170-116">Az Intel-whitelist veszélyforrás IP-címei</span><span class="sxs-lookup"><span data-stu-id="ce170-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="ce170-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce170-117">CommonParameters</span></span>
<span data-ttu-id="ce170-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce170-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce170-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ce170-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce170-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce170-120">INPUTS</span></span>

### <span data-ttu-id="ce170-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="ce170-121">None</span></span>

## <span data-ttu-id="ce170-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce170-122">OUTPUTS</span></span>

### <span data-ttu-id="ce170-123">Microsoft. Azure. commands. Network. models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="ce170-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="ce170-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce170-124">NOTES</span></span>

## <span data-ttu-id="ce170-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce170-125">RELATED LINKS</span></span>

[<span data-ttu-id="ce170-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce170-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="ce170-127">Új – AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce170-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="ce170-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="ce170-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)