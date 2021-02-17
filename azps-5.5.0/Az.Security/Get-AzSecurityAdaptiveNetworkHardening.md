---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208343"
---
# <span data-ttu-id="42e67-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="42e67-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="42e67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42e67-102">SYNOPSIS</span></span>
<span data-ttu-id="42e67-103">Az Adaptive Network Hardenings erőforrások listája egy kiterjesztett erőforrás hatókörében.</span><span class="sxs-lookup"><span data-stu-id="42e67-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="42e67-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="42e67-104">SYNTAX</span></span>

### <span data-ttu-id="42e67-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="42e67-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="42e67-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="42e67-106">DESCRIPTION</span></span>
<span data-ttu-id="42e67-107">Az Adaptive Network Hardenings erőforrást az Azure Biztonsági központ automatikusan kiszámítja. Ezzel a parancsmaggal lekérte az Adaptive Network Hardenings erőforrások listáját egy kiterjesztett erőforrásra terjedve.</span><span class="sxs-lookup"><span data-stu-id="42e67-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="42e67-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="42e67-108">EXAMPLES</span></span>

### <span data-ttu-id="42e67-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="42e67-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="42e67-110">Az Adaptive Network Hardenings erőforrások listája egy kiterjesztett erőforrás hatókörében.</span><span class="sxs-lookup"><span data-stu-id="42e67-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="42e67-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="42e67-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="42e67-112">Adaptive Network Hardenings erőforrás</span><span class="sxs-lookup"><span data-stu-id="42e67-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="42e67-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42e67-113">PARAMETERS</span></span>

### <span data-ttu-id="42e67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e67-114">-DefaultProfile</span></span>
<span data-ttu-id="42e67-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="42e67-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42e67-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42e67-116">-ResourceGroupName</span></span>
<span data-ttu-id="42e67-117">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="42e67-117">Resource group name.</span></span>

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

### <span data-ttu-id="42e67-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="42e67-118">-ResourceName</span></span>
<span data-ttu-id="42e67-119">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="42e67-119">Resource name.</span></span>

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

### <span data-ttu-id="42e67-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="42e67-120">-ResourceNamespace</span></span>
<span data-ttu-id="42e67-121">Az erőforrás névtere.</span><span class="sxs-lookup"><span data-stu-id="42e67-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="42e67-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="42e67-122">-ResourceType</span></span>
<span data-ttu-id="42e67-123">Az erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="42e67-123">The type of the resource.</span></span>

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

### <span data-ttu-id="42e67-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="42e67-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="42e67-125">Az Adaptive Network Hardening erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="42e67-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="42e67-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42e67-126">-SubscriptionId</span></span>
<span data-ttu-id="42e67-127">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="42e67-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="42e67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e67-128">CommonParameters</span></span>
<span data-ttu-id="42e67-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e67-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e67-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e67-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42e67-131">INPUTS</span></span>

### <span data-ttu-id="42e67-132">System.String</span><span class="sxs-lookup"><span data-stu-id="42e67-132">System.String</span></span>

## <span data-ttu-id="42e67-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42e67-133">OUTPUTS</span></span>

### <span data-ttu-id="42e67-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="42e67-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="42e67-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="42e67-135">NOTES</span></span>

## <span data-ttu-id="42e67-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42e67-136">RELATED LINKS</span></span>