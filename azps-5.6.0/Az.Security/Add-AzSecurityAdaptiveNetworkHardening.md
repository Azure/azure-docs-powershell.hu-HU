---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: e0e634a4947953f65c3fd68c9cc3e40dfca17fd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928881"
---
# <span data-ttu-id="00ccf-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="00ccf-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="00ccf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="00ccf-103">A megadott szabályok érvényesítése a kérelemben felsorolt NSG(k) esetén</span><span class="sxs-lookup"><span data-stu-id="00ccf-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="00ccf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00ccf-104">SYNTAX</span></span>

### <span data-ttu-id="00ccf-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00ccf-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ccf-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00ccf-106">DESCRIPTION</span></span>
<span data-ttu-id="00ccf-107">Az Adaptive Network Hardenings számítását automatikusan az Azure Biztonsági központ számítja ki. Ezzel a parancsmaggal kényszeríti a kérelemben felsorolt NSG(k)re vonatkozó szabályokat.</span><span class="sxs-lookup"><span data-stu-id="00ccf-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="00ccf-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00ccf-108">EXAMPLES</span></span>

### <span data-ttu-id="00ccf-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="00ccf-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="00ccf-110">A megadott szabályok érvényesítése a kérelemben felsorolt NSG(k) esetén</span><span class="sxs-lookup"><span data-stu-id="00ccf-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="00ccf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00ccf-111">PARAMETERS</span></span>

### <span data-ttu-id="00ccf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ccf-112">-DefaultProfile</span></span>
<span data-ttu-id="00ccf-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00ccf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00ccf-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="00ccf-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="00ccf-115">Az Adaptive Network Hardening erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="00ccf-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="00ccf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00ccf-116">-ResourceGroupName</span></span>
<span data-ttu-id="00ccf-117">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="00ccf-117">Resource group name.</span></span>

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

### <span data-ttu-id="00ccf-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="00ccf-118">-ResourceName</span></span>
<span data-ttu-id="00ccf-119">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="00ccf-119">Resource name.</span></span>

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

### <span data-ttu-id="00ccf-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="00ccf-120">-ResourceNamespace</span></span>
<span data-ttu-id="00ccf-121">Az erőforrás névtere.</span><span class="sxs-lookup"><span data-stu-id="00ccf-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="00ccf-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="00ccf-122">-ResourceType</span></span>
<span data-ttu-id="00ccf-123">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="00ccf-123">The type of the resource.</span></span>

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

### <span data-ttu-id="00ccf-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00ccf-124">-SubscriptionId</span></span>
<span data-ttu-id="00ccf-125">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="00ccf-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="00ccf-126">-Rules</span><span class="sxs-lookup"><span data-stu-id="00ccf-126">-Rules</span></span>
<span data-ttu-id="00ccf-127">Az érvényesíthető szabályok.</span><span class="sxs-lookup"><span data-stu-id="00ccf-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="00ccf-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="00ccf-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="00ccf-129">A hatékony hálózati biztonsági csoportok Azure-erőforrás-adatokatói, amelyek frissítve lesznek az Adaptive Network hardening (Adaptive Network Hardening) szabályok által létrehozott biztonsági szabályokkal.</span><span class="sxs-lookup"><span data-stu-id="00ccf-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="00ccf-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00ccf-130">-PassThru</span></span>
<span data-ttu-id="00ccf-131">Sikeres vagy sikertelenséget jelző értéket ad vissza</span><span class="sxs-lookup"><span data-stu-id="00ccf-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="00ccf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ccf-132">CommonParameters</span></span>
<span data-ttu-id="00ccf-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ccf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ccf-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ccf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ccf-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00ccf-135">INPUTS</span></span>

### <span data-ttu-id="00ccf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="00ccf-136">System.String</span></span>

### <span data-ttu-id="00ccf-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="00ccf-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="00ccf-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00ccf-138">OUTPUTS</span></span>

### <span data-ttu-id="00ccf-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00ccf-139">System.Boolean</span></span>

## <span data-ttu-id="00ccf-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00ccf-140">NOTES</span></span>

## <span data-ttu-id="00ccf-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00ccf-141">RELATED LINKS</span></span>