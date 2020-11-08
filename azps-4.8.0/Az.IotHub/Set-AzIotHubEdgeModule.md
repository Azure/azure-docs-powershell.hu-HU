---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025311"
---
# <span data-ttu-id="97279-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="97279-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="97279-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97279-102">SYNOPSIS</span></span>
<span data-ttu-id="97279-103">Az Edge-modulokat egyetlen Edge-eszközön állítsa be.</span><span class="sxs-lookup"><span data-stu-id="97279-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="97279-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97279-104">SYNTAX</span></span>

### <span data-ttu-id="97279-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97279-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97279-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="97279-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97279-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="97279-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97279-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="97279-108">DESCRIPTION</span></span>
<span data-ttu-id="97279-109">A megadott modul konfigurációs tartalmát alkalmazza a megadott Edge-eszközre.</span><span class="sxs-lookup"><span data-stu-id="97279-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="97279-110">Megjegyzés: a végrehajtáskor a parancs megjeleníti az eszközre alkalmazott modulok gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="97279-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="97279-111">Példák</span><span class="sxs-lookup"><span data-stu-id="97279-111">EXAMPLES</span></span>

### <span data-ttu-id="97279-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97279-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="97279-113">Tesztelje az Edge-modulokat a fejlesztés során, ha egy céleszköz moduljait állít be.</span><span class="sxs-lookup"><span data-stu-id="97279-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="97279-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97279-114">PARAMETERS</span></span>

### <span data-ttu-id="97279-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97279-115">-DefaultProfile</span></span>
<span data-ttu-id="97279-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97279-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97279-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="97279-117">-DeviceId</span></span>
<span data-ttu-id="97279-118">Cél Edge Device id.</span><span class="sxs-lookup"><span data-stu-id="97279-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="97279-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97279-119">-InputObject</span></span>
<span data-ttu-id="97279-120">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="97279-120">IotHub object</span></span>

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

### <span data-ttu-id="97279-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="97279-121">-IotHubName</span></span>
<span data-ttu-id="97279-122">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="97279-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="97279-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="97279-123">-ModulesContent</span></span>
<span data-ttu-id="97279-124">A IoT moduljainak konfigurációs tartalma.</span><span class="sxs-lookup"><span data-stu-id="97279-124">Configuration content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="97279-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97279-125">-ResourceGroupName</span></span>
<span data-ttu-id="97279-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="97279-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="97279-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97279-127">-ResourceId</span></span>
<span data-ttu-id="97279-128">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="97279-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="97279-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97279-129">-Confirm</span></span>
<span data-ttu-id="97279-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97279-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97279-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97279-131">-WhatIf</span></span>
<span data-ttu-id="97279-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97279-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97279-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97279-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97279-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97279-134">CommonParameters</span></span>
<span data-ttu-id="97279-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97279-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97279-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97279-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97279-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97279-137">INPUTS</span></span>

### <span data-ttu-id="97279-138">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="97279-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="97279-139">System. String</span><span class="sxs-lookup"><span data-stu-id="97279-139">System.String</span></span>

## <span data-ttu-id="97279-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97279-140">OUTPUTS</span></span>

### <span data-ttu-id="97279-141">Microsoft. Azure. Command. Management. IotHub. models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="97279-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="97279-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97279-142">NOTES</span></span>

## <span data-ttu-id="97279-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97279-143">RELATED LINKS</span></span>
