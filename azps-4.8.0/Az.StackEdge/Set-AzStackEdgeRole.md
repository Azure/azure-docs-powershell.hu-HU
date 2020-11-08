---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183204"
---
# <span data-ttu-id="166fc-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="166fc-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="166fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="166fc-102">SYNOPSIS</span></span>
<span data-ttu-id="166fc-103">Egy eszköz szerepkörének frissítése</span><span class="sxs-lookup"><span data-stu-id="166fc-103">Updates a Role for a device</span></span>

## <span data-ttu-id="166fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="166fc-104">SYNTAX</span></span>

### <span data-ttu-id="166fc-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="166fc-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166fc-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="166fc-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="166fc-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="166fc-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="166fc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="166fc-108">DESCRIPTION</span></span>
<span data-ttu-id="166fc-109">A **set-AzStackEdgeRole** parancsmag a IoT szerepkört frissíti egy halom szélén álló eszközön.</span><span class="sxs-lookup"><span data-stu-id="166fc-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="166fc-110">A régi csatlakoztatott megosztásokat az újonnan megadott megosztásnév a megosztásnév paraméterben fogja lecserélni.</span><span class="sxs-lookup"><span data-stu-id="166fc-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="166fc-111">Példák</span><span class="sxs-lookup"><span data-stu-id="166fc-111">EXAMPLES</span></span>

### <span data-ttu-id="166fc-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="166fc-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="166fc-113">A megosztási nevek felülírják a régi csatlakoztatott megosztásokat az újonnan megadottekkel.</span><span class="sxs-lookup"><span data-stu-id="166fc-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="166fc-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="166fc-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="166fc-115">Az összes megosztás leválasztása</span><span class="sxs-lookup"><span data-stu-id="166fc-115">To unmount all shares</span></span>

## <span data-ttu-id="166fc-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="166fc-116">PARAMETERS</span></span>

### <span data-ttu-id="166fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166fc-117">-DefaultProfile</span></span>
<span data-ttu-id="166fc-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="166fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="166fc-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="166fc-119">-DeviceName</span></span>
<span data-ttu-id="166fc-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="166fc-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166fc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="166fc-121">-InputObject</span></span>
<span data-ttu-id="166fc-122">Adja meg a megfelelő eszköz-objektumot</span><span class="sxs-lookup"><span data-stu-id="166fc-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="166fc-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="166fc-123">-Name</span></span>
<span data-ttu-id="166fc-124">A szerepkör neve</span><span class="sxs-lookup"><span data-stu-id="166fc-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166fc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="166fc-125">-ResourceGroupName</span></span>
<span data-ttu-id="166fc-126">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="166fc-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166fc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="166fc-127">-ResourceId</span></span>
<span data-ttu-id="166fc-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="166fc-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166fc-129">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="166fc-129">-ShareName</span></span>
<span data-ttu-id="166fc-130">Megosztás (ok) egy szerepkörben</span><span class="sxs-lookup"><span data-stu-id="166fc-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="166fc-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="166fc-131">-Confirm</span></span>
<span data-ttu-id="166fc-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="166fc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="166fc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="166fc-133">-WhatIf</span></span>
<span data-ttu-id="166fc-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="166fc-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="166fc-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="166fc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="166fc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166fc-136">CommonParameters</span></span>
<span data-ttu-id="166fc-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="166fc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166fc-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="166fc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166fc-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="166fc-139">INPUTS</span></span>

### <span data-ttu-id="166fc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="166fc-140">System.String</span></span>

### <span data-ttu-id="166fc-141">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="166fc-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="166fc-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="166fc-142">OUTPUTS</span></span>

### <span data-ttu-id="166fc-143">Microsoft. Azure. PowerShell. parancsmagok. StackEdge. models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="166fc-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="166fc-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="166fc-144">NOTES</span></span>

## <span data-ttu-id="166fc-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="166fc-145">RELATED LINKS</span></span>
