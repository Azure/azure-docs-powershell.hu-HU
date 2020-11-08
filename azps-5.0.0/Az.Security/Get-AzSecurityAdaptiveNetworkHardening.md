---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187539"
---
# <span data-ttu-id="2e16d-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="2e16d-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="2e16d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e16d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e16d-103">Beolvassa az adaptív hálózati keményedési erőforrások listáját egy kiterjesztett erőforrás hatókörében.</span><span class="sxs-lookup"><span data-stu-id="2e16d-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="2e16d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e16d-104">SYNTAX</span></span>

### <span data-ttu-id="2e16d-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="2e16d-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="2e16d-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e16d-106">DESCRIPTION</span></span>
<span data-ttu-id="2e16d-107">A adaptív hálózati edzéseket az Azure Security Center automatikusan számítja ki, ezzel a parancsmaggal lekérheti a kiterjesztett erőforrás hatókörében található adaptív hálózati erőforrások listáját.</span><span class="sxs-lookup"><span data-stu-id="2e16d-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="2e16d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2e16d-108">EXAMPLES</span></span>

### <span data-ttu-id="2e16d-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e16d-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="2e16d-110">Beolvassa az adaptív hálózati keményedési erőforrások listáját egy kiterjesztett erőforrás hatókörében.</span><span class="sxs-lookup"><span data-stu-id="2e16d-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="2e16d-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="2e16d-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="2e16d-112">Egyetlen adaptív hálózati keményedési erőforrás beszerzése</span><span class="sxs-lookup"><span data-stu-id="2e16d-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="2e16d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e16d-113">PARAMETERS</span></span>

### <span data-ttu-id="2e16d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e16d-114">-DefaultProfile</span></span>
<span data-ttu-id="2e16d-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e16d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e16d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e16d-116">-ResourceGroupName</span></span>
<span data-ttu-id="2e16d-117">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="2e16d-117">Resource group name.</span></span>

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

### <span data-ttu-id="2e16d-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2e16d-118">-ResourceName</span></span>
<span data-ttu-id="2e16d-119">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="2e16d-119">Resource name.</span></span>

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

### <span data-ttu-id="2e16d-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="2e16d-120">-ResourceNamespace</span></span>
<span data-ttu-id="2e16d-121">Az erőforrás névterét.</span><span class="sxs-lookup"><span data-stu-id="2e16d-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="2e16d-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2e16d-122">-ResourceType</span></span>
<span data-ttu-id="2e16d-123">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="2e16d-123">The type of the resource.</span></span>

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

### <span data-ttu-id="2e16d-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="2e16d-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="2e16d-125">Az adaptív hálózat megkeményedési erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="2e16d-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e16d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e16d-126">-SubscriptionId</span></span>
<span data-ttu-id="2e16d-127">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="2e16d-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="2e16d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e16d-128">CommonParameters</span></span>
<span data-ttu-id="2e16d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e16d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e16d-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e16d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e16d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e16d-131">INPUTS</span></span>

### <span data-ttu-id="2e16d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2e16d-132">System.String</span></span>

## <span data-ttu-id="2e16d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e16d-133">OUTPUTS</span></span>

### <span data-ttu-id="2e16d-134">Microsoft. Azure. commands. Security. models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="2e16d-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="2e16d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e16d-135">NOTES</span></span>

## <span data-ttu-id="2e16d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e16d-136">RELATED LINKS</span></span>