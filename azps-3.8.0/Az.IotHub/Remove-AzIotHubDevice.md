---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013799"
---
# <span data-ttu-id="83020-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="83020-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="83020-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83020-102">SYNOPSIS</span></span>
<span data-ttu-id="83020-103">IoT-hub eszköz törlése</span><span class="sxs-lookup"><span data-stu-id="83020-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="83020-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83020-104">SYNTAX</span></span>

### <span data-ttu-id="83020-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="83020-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83020-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="83020-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83020-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="83020-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83020-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="83020-108">DESCRIPTION</span></span>
<span data-ttu-id="83020-109">Az összes eszköz vagy egy adott eszköz törlése egy IOT-hub-ról</span><span class="sxs-lookup"><span data-stu-id="83020-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="83020-110">Példák</span><span class="sxs-lookup"><span data-stu-id="83020-110">EXAMPLES</span></span>

### <span data-ttu-id="83020-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="83020-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="83020-112">Törölje az összes IOT hub-eszközt.</span><span class="sxs-lookup"><span data-stu-id="83020-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="83020-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="83020-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="83020-114">IOT-hub eszköz törlése</span><span class="sxs-lookup"><span data-stu-id="83020-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="83020-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83020-115">PARAMETERS</span></span>

### <span data-ttu-id="83020-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83020-116">-DefaultProfile</span></span>
<span data-ttu-id="83020-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83020-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83020-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="83020-118">-DeviceId</span></span>
<span data-ttu-id="83020-119">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="83020-119">Target Device Id.</span></span>

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

### <span data-ttu-id="83020-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83020-120">-InputObject</span></span>
<span data-ttu-id="83020-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="83020-121">IotHub object</span></span>

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

### <span data-ttu-id="83020-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="83020-122">-IotHubName</span></span>
<span data-ttu-id="83020-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="83020-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="83020-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83020-124">-PassThru</span></span>
<span data-ttu-id="83020-125">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="83020-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="83020-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="83020-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83020-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83020-127">-ResourceGroupName</span></span>
<span data-ttu-id="83020-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="83020-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="83020-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83020-129">-ResourceId</span></span>
<span data-ttu-id="83020-130">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="83020-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="83020-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="83020-131">-Confirm</span></span>
<span data-ttu-id="83020-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="83020-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83020-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83020-133">-WhatIf</span></span>
<span data-ttu-id="83020-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="83020-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83020-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83020-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83020-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83020-136">CommonParameters</span></span>
<span data-ttu-id="83020-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83020-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83020-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83020-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83020-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83020-139">INPUTS</span></span>

### <span data-ttu-id="83020-140">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="83020-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="83020-141">System. String</span><span class="sxs-lookup"><span data-stu-id="83020-141">System.String</span></span>

## <span data-ttu-id="83020-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83020-142">OUTPUTS</span></span>

### <span data-ttu-id="83020-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83020-143">System.Boolean</span></span>

## <span data-ttu-id="83020-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83020-144">NOTES</span></span>

## <span data-ttu-id="83020-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83020-145">RELATED LINKS</span></span>
