---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479544"
---
# <span data-ttu-id="e07c6-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="e07c6-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="e07c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e07c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e07c6-103">Alkalmazás eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="e07c6-103">Remove an application from the cluster.</span></span> <span data-ttu-id="e07c6-104">Ezzel eltávolítja az alkalmazás összes szolgáltatását.</span><span class="sxs-lookup"><span data-stu-id="e07c6-104">This will remove all the services under the application.</span></span> <span data-ttu-id="e07c6-105">Csak az ARM támogatott.</span><span class="sxs-lookup"><span data-stu-id="e07c6-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="e07c6-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e07c6-106">SYNTAX</span></span>

### <span data-ttu-id="e07c6-107">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e07c6-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07c6-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e07c6-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e07c6-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e07c6-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e07c6-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e07c6-110">DESCRIPTION</span></span>
<span data-ttu-id="e07c6-111">Ez a parancsmag eltávolítja a fürt egy alkalmazásűrlapját.</span><span class="sxs-lookup"><span data-stu-id="e07c6-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="e07c6-112">Ezzel eltávolítja az alkalmazáserőforrás összes szolgáltatását (ha van ilyen).</span><span class="sxs-lookup"><span data-stu-id="e07c6-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="e07c6-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e07c6-113">EXAMPLES</span></span>

### <span data-ttu-id="e07c6-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="e07c6-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="e07c6-115">Ez a példa eltávolítja a "testApp" alkalmazást a "testRG" erőforráscsoportból és a "testCluster" fürtből.</span><span class="sxs-lookup"><span data-stu-id="e07c6-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="e07c6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e07c6-116">PARAMETERS</span></span>

### <span data-ttu-id="e07c6-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e07c6-117">-ClusterName</span></span>
<span data-ttu-id="e07c6-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="e07c6-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07c6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e07c6-119">-DefaultProfile</span></span>
<span data-ttu-id="e07c6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e07c6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e07c6-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e07c6-121">-Force</span></span>
<span data-ttu-id="e07c6-122">Eltávolítás kérdés nélkül.</span><span class="sxs-lookup"><span data-stu-id="e07c6-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="e07c6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e07c6-123">-InputObject</span></span>
<span data-ttu-id="e07c6-124">Az alkalmazáserőforrás.</span><span class="sxs-lookup"><span data-stu-id="e07c6-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e07c6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e07c6-125">-Name</span></span>
<span data-ttu-id="e07c6-126">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="e07c6-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e07c6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e07c6-127">-PassThru</span></span>
<span data-ttu-id="e07c6-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e07c6-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e07c6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e07c6-129">-ResourceGroupName</span></span>
<span data-ttu-id="e07c6-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="e07c6-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07c6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e07c6-131">-ResourceId</span></span>
<span data-ttu-id="e07c6-132">Arm ResourceId of the application.</span><span class="sxs-lookup"><span data-stu-id="e07c6-132">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e07c6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e07c6-133">-Confirm</span></span>
<span data-ttu-id="e07c6-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e07c6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e07c6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e07c6-135">-WhatIf</span></span>
<span data-ttu-id="e07c6-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e07c6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e07c6-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e07c6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e07c6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e07c6-138">CommonParameters</span></span>
<span data-ttu-id="e07c6-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e07c6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e07c6-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e07c6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e07c6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e07c6-141">INPUTS</span></span>

### <span data-ttu-id="e07c6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e07c6-142">System.String</span></span>

### <span data-ttu-id="e07c6-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="e07c6-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="e07c6-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e07c6-144">OUTPUTS</span></span>

### <span data-ttu-id="e07c6-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e07c6-145">System.Boolean</span></span>

## <span data-ttu-id="e07c6-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e07c6-146">NOTES</span></span>

## <span data-ttu-id="e07c6-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e07c6-147">RELATED LINKS</span></span>
