---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025149"
---
# <span data-ttu-id="43d00-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="43d00-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="43d00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="43d00-102">SYNOPSIS</span></span>
<span data-ttu-id="43d00-103">Egy Azure-IpAllocation törlése</span><span class="sxs-lookup"><span data-stu-id="43d00-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="43d00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="43d00-104">SYNTAX</span></span>

### <span data-ttu-id="43d00-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43d00-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d00-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43d00-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d00-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43d00-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43d00-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="43d00-108">DESCRIPTION</span></span>
<span data-ttu-id="43d00-109">A **Remove-AzIpAllocation** parancsmag töröl egy Azure-IpAllocation</span><span class="sxs-lookup"><span data-stu-id="43d00-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="43d00-110">Példák</span><span class="sxs-lookup"><span data-stu-id="43d00-110">EXAMPLES</span></span>

### <span data-ttu-id="43d00-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="43d00-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="43d00-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="43d00-112">PARAMETERS</span></span>

### <span data-ttu-id="43d00-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43d00-113">-AsJob</span></span>
<span data-ttu-id="43d00-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="43d00-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43d00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d00-115">-DefaultProfile</span></span>
<span data-ttu-id="43d00-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="43d00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d00-117">-Force</span><span class="sxs-lookup"><span data-stu-id="43d00-117">-Force</span></span>
<span data-ttu-id="43d00-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43d00-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="43d00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d00-119">-InputObject</span></span>
<span data-ttu-id="43d00-120">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="43d00-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43d00-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="43d00-121">-Name</span></span>
<span data-ttu-id="43d00-122">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="43d00-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43d00-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43d00-123">-PassThru</span></span>
<span data-ttu-id="43d00-124">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="43d00-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43d00-125">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="43d00-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43d00-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d00-126">-ResourceGroupName</span></span>
<span data-ttu-id="43d00-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="43d00-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43d00-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43d00-128">-ResourceId</span></span>
<span data-ttu-id="43d00-129">IpAllocation erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="43d00-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43d00-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="43d00-130">-Confirm</span></span>
<span data-ttu-id="43d00-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="43d00-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d00-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d00-132">-WhatIf</span></span>
<span data-ttu-id="43d00-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="43d00-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d00-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="43d00-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d00-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d00-135">CommonParameters</span></span>
<span data-ttu-id="43d00-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="43d00-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d00-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="43d00-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d00-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="43d00-138">INPUTS</span></span>

### <span data-ttu-id="43d00-139">System. String</span><span class="sxs-lookup"><span data-stu-id="43d00-139">System.String</span></span>

## <span data-ttu-id="43d00-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43d00-140">OUTPUTS</span></span>

### <span data-ttu-id="43d00-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43d00-141">System.Boolean</span></span>

## <span data-ttu-id="43d00-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="43d00-142">NOTES</span></span>

## <span data-ttu-id="43d00-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43d00-143">RELATED LINKS</span></span>
