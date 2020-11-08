---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188184"
---
# <span data-ttu-id="bab5c-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="bab5c-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="bab5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bab5c-102">SYNOPSIS</span></span>
<span data-ttu-id="bab5c-103">A megadott szabályok érvényesítése a kérelemben felsorolt NSG (ek) ben</span><span class="sxs-lookup"><span data-stu-id="bab5c-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="bab5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bab5c-104">SYNTAX</span></span>

### <span data-ttu-id="bab5c-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bab5c-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bab5c-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="bab5c-106">DESCRIPTION</span></span>
<span data-ttu-id="bab5c-107">A adaptív hálózati edzéseket az Azure Security Center automatikusan számítja ki, ezzel a parancsmaggal a kérésben felsorolt NSG (ek) re kényszeríti a megadott szabályokat.</span><span class="sxs-lookup"><span data-stu-id="bab5c-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="bab5c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bab5c-108">EXAMPLES</span></span>

### <span data-ttu-id="bab5c-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bab5c-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="bab5c-110">A megadott szabályok érvényesítése a kérelemben felsorolt NSG (ek) ben</span><span class="sxs-lookup"><span data-stu-id="bab5c-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="bab5c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bab5c-111">PARAMETERS</span></span>

### <span data-ttu-id="bab5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab5c-112">-DefaultProfile</span></span>
<span data-ttu-id="bab5c-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bab5c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bab5c-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="bab5c-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="bab5c-115">Az adaptív hálózat megkeményedési erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="bab5c-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bab5c-116">-ResourceGroupName</span></span>
<span data-ttu-id="bab5c-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="bab5c-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bab5c-118">-ResourceName</span></span>
<span data-ttu-id="bab5c-119">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="bab5c-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="bab5c-120">-ResourceNamespace</span></span>
<span data-ttu-id="bab5c-121">Az erőforrás névterét.</span><span class="sxs-lookup"><span data-stu-id="bab5c-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bab5c-122">-ResourceType</span></span>
<span data-ttu-id="bab5c-123">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="bab5c-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bab5c-124">-SubscriptionId</span></span>
<span data-ttu-id="bab5c-125">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="bab5c-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-126">-Szabályok</span><span class="sxs-lookup"><span data-stu-id="bab5c-126">-Rules</span></span>
<span data-ttu-id="bab5c-127">Az érvényesíteni kívánt szabályok.</span><span class="sxs-lookup"><span data-stu-id="bab5c-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="bab5c-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="bab5c-129">A hatékony hálózati biztonsági csoportok Azure Resource id azonosítói, amelyek a létrehozott biztonsági szabályokkal fognak frissülni az adaptív hálózat megerősítési szabályaiból.</span><span class="sxs-lookup"><span data-stu-id="bab5c-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bab5c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bab5c-130">-PassThru</span></span>
<span data-ttu-id="bab5c-131">Sikert vagy kudarcot jelző érték visszaadása</span><span class="sxs-lookup"><span data-stu-id="bab5c-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="bab5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab5c-132">CommonParameters</span></span>
<span data-ttu-id="bab5c-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bab5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab5c-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab5c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab5c-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bab5c-135">INPUTS</span></span>

### <span data-ttu-id="bab5c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bab5c-136">System.String</span></span>

### <span data-ttu-id="bab5c-137">Microsoft. Azure. Command. SecurityCenter. models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="bab5c-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="bab5c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bab5c-138">OUTPUTS</span></span>

### <span data-ttu-id="bab5c-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bab5c-139">System.Boolean</span></span>

## <span data-ttu-id="bab5c-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bab5c-140">NOTES</span></span>

## <span data-ttu-id="bab5c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bab5c-141">RELATED LINKS</span></span>