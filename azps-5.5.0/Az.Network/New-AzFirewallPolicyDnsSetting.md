---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154298"
---
# <span data-ttu-id="10cb8-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="10cb8-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="10cb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="10cb8-103">Új DNS-beállítást hoz létre az Azure tűzfal házirendhez</span><span class="sxs-lookup"><span data-stu-id="10cb8-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="10cb8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10cb8-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10cb8-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="10cb8-106">A **New-AzFirewallPolicyDnsSetting** parancsmag létrehoz egy DNS-beállításobjektumot az Azure tűzfal házirendhez</span><span class="sxs-lookup"><span data-stu-id="10cb8-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="10cb8-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="10cb8-108">1. Üres házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="10cb8-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="10cb8-109">Ez a példa dns-beállítási objektumot hoz létre a DNS-proxy engedélyezésével.</span><span class="sxs-lookup"><span data-stu-id="10cb8-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="10cb8-110">2. Üres házirend létrehozása a ThreatIntel módban</span><span class="sxs-lookup"><span data-stu-id="10cb8-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="10cb8-111">Ez a példa létrehoz egy DNS Setting objektumot a DNS-proxy engedélyezésével és az egyéni DNS-kiszolgálók beállításával.</span><span class="sxs-lookup"><span data-stu-id="10cb8-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="10cb8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10cb8-112">PARAMETERS</span></span>

### <span data-ttu-id="10cb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10cb8-113">-DefaultProfile</span></span>
<span data-ttu-id="10cb8-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10cb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10cb8-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="10cb8-115">-EnableProxy</span></span>
<span data-ttu-id="10cb8-116">Engedélyezze a DNS-proxyt.</span><span class="sxs-lookup"><span data-stu-id="10cb8-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="10cb8-117">Alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="10cb8-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="10cb8-118">-Server</span><span class="sxs-lookup"><span data-stu-id="10cb8-118">-Server</span></span>
<span data-ttu-id="10cb8-119">A DNS-kiszolgálók listája</span><span class="sxs-lookup"><span data-stu-id="10cb8-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="10cb8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10cb8-120">-Confirm</span></span>
<span data-ttu-id="10cb8-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="10cb8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10cb8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10cb8-122">-WhatIf</span></span>
<span data-ttu-id="10cb8-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="10cb8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10cb8-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10cb8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10cb8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10cb8-125">CommonParameters</span></span>
<span data-ttu-id="10cb8-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10cb8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10cb8-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10cb8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10cb8-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10cb8-128">INPUTS</span></span>

### <span data-ttu-id="10cb8-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="10cb8-129">None</span></span>

## <span data-ttu-id="10cb8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10cb8-130">OUTPUTS</span></span>

### <span data-ttu-id="10cb8-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="10cb8-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="10cb8-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10cb8-132">NOTES</span></span>

## <span data-ttu-id="10cb8-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10cb8-133">RELATED LINKS</span></span>
