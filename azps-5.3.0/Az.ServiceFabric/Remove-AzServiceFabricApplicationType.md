---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479540"
---
# <span data-ttu-id="ea5c5-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ea5c5-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="ea5c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea5c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5c5-103">Távolítsa el a Service fabric egy alkalmazástípust a fürtből.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="ea5c5-104">Ezzel eltávolítja az erőforrás összes típusverzióját.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="ea5c5-105">Csak az ARM támogatott.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="ea5c5-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ea5c5-106">SYNTAX</span></span>

### <span data-ttu-id="ea5c5-107">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea5c5-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea5c5-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea5c5-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea5c5-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea5c5-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea5c5-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ea5c5-110">DESCRIPTION</span></span>
<span data-ttu-id="ea5c5-111">Ez a parancsmag eltávolítja a fürtön futó alkalmazástípust, és eltávolítja az erőforrás összes típusverzióját, de a parancs futtatása előtt az alatta található összes alkalmazást el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="ea5c5-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ea5c5-112">EXAMPLES</span></span>

### <span data-ttu-id="ea5c5-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="ea5c5-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="ea5c5-114">Ez a példa eltávolítja a "testAppType" alkalmazástípust és az alatta elérhető összes verziót.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="ea5c5-115">Ha vannak ezzel a típussal létrehozott alkalmazások, a parancs kivételt tesz ki.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="ea5c5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea5c5-116">PARAMETERS</span></span>

### <span data-ttu-id="ea5c5-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ea5c5-117">-ClusterName</span></span>
<span data-ttu-id="ea5c5-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ea5c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5c5-119">-DefaultProfile</span></span>
<span data-ttu-id="ea5c5-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea5c5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ea5c5-121">-Force</span></span>
<span data-ttu-id="ea5c5-122">Eltávolítás kérdés nélkül.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="ea5c5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea5c5-123">-InputObject</span></span>
<span data-ttu-id="ea5c5-124">Az alkalmazástípus-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ea5c5-125">-Name</span></span>
<span data-ttu-id="ea5c5-126">Adja meg az alkalmazástípus nevét.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea5c5-127">-PassThru</span></span>
<span data-ttu-id="ea5c5-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ea5c5-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ea5c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="ea5c5-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ea5c5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea5c5-131">-ResourceId</span></span>
<span data-ttu-id="ea5c5-132">Arm ResourceId of the application type.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="ea5c5-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea5c5-133">-Confirm</span></span>
<span data-ttu-id="ea5c5-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5c5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5c5-135">-WhatIf</span></span>
<span data-ttu-id="ea5c5-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea5c5-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5c5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5c5-138">CommonParameters</span></span>
<span data-ttu-id="ea5c5-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5c5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5c5-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea5c5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5c5-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea5c5-141">INPUTS</span></span>

### <span data-ttu-id="ea5c5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ea5c5-142">System.String</span></span>

### <span data-ttu-id="ea5c5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="ea5c5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="ea5c5-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea5c5-144">OUTPUTS</span></span>

### <span data-ttu-id="ea5c5-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ea5c5-145">System.Boolean</span></span>

## <span data-ttu-id="ea5c5-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ea5c5-146">NOTES</span></span>

## <span data-ttu-id="ea5c5-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea5c5-147">RELATED LINKS</span></span>
