---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147738"
---
# <span data-ttu-id="ed954-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="ed954-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="ed954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed954-102">SYNOPSIS</span></span>
<span data-ttu-id="ed954-103">A peremmodulok beállítása egyetlen élen található eszközön.</span><span class="sxs-lookup"><span data-stu-id="ed954-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="ed954-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ed954-104">SYNTAX</span></span>

### <span data-ttu-id="ed954-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ed954-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed954-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed954-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed954-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ed954-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed954-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ed954-108">DESCRIPTION</span></span>
<span data-ttu-id="ed954-109">A megadott modulkonfigurációs tartalmat alkalmazza a megadott éleszközre.</span><span class="sxs-lookup"><span data-stu-id="ed954-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="ed954-110">Megjegyzés: A parancs végrehajtásakor a parancs kimenetként fogja kimenetként használni az eszközre alkalmazott modulok gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="ed954-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="ed954-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ed954-111">EXAMPLES</span></span>

### <span data-ttu-id="ed954-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ed954-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="ed954-113">Tesztelje a peremmodulokat fejlesztés alatt úgy, hogy modulokat ad meg egy céleszközön.</span><span class="sxs-lookup"><span data-stu-id="ed954-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="ed954-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed954-114">PARAMETERS</span></span>

### <span data-ttu-id="ed954-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed954-115">-DefaultProfile</span></span>
<span data-ttu-id="ed954-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ed954-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed954-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ed954-117">-DeviceId</span></span>
<span data-ttu-id="ed954-118">Target Edge eszközazonosító.</span><span class="sxs-lookup"><span data-stu-id="ed954-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="ed954-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed954-119">-InputObject</span></span>
<span data-ttu-id="ed954-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="ed954-120">IotHub object</span></span>

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

### <span data-ttu-id="ed954-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ed954-121">-IotHubName</span></span>
<span data-ttu-id="ed954-122">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="ed954-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ed954-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="ed954-123">-ModulesContent</span></span>
<span data-ttu-id="ed954-124">Az IoT Edge-eszközökhöz használható modulok konfigurációs tartalma.</span><span class="sxs-lookup"><span data-stu-id="ed954-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="ed954-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed954-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed954-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ed954-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ed954-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed954-127">-ResourceId</span></span>
<span data-ttu-id="ed954-128">IotHub erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ed954-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ed954-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed954-129">-Confirm</span></span>
<span data-ttu-id="ed954-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ed954-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed954-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed954-131">-WhatIf</span></span>
<span data-ttu-id="ed954-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ed954-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed954-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ed954-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed954-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed954-134">CommonParameters</span></span>
<span data-ttu-id="ed954-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed954-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed954-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed954-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed954-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed954-137">INPUTS</span></span>

### <span data-ttu-id="ed954-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ed954-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ed954-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ed954-139">System.String</span></span>

## <span data-ttu-id="ed954-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ed954-140">OUTPUTS</span></span>

### <span data-ttu-id="ed954-141">Microsoft.Azure.Commands.Management.iotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="ed954-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="ed954-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ed954-142">NOTES</span></span>

## <span data-ttu-id="ed954-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ed954-143">RELATED LINKS</span></span>
