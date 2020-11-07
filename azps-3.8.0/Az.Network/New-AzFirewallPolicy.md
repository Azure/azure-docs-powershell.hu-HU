---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 5c432224891de6c2fcadc42ae308e9607bc3e432
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845010"
---
# <span data-ttu-id="eef28-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="eef28-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="eef28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eef28-102">SYNOPSIS</span></span>
<span data-ttu-id="eef28-103">Új Azure tűzfal-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="eef28-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="eef28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eef28-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eef28-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eef28-105">DESCRIPTION</span></span>
<span data-ttu-id="eef28-106">A **New-AzFirewallPolicy** parancsmag Azure tűzfal-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eef28-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="eef28-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eef28-107">EXAMPLES</span></span>

### <span data-ttu-id="eef28-108">1. üres házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="eef28-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="eef28-109">Ez a példa Azure tűzfal-házirendet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="eef28-109">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="eef28-110">2. üres házirend létrehozása a ThreatIntel móddal</span><span class="sxs-lookup"><span data-stu-id="eef28-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="eef28-111">Ez a példa egy Azure tűzfal-házirendet hoz létre egy veszélyforrás Intel móddal</span><span class="sxs-lookup"><span data-stu-id="eef28-111">This example creates an azure firewall policy with a threat intel mode</span></span>

## <span data-ttu-id="eef28-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eef28-112">PARAMETERS</span></span>

### <span data-ttu-id="eef28-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eef28-113">-AsJob</span></span>
<span data-ttu-id="eef28-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="eef28-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eef28-115">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="eef28-115">-BasePolicy</span></span>
<span data-ttu-id="eef28-116">A veszélyforrások felderítésének üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="eef28-116">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef28-117">-DefaultProfile</span></span>
<span data-ttu-id="eef28-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eef28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef28-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eef28-119">-Force</span></span>
<span data-ttu-id="eef28-120">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eef28-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eef28-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="eef28-121">-Location</span></span>
<span data-ttu-id="eef28-122">helyre.</span><span class="sxs-lookup"><span data-stu-id="eef28-122">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef28-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eef28-123">-Name</span></span>
<span data-ttu-id="eef28-124">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="eef28-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef28-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef28-125">-ResourceGroupName</span></span>
<span data-ttu-id="eef28-126">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="eef28-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef28-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="eef28-127">-Tag</span></span>
<span data-ttu-id="eef28-128">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="eef28-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef28-129">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="eef28-129">-ThreatIntelMode</span></span>
<span data-ttu-id="eef28-130">A veszélyforrások felderítésének üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="eef28-130">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eef28-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="eef28-131">-Confirm</span></span>
<span data-ttu-id="eef28-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eef28-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eef28-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eef28-133">-WhatIf</span></span>
<span data-ttu-id="eef28-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="eef28-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eef28-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eef28-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eef28-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef28-136">CommonParameters</span></span>
<span data-ttu-id="eef28-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eef28-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef28-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="eef28-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef28-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eef28-139">INPUTS</span></span>

### <span data-ttu-id="eef28-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eef28-140">System.String</span></span>

### <span data-ttu-id="eef28-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eef28-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eef28-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eef28-142">OUTPUTS</span></span>

### <span data-ttu-id="eef28-143">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="eef28-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="eef28-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eef28-144">NOTES</span></span>

## <span data-ttu-id="eef28-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eef28-145">RELATED LINKS</span></span>
