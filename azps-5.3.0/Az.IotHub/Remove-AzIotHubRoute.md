---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386649"
---
# <span data-ttu-id="b3d95-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="b3d95-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="b3d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3d95-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d95-103">Útvonal törlése az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="b3d95-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="b3d95-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3d95-104">SYNTAX</span></span>

### <span data-ttu-id="b3d95-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3d95-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d95-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3d95-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3d95-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b3d95-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3d95-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3d95-108">DESCRIPTION</span></span>
<span data-ttu-id="b3d95-109">Végponthoz való útvonalak törlése</span><span class="sxs-lookup"><span data-stu-id="b3d95-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="b3d95-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3d95-110">EXAMPLES</span></span>

### <span data-ttu-id="b3d95-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b3d95-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="b3d95-112">Törölje az "R1" útvonalat a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="b3d95-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="b3d95-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3d95-113">PARAMETERS</span></span>

### <span data-ttu-id="b3d95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d95-114">-DefaultProfile</span></span>
<span data-ttu-id="b3d95-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3d95-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d95-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3d95-116">-InputObject</span></span>
<span data-ttu-id="b3d95-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="b3d95-117">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d95-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b3d95-118">-Name</span></span>
<span data-ttu-id="b3d95-119">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="b3d95-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d95-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3d95-120">-PassThru</span></span>
<span data-ttu-id="b3d95-121">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="b3d95-121">Allows to return the boolean object.</span></span> <span data-ttu-id="b3d95-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b3d95-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3d95-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d95-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3d95-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b3d95-124">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d95-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3d95-125">-ResourceId</span></span>
<span data-ttu-id="b3d95-126">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b3d95-126">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d95-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="b3d95-127">-RouteName</span></span>
<span data-ttu-id="b3d95-128">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="b3d95-128">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d95-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3d95-129">-Confirm</span></span>
<span data-ttu-id="b3d95-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b3d95-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3d95-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3d95-131">-WhatIf</span></span>
<span data-ttu-id="b3d95-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b3d95-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3d95-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b3d95-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3d95-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d95-134">CommonParameters</span></span>
<span data-ttu-id="b3d95-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d95-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d95-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3d95-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d95-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3d95-137">INPUTS</span></span>

### <span data-ttu-id="b3d95-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b3d95-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b3d95-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b3d95-139">System.String</span></span>

## <span data-ttu-id="b3d95-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3d95-140">OUTPUTS</span></span>

### <span data-ttu-id="b3d95-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3d95-141">System.Boolean</span></span>

## <span data-ttu-id="b3d95-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3d95-142">NOTES</span></span>

## <span data-ttu-id="b3d95-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3d95-143">RELATED LINKS</span></span>
