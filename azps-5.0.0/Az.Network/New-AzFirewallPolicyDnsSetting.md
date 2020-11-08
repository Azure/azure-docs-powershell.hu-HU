---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195373"
---
# <span data-ttu-id="b1450-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="b1450-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="b1450-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1450-102">SYNOPSIS</span></span>
<span data-ttu-id="b1450-103">Új DNS-beállítás létrehozása az Azure tűzfal házirendjéhez</span><span class="sxs-lookup"><span data-stu-id="b1450-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="b1450-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1450-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1450-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1450-105">DESCRIPTION</span></span>
<span data-ttu-id="b1450-106">A **New-AzFirewallPolicyDnsSetting** parancsmag létrehoz egy DNS-beállítási objektumot az Azure tűzfal házirendjéhez</span><span class="sxs-lookup"><span data-stu-id="b1450-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="b1450-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1450-107">EXAMPLES</span></span>

### <span data-ttu-id="b1450-108">1. üres házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="b1450-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="b1450-109">Ebben a példában egy DNS-beállítási objektum jön létre, amelyben a DNS-proxy engedélyezve van.</span><span class="sxs-lookup"><span data-stu-id="b1450-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="b1450-110">2. üres házirend létrehozása a ThreatIntel móddal</span><span class="sxs-lookup"><span data-stu-id="b1450-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="b1450-111">Ez a példa létrehoz egy DNS-beállítási objektumot, amely lehetővé teszi a DNS-proxy beállítását és az egyéni DNS-kiszolgálók beállítását.</span><span class="sxs-lookup"><span data-stu-id="b1450-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="b1450-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1450-112">PARAMETERS</span></span>

### <span data-ttu-id="b1450-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1450-113">-DefaultProfile</span></span>
<span data-ttu-id="b1450-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b1450-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1450-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="b1450-115">-EnableProxy</span></span>
<span data-ttu-id="b1450-116">Engedélyezze a DNS-proxyt.</span><span class="sxs-lookup"><span data-stu-id="b1450-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="b1450-117">Alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="b1450-117">By default it is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1450-118">-Server</span><span class="sxs-lookup"><span data-stu-id="b1450-118">-Server</span></span>
<span data-ttu-id="b1450-119">A DNS-kiszolgálók listája</span><span class="sxs-lookup"><span data-stu-id="b1450-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="b1450-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b1450-120">-Confirm</span></span>
<span data-ttu-id="b1450-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b1450-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1450-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1450-122">-WhatIf</span></span>
<span data-ttu-id="b1450-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b1450-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1450-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b1450-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1450-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1450-125">CommonParameters</span></span>
<span data-ttu-id="b1450-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1450-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1450-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b1450-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1450-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1450-128">INPUTS</span></span>

### <span data-ttu-id="b1450-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="b1450-129">None</span></span>

## <span data-ttu-id="b1450-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1450-130">OUTPUTS</span></span>

### <span data-ttu-id="b1450-131">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="b1450-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="b1450-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1450-132">NOTES</span></span>

## <span data-ttu-id="b1450-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1450-133">RELATED LINKS</span></span>
