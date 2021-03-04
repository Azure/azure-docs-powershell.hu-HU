---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: f3bc819c7050300c82f039981b1df34010771eb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918929"
---
# <span data-ttu-id="e77ed-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="e77ed-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="e77ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e77ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e77ed-103">A peremmodulokat egyetlen él mentén állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="e77ed-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="e77ed-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e77ed-104">SYNTAX</span></span>

### <span data-ttu-id="e77ed-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e77ed-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e77ed-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e77ed-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77ed-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e77ed-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e77ed-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e77ed-108">DESCRIPTION</span></span>
<span data-ttu-id="e77ed-109">A megadott modulkonfigurációs tartalmat alkalmazza a megadott éleszközre.</span><span class="sxs-lookup"><span data-stu-id="e77ed-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="e77ed-110">Megjegyzés: A parancs végrehajtásakor a parancs kimenetként fogja kimenetként használni az eszközre alkalmazott modulok gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="e77ed-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="e77ed-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e77ed-111">EXAMPLES</span></span>

### <span data-ttu-id="e77ed-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="e77ed-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="e77ed-113">Tesztelje az edge modulokat fejlesztés alatt úgy, hogy modulokat ad meg egy céleszközön.</span><span class="sxs-lookup"><span data-stu-id="e77ed-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="e77ed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e77ed-114">PARAMETERS</span></span>

### <span data-ttu-id="e77ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77ed-115">-DefaultProfile</span></span>
<span data-ttu-id="e77ed-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e77ed-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e77ed-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e77ed-117">-DeviceId</span></span>
<span data-ttu-id="e77ed-118">Target Edge eszközazonosító.</span><span class="sxs-lookup"><span data-stu-id="e77ed-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e77ed-119">-InputObject</span></span>
<span data-ttu-id="e77ed-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="e77ed-120">IotHub object</span></span>

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

### <span data-ttu-id="e77ed-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e77ed-121">-IotHubName</span></span>
<span data-ttu-id="e77ed-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="e77ed-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e77ed-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="e77ed-123">-ModulesContent</span></span>
<span data-ttu-id="e77ed-124">Az IoT Edge-eszközökhöz használható modulok konfigurációs tartalma.</span><span class="sxs-lookup"><span data-stu-id="e77ed-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77ed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77ed-125">-ResourceGroupName</span></span>
<span data-ttu-id="e77ed-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e77ed-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e77ed-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e77ed-127">-ResourceId</span></span>
<span data-ttu-id="e77ed-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="e77ed-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e77ed-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e77ed-129">-Confirm</span></span>
<span data-ttu-id="e77ed-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e77ed-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e77ed-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77ed-131">-WhatIf</span></span>
<span data-ttu-id="e77ed-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e77ed-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77ed-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e77ed-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e77ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77ed-134">CommonParameters</span></span>
<span data-ttu-id="e77ed-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e77ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77ed-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e77ed-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77ed-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e77ed-137">INPUTS</span></span>

### <span data-ttu-id="e77ed-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e77ed-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e77ed-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e77ed-139">System.String</span></span>

## <span data-ttu-id="e77ed-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e77ed-140">OUTPUTS</span></span>

### <span data-ttu-id="e77ed-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="e77ed-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="e77ed-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e77ed-142">NOTES</span></span>

## <span data-ttu-id="e77ed-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e77ed-143">RELATED LINKS</span></span>
