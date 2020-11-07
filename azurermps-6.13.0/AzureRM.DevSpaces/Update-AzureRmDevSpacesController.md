---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679842"
---
# <span data-ttu-id="4cc5b-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="4cc5b-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="4cc5b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4cc5b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc5b-103">Frissítse a DevSpaces-vezérlőt a címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc5b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4cc5b-104">SYNTAX</span></span>

### <span data-ttu-id="4cc5b-105">DevSpacesControllerNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc5b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc5b-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cc5b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cc5b-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc5b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4cc5b-108">DESCRIPTION</span></span>
<span data-ttu-id="4cc5b-109">Frissítse a DevSpaces-vezérlőt a címkék hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="4cc5b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4cc5b-110">EXAMPLES</span></span>

### <span data-ttu-id="4cc5b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4cc5b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="4cc5b-112">DevSpaces-előfizetőt tartalmazó címke</span><span class="sxs-lookup"><span data-stu-id="4cc5b-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="4cc5b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4cc5b-113">PARAMETERS</span></span>

### <span data-ttu-id="4cc5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc5b-114">-DefaultProfile</span></span>
<span data-ttu-id="4cc5b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc5b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cc5b-116">-InputObject</span></span>
<span data-ttu-id="4cc5b-117">Egy PSController objektum, amely normál esetben áthalad a csővezetéken.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="4cc5b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-118">-Name</span></span>
<span data-ttu-id="4cc5b-119">DevSpaces-vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="4cc5b-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="4cc5b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cc5b-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cc5b-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="4cc5b-121">Resource group name</span></span>

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

### <span data-ttu-id="4cc5b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cc5b-122">-ResourceId</span></span>
<span data-ttu-id="4cc5b-123">A DevSpaces erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="4cc5b-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="4cc5b-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="4cc5b-124">-Tag</span></span>
<span data-ttu-id="4cc5b-125">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4cc5b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4cc5b-126">-Confirm</span></span>
<span data-ttu-id="4cc5b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc5b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc5b-128">-WhatIf</span></span>
<span data-ttu-id="4cc5b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc5b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4cc5b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc5b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc5b-131">CommonParameters</span></span>
<span data-ttu-id="4cc5b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4cc5b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc5b-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc5b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc5b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cc5b-134">INPUTS</span></span>

### <span data-ttu-id="4cc5b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc5b-135">System.String</span></span>

### <span data-ttu-id="4cc5b-136">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="4cc5b-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="4cc5b-137">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4cc5b-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4cc5b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cc5b-138">OUTPUTS</span></span>

### <span data-ttu-id="4cc5b-139">Microsoft. Azure. Command. DevSpaces. models. PSController</span><span class="sxs-lookup"><span data-stu-id="4cc5b-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="4cc5b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4cc5b-140">NOTES</span></span>

## <span data-ttu-id="4cc5b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4cc5b-141">RELATED LINKS</span></span>
