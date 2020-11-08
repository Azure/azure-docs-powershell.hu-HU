---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012510"
---
# <span data-ttu-id="ad80e-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ad80e-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="ad80e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad80e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad80e-103">Módosított Azure tűzfal-házirend mentése</span><span class="sxs-lookup"><span data-stu-id="ad80e-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="ad80e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad80e-104">SYNTAX</span></span>

### <span data-ttu-id="ad80e-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad80e-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad80e-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad80e-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad80e-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad80e-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad80e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad80e-108">DESCRIPTION</span></span>
<span data-ttu-id="ad80e-109">A **set-AzFirewallPolicy** parancsmag egy Azure tűzfal-házirendet frissít.</span><span class="sxs-lookup"><span data-stu-id="ad80e-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="ad80e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ad80e-110">EXAMPLES</span></span>

### <span data-ttu-id="ad80e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad80e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="ad80e-112">Ez a példa beállítja a tűzfal házirendjét az új tűzfal házirend-értékkel.</span><span class="sxs-lookup"><span data-stu-id="ad80e-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="ad80e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ad80e-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="ad80e-114">Ebben a példában a tűzfal-házirendet az új veszélyforrás Intel módra állítja be</span><span class="sxs-lookup"><span data-stu-id="ad80e-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="ad80e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad80e-115">PARAMETERS</span></span>

### <span data-ttu-id="ad80e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad80e-116">-AsJob</span></span>
<span data-ttu-id="ad80e-117">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ad80e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad80e-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="ad80e-118">-BasePolicy</span></span>
<span data-ttu-id="ad80e-119">Az alapházirend, amelyet örökölni szeretne</span><span class="sxs-lookup"><span data-stu-id="ad80e-119">The base policy to inherit from</span></span>

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

### <span data-ttu-id="ad80e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad80e-120">-DefaultProfile</span></span>
<span data-ttu-id="ad80e-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad80e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad80e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad80e-122">-InputObject</span></span>
<span data-ttu-id="ad80e-123">A AzureFirewall házirend</span><span class="sxs-lookup"><span data-stu-id="ad80e-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80e-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="ad80e-124">-Location</span></span>
<span data-ttu-id="ad80e-125">helyre.</span><span class="sxs-lookup"><span data-stu-id="ad80e-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80e-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad80e-126">-Name</span></span>
<span data-ttu-id="ad80e-127">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ad80e-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad80e-128">-ResourceGroupName</span></span>
<span data-ttu-id="ad80e-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ad80e-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad80e-130">-ResourceId</span></span>
<span data-ttu-id="ad80e-131">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ad80e-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad80e-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="ad80e-132">-Tag</span></span>
<span data-ttu-id="ad80e-133">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ad80e-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="ad80e-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="ad80e-134">-ThreatIntelMode</span></span>
<span data-ttu-id="ad80e-135">A veszélyforrások felderítésének üzemmódja.</span><span class="sxs-lookup"><span data-stu-id="ad80e-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="ad80e-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad80e-136">-Confirm</span></span>
<span data-ttu-id="ad80e-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad80e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad80e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad80e-138">-WhatIf</span></span>
<span data-ttu-id="ad80e-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad80e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad80e-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad80e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad80e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad80e-141">CommonParameters</span></span>
<span data-ttu-id="ad80e-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad80e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad80e-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad80e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad80e-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad80e-144">INPUTS</span></span>

### <span data-ttu-id="ad80e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ad80e-145">System.String</span></span>

### <span data-ttu-id="ad80e-146">Microsoft. Azure. commands. Network. models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ad80e-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="ad80e-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad80e-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad80e-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad80e-148">OUTPUTS</span></span>

### <span data-ttu-id="ad80e-149">Microsoft. Azure. commands. Network. models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="ad80e-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="ad80e-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad80e-150">NOTES</span></span>

## <span data-ttu-id="ad80e-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad80e-151">RELATED LINKS</span></span>
