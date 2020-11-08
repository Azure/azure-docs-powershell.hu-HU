---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011511"
---
# <span data-ttu-id="c970e-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="c970e-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="c970e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c970e-102">SYNOPSIS</span></span>
<span data-ttu-id="c970e-103">Modul (ok) törlése egy IoT-hub IoT-eszközén.</span><span class="sxs-lookup"><span data-stu-id="c970e-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="c970e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c970e-104">SYNTAX</span></span>

### <span data-ttu-id="c970e-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c970e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c970e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c970e-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c970e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c970e-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c970e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c970e-108">DESCRIPTION</span></span>
<span data-ttu-id="c970e-109">Modul (ok) törlése egy IoT-hub IoT-eszközén.</span><span class="sxs-lookup"><span data-stu-id="c970e-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="c970e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c970e-110">EXAMPLES</span></span>

### <span data-ttu-id="c970e-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c970e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="c970e-112">IOT-eszköz modul törlése</span><span class="sxs-lookup"><span data-stu-id="c970e-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="c970e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c970e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="c970e-114">Törölje az összes IOT-eszközt.</span><span class="sxs-lookup"><span data-stu-id="c970e-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="c970e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c970e-115">PARAMETERS</span></span>

### <span data-ttu-id="c970e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c970e-116">-DefaultProfile</span></span>
<span data-ttu-id="c970e-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c970e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c970e-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c970e-118">-DeviceId</span></span>
<span data-ttu-id="c970e-119">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c970e-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c970e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c970e-120">-InputObject</span></span>
<span data-ttu-id="c970e-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="c970e-121">IotHub object</span></span>

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

### <span data-ttu-id="c970e-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c970e-122">-IotHubName</span></span>
<span data-ttu-id="c970e-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="c970e-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c970e-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="c970e-124">-ModuleId</span></span>
<span data-ttu-id="c970e-125">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="c970e-125">Target Module Id.</span></span>

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

### <span data-ttu-id="c970e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c970e-126">-PassThru</span></span>
<span data-ttu-id="c970e-127">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="c970e-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="c970e-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c970e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c970e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c970e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c970e-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c970e-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c970e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c970e-131">-ResourceId</span></span>
<span data-ttu-id="c970e-132">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="c970e-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c970e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c970e-133">-Confirm</span></span>
<span data-ttu-id="c970e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c970e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c970e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c970e-135">-WhatIf</span></span>
<span data-ttu-id="c970e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c970e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c970e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c970e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c970e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c970e-138">CommonParameters</span></span>
<span data-ttu-id="c970e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c970e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c970e-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c970e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c970e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c970e-141">INPUTS</span></span>

### <span data-ttu-id="c970e-142">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c970e-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c970e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c970e-143">System.String</span></span>

## <span data-ttu-id="c970e-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c970e-144">OUTPUTS</span></span>

### <span data-ttu-id="c970e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c970e-145">System.Boolean</span></span>

## <span data-ttu-id="c970e-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c970e-146">NOTES</span></span>

## <span data-ttu-id="c970e-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c970e-147">RELATED LINKS</span></span>
