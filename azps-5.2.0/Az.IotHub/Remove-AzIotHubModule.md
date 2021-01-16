---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322401"
---
# <span data-ttu-id="b511d-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="b511d-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="b511d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b511d-102">SYNOPSIS</span></span>
<span data-ttu-id="b511d-103">Modul(ak) törlése egy cél IoT-eszközön egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="b511d-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b511d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b511d-104">SYNTAX</span></span>

### <span data-ttu-id="b511d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b511d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b511d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b511d-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b511d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b511d-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b511d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b511d-108">DESCRIPTION</span></span>
<span data-ttu-id="b511d-109">Modul(ak) törlése egy cél IoT-eszközön egy IoT-központban.</span><span class="sxs-lookup"><span data-stu-id="b511d-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="b511d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b511d-110">EXAMPLES</span></span>

### <span data-ttu-id="b511d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b511d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="b511d-112">Iot-eszközmodul törlése</span><span class="sxs-lookup"><span data-stu-id="b511d-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="b511d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b511d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="b511d-114">Törölje az összes iot eszközmodult.</span><span class="sxs-lookup"><span data-stu-id="b511d-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="b511d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b511d-115">PARAMETERS</span></span>

### <span data-ttu-id="b511d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b511d-116">-DefaultProfile</span></span>
<span data-ttu-id="b511d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b511d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b511d-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b511d-118">-DeviceId</span></span>
<span data-ttu-id="b511d-119">Céleszköz azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b511d-119">Target Device Id.</span></span>

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

### <span data-ttu-id="b511d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b511d-120">-InputObject</span></span>
<span data-ttu-id="b511d-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="b511d-121">IotHub object</span></span>

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

### <span data-ttu-id="b511d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b511d-122">-IotHubName</span></span>
<span data-ttu-id="b511d-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="b511d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b511d-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="b511d-124">-ModuleId</span></span>
<span data-ttu-id="b511d-125">Célmodul-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b511d-125">Target Module Id.</span></span>

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

### <span data-ttu-id="b511d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b511d-126">-PassThru</span></span>
<span data-ttu-id="b511d-127">Visszaadja a logikai objektumot.</span><span class="sxs-lookup"><span data-stu-id="b511d-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="b511d-128">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b511d-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b511d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b511d-129">-ResourceGroupName</span></span>
<span data-ttu-id="b511d-130">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b511d-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b511d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b511d-131">-ResourceId</span></span>
<span data-ttu-id="b511d-132">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="b511d-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b511d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b511d-133">-Confirm</span></span>
<span data-ttu-id="b511d-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b511d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b511d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b511d-135">-WhatIf</span></span>
<span data-ttu-id="b511d-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b511d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b511d-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b511d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b511d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b511d-138">CommonParameters</span></span>
<span data-ttu-id="b511d-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b511d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b511d-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b511d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b511d-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b511d-141">INPUTS</span></span>

### <span data-ttu-id="b511d-142">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b511d-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b511d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b511d-143">System.String</span></span>

## <span data-ttu-id="b511d-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b511d-144">OUTPUTS</span></span>

### <span data-ttu-id="b511d-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b511d-145">System.Boolean</span></span>

## <span data-ttu-id="b511d-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b511d-146">NOTES</span></span>

## <span data-ttu-id="b511d-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b511d-147">RELATED LINKS</span></span>
