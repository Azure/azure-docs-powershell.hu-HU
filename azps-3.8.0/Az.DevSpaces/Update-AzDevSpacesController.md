---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012368"
---
# <span data-ttu-id="4e73c-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="4e73c-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="4e73c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e73c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e73c-103">Frissítse a DevSpaces-vezérlőt a címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="4e73c-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="4e73c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e73c-104">SYNTAX</span></span>

### <span data-ttu-id="4e73c-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4e73c-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e73c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e73c-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e73c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e73c-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e73c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e73c-108">DESCRIPTION</span></span>
<span data-ttu-id="4e73c-109">Frissítse a DevSpaces-vezérlőt a címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="4e73c-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="4e73c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4e73c-110">EXAMPLES</span></span>

### <span data-ttu-id="4e73c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4e73c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="4e73c-112">DevSpaces-vezérlő címkézése</span><span class="sxs-lookup"><span data-stu-id="4e73c-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="4e73c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e73c-113">PARAMETERS</span></span>

### <span data-ttu-id="4e73c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e73c-114">-DefaultProfile</span></span>
<span data-ttu-id="4e73c-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e73c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e73c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e73c-116">-InputObject</span></span>
<span data-ttu-id="4e73c-117">Egy PSController objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="4e73c-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e73c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4e73c-118">-Name</span></span>
<span data-ttu-id="4e73c-119">DevSpaces-vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="4e73c-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e73c-120">-ResourceGroupName</span></span>
<span data-ttu-id="4e73c-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4e73c-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e73c-122">-ResourceId</span></span>
<span data-ttu-id="4e73c-123">A DevSpaces erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="4e73c-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e73c-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="4e73c-124">-Tag</span></span>
<span data-ttu-id="4e73c-125">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="4e73c-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e73c-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4e73c-126">-Confirm</span></span>
<span data-ttu-id="4e73c-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4e73c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e73c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e73c-128">-WhatIf</span></span>
<span data-ttu-id="4e73c-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4e73c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e73c-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4e73c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e73c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e73c-131">CommonParameters</span></span>
<span data-ttu-id="4e73c-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e73c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e73c-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e73c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e73c-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e73c-134">INPUTS</span></span>

### <span data-ttu-id="4e73c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4e73c-135">System.String</span></span>

### <span data-ttu-id="4e73c-136">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="4e73c-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="4e73c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e73c-137">OUTPUTS</span></span>

### <span data-ttu-id="4e73c-138">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="4e73c-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="4e73c-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e73c-139">NOTES</span></span>

## <span data-ttu-id="4e73c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e73c-140">RELATED LINKS</span></span>
