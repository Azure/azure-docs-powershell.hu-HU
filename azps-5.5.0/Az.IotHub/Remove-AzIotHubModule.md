---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203874"
---
# <span data-ttu-id="8d507-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="8d507-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="8d507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d507-102">SYNOPSIS</span></span>
<span data-ttu-id="8d507-103">Modul(ak) törlése egy cél IoT-eszközön az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="8d507-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="8d507-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8d507-104">SYNTAX</span></span>

### <span data-ttu-id="8d507-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8d507-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d507-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8d507-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d507-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8d507-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d507-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8d507-108">DESCRIPTION</span></span>
<span data-ttu-id="8d507-109">Modul(ak) törlése egy cél IoT-eszközön az IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="8d507-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="8d507-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8d507-110">EXAMPLES</span></span>

### <span data-ttu-id="8d507-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="8d507-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="8d507-112">Iot-eszközmodul törlése</span><span class="sxs-lookup"><span data-stu-id="8d507-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="8d507-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8d507-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="8d507-114">Törölje az összes iot eszközmodult.</span><span class="sxs-lookup"><span data-stu-id="8d507-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="8d507-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d507-115">PARAMETERS</span></span>

### <span data-ttu-id="8d507-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d507-116">-DefaultProfile</span></span>
<span data-ttu-id="8d507-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d507-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d507-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8d507-118">-DeviceId</span></span>
<span data-ttu-id="8d507-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8d507-119">Target Device Id.</span></span>

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

### <span data-ttu-id="8d507-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d507-120">-InputObject</span></span>
<span data-ttu-id="8d507-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="8d507-121">IotHub object</span></span>

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

### <span data-ttu-id="8d507-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8d507-122">-IotHubName</span></span>
<span data-ttu-id="8d507-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="8d507-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8d507-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="8d507-124">-ModuleId</span></span>
<span data-ttu-id="8d507-125">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="8d507-125">Target Module Id.</span></span>

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

### <span data-ttu-id="8d507-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d507-126">-PassThru</span></span>
<span data-ttu-id="8d507-127">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="8d507-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="8d507-128">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8d507-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d507-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d507-129">-ResourceGroupName</span></span>
<span data-ttu-id="8d507-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8d507-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8d507-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d507-131">-ResourceId</span></span>
<span data-ttu-id="8d507-132">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="8d507-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8d507-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d507-133">-Confirm</span></span>
<span data-ttu-id="8d507-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8d507-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d507-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d507-135">-WhatIf</span></span>
<span data-ttu-id="8d507-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8d507-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d507-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d507-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d507-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d507-138">CommonParameters</span></span>
<span data-ttu-id="8d507-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d507-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d507-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d507-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d507-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d507-141">INPUTS</span></span>

### <span data-ttu-id="8d507-142">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8d507-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8d507-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8d507-143">System.String</span></span>

## <span data-ttu-id="8d507-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d507-144">OUTPUTS</span></span>

### <span data-ttu-id="8d507-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d507-145">System.Boolean</span></span>

## <span data-ttu-id="8d507-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8d507-146">NOTES</span></span>

## <span data-ttu-id="8d507-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d507-147">RELATED LINKS</span></span>
