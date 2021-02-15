---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152867"
---
# <span data-ttu-id="be574-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="be574-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="be574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be574-102">SYNOPSIS</span></span>
<span data-ttu-id="be574-103">Útvonal törlése az IoT-központban</span><span class="sxs-lookup"><span data-stu-id="be574-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="be574-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="be574-104">SYNTAX</span></span>

### <span data-ttu-id="be574-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be574-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be574-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="be574-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be574-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="be574-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be574-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="be574-108">DESCRIPTION</span></span>
<span data-ttu-id="be574-109">Végponthoz való útvonalak törlése</span><span class="sxs-lookup"><span data-stu-id="be574-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="be574-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="be574-110">EXAMPLES</span></span>

### <span data-ttu-id="be574-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="be574-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="be574-112">Törölje az "R1" útvonalat a "myiothub" IoT-központból.</span><span class="sxs-lookup"><span data-stu-id="be574-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="be574-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be574-113">PARAMETERS</span></span>

### <span data-ttu-id="be574-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be574-114">-DefaultProfile</span></span>
<span data-ttu-id="be574-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be574-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be574-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be574-116">-InputObject</span></span>
<span data-ttu-id="be574-117">IotHub-objektum</span><span class="sxs-lookup"><span data-stu-id="be574-117">IotHub Object</span></span>

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

### <span data-ttu-id="be574-118">-Name</span><span class="sxs-lookup"><span data-stu-id="be574-118">-Name</span></span>
<span data-ttu-id="be574-119">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="be574-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="be574-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be574-120">-PassThru</span></span>
<span data-ttu-id="be574-121">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="be574-121">Allows to return the boolean object.</span></span> <span data-ttu-id="be574-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="be574-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be574-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be574-123">-ResourceGroupName</span></span>
<span data-ttu-id="be574-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="be574-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="be574-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be574-125">-ResourceId</span></span>
<span data-ttu-id="be574-126">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="be574-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="be574-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="be574-127">-RouteName</span></span>
<span data-ttu-id="be574-128">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="be574-128">Name of the Route</span></span>

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

### <span data-ttu-id="be574-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be574-129">-Confirm</span></span>
<span data-ttu-id="be574-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="be574-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be574-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be574-131">-WhatIf</span></span>
<span data-ttu-id="be574-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="be574-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be574-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be574-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be574-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be574-134">CommonParameters</span></span>
<span data-ttu-id="be574-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be574-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be574-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be574-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be574-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be574-137">INPUTS</span></span>

### <span data-ttu-id="be574-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="be574-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="be574-139">System.String</span><span class="sxs-lookup"><span data-stu-id="be574-139">System.String</span></span>

## <span data-ttu-id="be574-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be574-140">OUTPUTS</span></span>

### <span data-ttu-id="be574-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be574-141">System.Boolean</span></span>

## <span data-ttu-id="be574-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="be574-142">NOTES</span></span>

## <span data-ttu-id="be574-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be574-143">RELATED LINKS</span></span>
