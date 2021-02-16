---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 71e1cd6ea8f7aaa228ccdc5032971decfb21b2f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166138"
---
# <span data-ttu-id="3cf75-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3cf75-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="3cf75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf75-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf75-103">Egy eszköz szerepkörének frissítése</span><span class="sxs-lookup"><span data-stu-id="3cf75-103">Updates a Role for a device</span></span>

## <span data-ttu-id="3cf75-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3cf75-104">SYNTAX</span></span>

### <span data-ttu-id="3cf75-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3cf75-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf75-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf75-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf75-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cf75-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf75-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3cf75-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf75-109">A **Set-AzDataBoxEdgeRole** parancsmag frissíti egy IoT-szerepkört egy Data Box Edge-eszközön.</span><span class="sxs-lookup"><span data-stu-id="3cf75-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="3cf75-110">A régi telepített megosztásokat felváltja a ShareName paraméterben újonnan megadottak.</span><span class="sxs-lookup"><span data-stu-id="3cf75-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="3cf75-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3cf75-111">EXAMPLES</span></span>

### <span data-ttu-id="3cf75-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3cf75-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="3cf75-113">A Megosztásnevek helyére a régi telepített megosztások az újonnan hozzáadott megosztások lesznek.</span><span class="sxs-lookup"><span data-stu-id="3cf75-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="3cf75-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3cf75-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="3cf75-115">Az összes megosztás leválasztása</span><span class="sxs-lookup"><span data-stu-id="3cf75-115">To unmount all shares</span></span>

## <span data-ttu-id="3cf75-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cf75-116">PARAMETERS</span></span>

### <span data-ttu-id="3cf75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf75-117">-DefaultProfile</span></span>
<span data-ttu-id="3cf75-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3cf75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf75-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3cf75-119">-DeviceName</span></span>
<span data-ttu-id="3cf75-120">Eszköz neve</span><span class="sxs-lookup"><span data-stu-id="3cf75-120">Device Name</span></span>

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

### <span data-ttu-id="3cf75-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cf75-121">-InputObject</span></span>
<span data-ttu-id="3cf75-122">Kérjük, adja meg a megfelelő eszközobjektumot</span><span class="sxs-lookup"><span data-stu-id="3cf75-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf75-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3cf75-123">-Name</span></span>
<span data-ttu-id="3cf75-124">A szerepkör neve</span><span class="sxs-lookup"><span data-stu-id="3cf75-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf75-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf75-125">-ResourceGroupName</span></span>
<span data-ttu-id="3cf75-126">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3cf75-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3cf75-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf75-127">-ResourceId</span></span>
<span data-ttu-id="3cf75-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf75-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="3cf75-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3cf75-129">-ShareName</span></span>
<span data-ttu-id="3cf75-130">Megosztás szerepkörben</span><span class="sxs-lookup"><span data-stu-id="3cf75-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf75-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cf75-131">-Confirm</span></span>
<span data-ttu-id="3cf75-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3cf75-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf75-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf75-133">-WhatIf</span></span>
<span data-ttu-id="3cf75-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3cf75-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cf75-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3cf75-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf75-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf75-136">CommonParameters</span></span>
<span data-ttu-id="3cf75-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf75-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf75-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cf75-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf75-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cf75-139">INPUTS</span></span>

### <span data-ttu-id="3cf75-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3cf75-140">System.String</span></span>

### <span data-ttu-id="3cf75-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3cf75-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="3cf75-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3cf75-142">OUTPUTS</span></span>

### <span data-ttu-id="3cf75-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3cf75-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="3cf75-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3cf75-144">NOTES</span></span>

## <span data-ttu-id="3cf75-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3cf75-145">RELATED LINKS</span></span>
