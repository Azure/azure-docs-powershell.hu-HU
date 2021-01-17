---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348606"
---
# <span data-ttu-id="c2fc3-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c2fc3-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="c2fc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fc3-103">Távolítsa el a service fabric an application type version from the cluster.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="c2fc3-104">Csak az ARM telepített alkalmazástípus-verziók támogatottak.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="c2fc3-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2fc3-105">SYNTAX</span></span>

### <span data-ttu-id="c2fc3-106">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2fc3-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fc3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2fc3-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fc3-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2fc3-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2fc3-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2fc3-109">DESCRIPTION</span></span>
<span data-ttu-id="c2fc3-110">Ez a parancsmag eltávolítja a Service fabric egy alkalmazástípusú verziót a fürtből.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="c2fc3-111">A parancs futtatása előtt az erőforrás összes alkalmazását el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="c2fc3-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2fc3-112">EXAMPLES</span></span>

### <span data-ttu-id="c2fc3-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2fc3-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="c2fc3-114">Ez a példa eltávolítja a "v1" verziót a "testAppType" típus alatt.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="c2fc3-115">Ebben az erőforrásban a parancs kivételt tesz ki.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="c2fc3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2fc3-116">PARAMETERS</span></span>

### <span data-ttu-id="c2fc3-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c2fc3-117">-ClusterName</span></span>
<span data-ttu-id="c2fc3-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c2fc3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fc3-119">-DefaultProfile</span></span>
<span data-ttu-id="c2fc3-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fc3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c2fc3-121">-Force</span></span>
<span data-ttu-id="c2fc3-122">Eltávolítás kérdés nélkül.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="c2fc3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2fc3-123">-InputObject</span></span>
<span data-ttu-id="c2fc3-124">Az alkalmazástípus verzióerőforrása.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-124">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c2fc3-125">-Name</span></span>
<span data-ttu-id="c2fc3-126">Adja meg az alkalmazástípus nevét.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2fc3-127">-PassThru</span></span>
<span data-ttu-id="c2fc3-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c2fc3-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2fc3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2fc3-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2fc3-130">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c2fc3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2fc3-131">-ResourceId</span></span>
<span data-ttu-id="c2fc3-132">Arm ResourceId of the application type version.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="c2fc3-133">-Version</span><span class="sxs-lookup"><span data-stu-id="c2fc3-133">-Version</span></span>
<span data-ttu-id="c2fc3-134">Adja meg az alkalmazás típusát.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-134">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2fc3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2fc3-135">-Confirm</span></span>
<span data-ttu-id="c2fc3-136">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2fc3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2fc3-137">-WhatIf</span></span>
<span data-ttu-id="c2fc3-138">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2fc3-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2fc3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fc3-140">CommonParameters</span></span>
<span data-ttu-id="c2fc3-141">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fc3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fc3-142">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2fc3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fc3-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fc3-143">INPUTS</span></span>

### <span data-ttu-id="c2fc3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c2fc3-144">System.String</span></span>

### <span data-ttu-id="c2fc3-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c2fc3-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="c2fc3-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2fc3-146">OUTPUTS</span></span>

### <span data-ttu-id="c2fc3-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c2fc3-147">System.Boolean</span></span>

## <span data-ttu-id="c2fc3-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2fc3-148">NOTES</span></span>

## <span data-ttu-id="c2fc3-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2fc3-149">RELATED LINKS</span></span>
