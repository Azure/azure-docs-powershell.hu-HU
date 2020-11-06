---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
ms.openlocfilehash: 9af711bd449bc8c69808f30dc99ceea806dee00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503656"
---
# <span data-ttu-id="3670f-101">Remove-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="3670f-101">Remove-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="3670f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3670f-102">SYNOPSIS</span></span>
<span data-ttu-id="3670f-103">Útvonal törlése az IoT hub-ban</span><span class="sxs-lookup"><span data-stu-id="3670f-103">Delete a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3670f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3670f-104">SYNTAX</span></span>

### <span data-ttu-id="3670f-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3670f-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3670f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3670f-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3670f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3670f-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3670f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3670f-108">DESCRIPTION</span></span>
<span data-ttu-id="3670f-109">Útvonalak törlése végpontra</span><span class="sxs-lookup"><span data-stu-id="3670f-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="3670f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3670f-110">EXAMPLES</span></span>

### <span data-ttu-id="3670f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3670f-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="3670f-112">Az "R1" útvonal törlése a "myiothub" IoT hub-ról</span><span class="sxs-lookup"><span data-stu-id="3670f-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="3670f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3670f-113">PARAMETERS</span></span>

### <span data-ttu-id="3670f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3670f-114">-DefaultProfile</span></span>
<span data-ttu-id="3670f-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3670f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3670f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3670f-116">-InputObject</span></span>
<span data-ttu-id="3670f-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="3670f-117">IotHub Object</span></span>

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

### <span data-ttu-id="3670f-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3670f-118">-Name</span></span>
<span data-ttu-id="3670f-119">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="3670f-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3670f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3670f-120">-PassThru</span></span>
<span data-ttu-id="3670f-121">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="3670f-121">Allows to return the boolean object.</span></span> <span data-ttu-id="3670f-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3670f-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3670f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3670f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3670f-124">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3670f-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3670f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3670f-125">-ResourceId</span></span>
<span data-ttu-id="3670f-126">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="3670f-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3670f-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="3670f-127">-RouteName</span></span>
<span data-ttu-id="3670f-128">Az útvonal neve</span><span class="sxs-lookup"><span data-stu-id="3670f-128">Name of the Route</span></span>

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

### <span data-ttu-id="3670f-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3670f-129">-Confirm</span></span>
<span data-ttu-id="3670f-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3670f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3670f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3670f-131">-WhatIf</span></span>
<span data-ttu-id="3670f-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3670f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3670f-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3670f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3670f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3670f-134">CommonParameters</span></span>
<span data-ttu-id="3670f-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3670f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3670f-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3670f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3670f-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3670f-137">INPUTS</span></span>

### <span data-ttu-id="3670f-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3670f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="3670f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3670f-139">System.String</span></span>

## <span data-ttu-id="3670f-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3670f-140">OUTPUTS</span></span>

### <span data-ttu-id="3670f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3670f-141">System.Boolean</span></span>

## <span data-ttu-id="3670f-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3670f-142">NOTES</span></span>

## <span data-ttu-id="3670f-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3670f-143">RELATED LINKS</span></span>
