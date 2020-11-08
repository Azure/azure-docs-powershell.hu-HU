---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184513"
---
# <span data-ttu-id="2cdf4-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="2cdf4-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="2cdf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2cdf4-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdf4-103">Modul (ok) törlése egy IoT-hub IoT-eszközén.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="2cdf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2cdf4-104">SYNTAX</span></span>

### <span data-ttu-id="2cdf4-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2cdf4-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cdf4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2cdf4-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdf4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2cdf4-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cdf4-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2cdf4-108">DESCRIPTION</span></span>
<span data-ttu-id="2cdf4-109">Modul (ok) törlése egy IoT-hub IoT-eszközén.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="2cdf4-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2cdf4-110">EXAMPLES</span></span>

### <span data-ttu-id="2cdf4-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2cdf4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="2cdf4-112">IOT-eszköz modul törlése</span><span class="sxs-lookup"><span data-stu-id="2cdf4-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="2cdf4-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2cdf4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="2cdf4-114">Törölje az összes IOT-eszközt.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="2cdf4-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2cdf4-115">PARAMETERS</span></span>

### <span data-ttu-id="2cdf4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdf4-116">-DefaultProfile</span></span>
<span data-ttu-id="2cdf4-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cdf4-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2cdf4-118">-DeviceId</span></span>
<span data-ttu-id="2cdf4-119">Céleszköz-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-119">Target Device Id.</span></span>

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

### <span data-ttu-id="2cdf4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cdf4-120">-InputObject</span></span>
<span data-ttu-id="2cdf4-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="2cdf4-121">IotHub object</span></span>

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

### <span data-ttu-id="2cdf4-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2cdf4-122">-IotHubName</span></span>
<span data-ttu-id="2cdf4-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="2cdf4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2cdf4-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="2cdf4-124">-ModuleId</span></span>
<span data-ttu-id="2cdf4-125">A cél modul azonosítója</span><span class="sxs-lookup"><span data-stu-id="2cdf4-125">Target Module Id.</span></span>

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

### <span data-ttu-id="2cdf4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cdf4-126">-PassThru</span></span>
<span data-ttu-id="2cdf4-127">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="2cdf4-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2cdf4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cdf4-129">-ResourceGroupName</span></span>
<span data-ttu-id="2cdf4-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2cdf4-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2cdf4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cdf4-131">-ResourceId</span></span>
<span data-ttu-id="2cdf4-132">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2cdf4-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2cdf4-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2cdf4-133">-Confirm</span></span>
<span data-ttu-id="2cdf4-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cdf4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cdf4-135">-WhatIf</span></span>
<span data-ttu-id="2cdf4-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cdf4-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2cdf4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cdf4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdf4-138">CommonParameters</span></span>
<span data-ttu-id="2cdf4-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2cdf4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdf4-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cdf4-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdf4-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cdf4-141">INPUTS</span></span>

### <span data-ttu-id="2cdf4-142">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2cdf4-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2cdf4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2cdf4-143">System.String</span></span>

## <span data-ttu-id="2cdf4-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2cdf4-144">OUTPUTS</span></span>

### <span data-ttu-id="2cdf4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cdf4-145">System.Boolean</span></span>

## <span data-ttu-id="2cdf4-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2cdf4-146">NOTES</span></span>

## <span data-ttu-id="2cdf4-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2cdf4-147">RELATED LINKS</span></span>
