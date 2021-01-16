---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335657"
---
# <span data-ttu-id="ea7a6-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ea7a6-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="ea7a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7a6-103">Töröljön egy IoT-központot.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="ea7a6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea7a6-104">SYNTAX</span></span>

### <span data-ttu-id="ea7a6-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea7a6-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7a6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ea7a6-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7a6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ea7a6-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7a6-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea7a6-108">DESCRIPTION</span></span>
<span data-ttu-id="ea7a6-109">Az összes eszköz vagy egy adott eszköz törlése egy Iot-központban.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="ea7a6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea7a6-110">EXAMPLES</span></span>

### <span data-ttu-id="ea7a6-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea7a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="ea7a6-112">Törölje az összes Iot Hub-eszközt.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="ea7a6-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ea7a6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="ea7a6-114">Töröljön egy Iot Hub-eszközt.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="ea7a6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea7a6-115">PARAMETERS</span></span>

### <span data-ttu-id="ea7a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7a6-116">-DefaultProfile</span></span>
<span data-ttu-id="ea7a6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7a6-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ea7a6-118">-DeviceId</span></span>
<span data-ttu-id="ea7a6-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-119">Target Device Id.</span></span>

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

### <span data-ttu-id="ea7a6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea7a6-120">-InputObject</span></span>
<span data-ttu-id="ea7a6-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="ea7a6-121">IotHub object</span></span>

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

### <span data-ttu-id="ea7a6-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ea7a6-122">-IotHubName</span></span>
<span data-ttu-id="ea7a6-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="ea7a6-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ea7a6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea7a6-124">-PassThru</span></span>
<span data-ttu-id="ea7a6-125">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="ea7a6-126">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea7a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="ea7a6-128">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ea7a6-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ea7a6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea7a6-129">-ResourceId</span></span>
<span data-ttu-id="ea7a6-130">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="ea7a6-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ea7a6-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea7a6-131">-Confirm</span></span>
<span data-ttu-id="ea7a6-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7a6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7a6-133">-WhatIf</span></span>
<span data-ttu-id="ea7a6-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7a6-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7a6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7a6-136">CommonParameters</span></span>
<span data-ttu-id="ea7a6-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7a6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7a6-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7a6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7a6-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea7a6-139">INPUTS</span></span>

### <span data-ttu-id="ea7a6-140">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ea7a6-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ea7a6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ea7a6-141">System.String</span></span>

## <span data-ttu-id="ea7a6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea7a6-142">OUTPUTS</span></span>

### <span data-ttu-id="ea7a6-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea7a6-143">System.Boolean</span></span>

## <span data-ttu-id="ea7a6-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea7a6-144">NOTES</span></span>

## <span data-ttu-id="ea7a6-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea7a6-145">RELATED LINKS</span></span>
