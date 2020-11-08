---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185334"
---
# <span data-ttu-id="e7564-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7564-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="e7564-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7564-102">SYNOPSIS</span></span>
<span data-ttu-id="e7564-103">IoT-eszköz konfigurációjának törlése</span><span class="sxs-lookup"><span data-stu-id="e7564-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="e7564-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7564-104">SYNTAX</span></span>

### <span data-ttu-id="e7564-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e7564-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7564-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e7564-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7564-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e7564-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7564-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7564-108">DESCRIPTION</span></span>
<span data-ttu-id="e7564-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementTovábbi információt itt talál.</span><span class="sxs-lookup"><span data-stu-id="e7564-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="e7564-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e7564-110">EXAMPLES</span></span>

### <span data-ttu-id="e7564-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e7564-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="e7564-112">IoT-eszköz konfigurációjának törlése</span><span class="sxs-lookup"><span data-stu-id="e7564-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="e7564-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7564-113">PARAMETERS</span></span>

### <span data-ttu-id="e7564-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7564-114">-DefaultProfile</span></span>
<span data-ttu-id="e7564-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e7564-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7564-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7564-116">-InputObject</span></span>
<span data-ttu-id="e7564-117">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="e7564-117">IotHub object</span></span>

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

### <span data-ttu-id="e7564-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e7564-118">-IotHubName</span></span>
<span data-ttu-id="e7564-119">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="e7564-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e7564-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e7564-120">-Name</span></span>
<span data-ttu-id="e7564-121">A konfiguráció azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e7564-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="e7564-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7564-122">-PassThru</span></span>
<span data-ttu-id="e7564-123">Lehetővé teszi a logikai objektum visszaadását.</span><span class="sxs-lookup"><span data-stu-id="e7564-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="e7564-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e7564-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7564-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7564-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7564-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e7564-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e7564-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7564-127">-ResourceId</span></span>
<span data-ttu-id="e7564-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e7564-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e7564-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e7564-129">-Confirm</span></span>
<span data-ttu-id="e7564-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e7564-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7564-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7564-131">-WhatIf</span></span>
<span data-ttu-id="e7564-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e7564-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7564-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e7564-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7564-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7564-134">CommonParameters</span></span>
<span data-ttu-id="e7564-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7564-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7564-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7564-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7564-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7564-137">INPUTS</span></span>

### <span data-ttu-id="e7564-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e7564-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e7564-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e7564-139">System.String</span></span>

## <span data-ttu-id="e7564-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7564-140">OUTPUTS</span></span>

### <span data-ttu-id="e7564-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7564-141">System.Boolean</span></span>

## <span data-ttu-id="e7564-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7564-142">NOTES</span></span>

## <span data-ttu-id="e7564-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7564-143">RELATED LINKS</span></span>
