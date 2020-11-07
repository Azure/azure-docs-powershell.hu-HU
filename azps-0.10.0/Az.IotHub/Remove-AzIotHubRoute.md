---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 1066c922e24f8a521ac7a52bab437812a7733021
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842194"
---
# <span data-ttu-id="2f271-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="2f271-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="2f271-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f271-102">SYNOPSIS</span></span>
<span data-ttu-id="2f271-103">Útvonal törlése az IoT hub-ban</span><span class="sxs-lookup"><span data-stu-id="2f271-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="2f271-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f271-104">SYNTAX</span></span>

### <span data-ttu-id="2f271-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f271-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f271-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2f271-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f271-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2f271-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f271-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f271-108">DESCRIPTION</span></span>
<span data-ttu-id="2f271-109">Útvonalak törlése végpontra</span><span class="sxs-lookup"><span data-stu-id="2f271-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="2f271-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2f271-110">EXAMPLES</span></span>

### <span data-ttu-id="2f271-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f271-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="2f271-112">Az "R1" útvonal törlése a "myiothub" IoT hub-ról</span><span class="sxs-lookup"><span data-stu-id="2f271-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="2f271-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f271-113">PARAMETERS</span></span>

### <span data-ttu-id="2f271-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f271-114">-DefaultProfile</span></span>
<span data-ttu-id="2f271-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f271-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f271-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f271-116">-InputObject</span></span>
<span data-ttu-id="2f271-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="2f271-117">IotHub Object</span></span>

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

### <span data-ttu-id="2f271-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f271-118">-Name</span></span>
<span data-ttu-id="2f271-119">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="2f271-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2f271-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f271-120">-PassThru</span></span>
<span data-ttu-id="2f271-121">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="2f271-121">Allows to return the boolean object.</span></span> <span data-ttu-id="2f271-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2f271-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f271-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f271-123">-ResourceGroupName</span></span>
<span data-ttu-id="2f271-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2f271-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2f271-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f271-125">-ResourceId</span></span>
<span data-ttu-id="2f271-126">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2f271-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2f271-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="2f271-127">-RouteName</span></span>
<span data-ttu-id="2f271-128">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="2f271-128">Name of the Route</span></span>

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

### <span data-ttu-id="2f271-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f271-129">-Confirm</span></span>
<span data-ttu-id="2f271-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f271-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f271-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f271-131">-WhatIf</span></span>
<span data-ttu-id="2f271-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f271-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f271-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f271-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f271-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f271-134">CommonParameters</span></span>
<span data-ttu-id="2f271-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f271-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f271-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f271-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f271-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f271-137">INPUTS</span></span>

### <span data-ttu-id="2f271-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2f271-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2f271-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2f271-139">System.String</span></span>

## <span data-ttu-id="2f271-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f271-140">OUTPUTS</span></span>

### <span data-ttu-id="2f271-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f271-141">System.Boolean</span></span>

## <span data-ttu-id="2f271-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f271-142">NOTES</span></span>

## <span data-ttu-id="2f271-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f271-143">RELATED LINKS</span></span>
