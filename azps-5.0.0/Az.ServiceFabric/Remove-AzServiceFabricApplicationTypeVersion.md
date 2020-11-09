---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 498dec77dfc2f4ede8ae81aa70b10acfe2ad2954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300914"
---
# <span data-ttu-id="45c09-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="45c09-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="45c09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45c09-102">SYNOPSIS</span></span>
<span data-ttu-id="45c09-103">A szolgáltatás eltávolítása: az alkalmazás típusának verziója a fürtből</span><span class="sxs-lookup"><span data-stu-id="45c09-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="45c09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45c09-104">SYNTAX</span></span>

### <span data-ttu-id="45c09-105">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="45c09-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c09-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="45c09-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c09-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="45c09-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c09-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="45c09-108">DESCRIPTION</span></span>
<span data-ttu-id="45c09-109">Ez a parancsmag eltávolítja a szolgáltatást a fürtben egy alkalmazás típusú verzióból.</span><span class="sxs-lookup"><span data-stu-id="45c09-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="45c09-110">A parancs futtatása előtt az erőforrás minden alkalmazását el kell távolítani.</span><span class="sxs-lookup"><span data-stu-id="45c09-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="45c09-111">Példák</span><span class="sxs-lookup"><span data-stu-id="45c09-111">EXAMPLES</span></span>

### <span data-ttu-id="45c09-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="45c09-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="45c09-113">Ebben a példában a "v1"-es verzió törlődik a "testAppType" típus alatt.</span><span class="sxs-lookup"><span data-stu-id="45c09-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="45c09-114">Az adott erőforrásban vannak alkalmazások, a parancs kivételt fog kidobni.</span><span class="sxs-lookup"><span data-stu-id="45c09-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="45c09-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45c09-115">PARAMETERS</span></span>

### <span data-ttu-id="45c09-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="45c09-116">-ClusterName</span></span>
<span data-ttu-id="45c09-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="45c09-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="45c09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c09-118">-DefaultProfile</span></span>
<span data-ttu-id="45c09-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="45c09-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c09-120">-Force</span><span class="sxs-lookup"><span data-stu-id="45c09-120">-Force</span></span>
<span data-ttu-id="45c09-121">Eltávolítás kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="45c09-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="45c09-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45c09-122">-InputObject</span></span>
<span data-ttu-id="45c09-123">Az alkalmazás típusa – verzió-erőforrás.</span><span class="sxs-lookup"><span data-stu-id="45c09-123">The application type version resource.</span></span>

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

### <span data-ttu-id="45c09-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45c09-124">-Name</span></span>
<span data-ttu-id="45c09-125">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="45c09-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="45c09-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45c09-126">-PassThru</span></span>
<span data-ttu-id="45c09-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="45c09-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="45c09-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c09-128">-ResourceGroupName</span></span>
<span data-ttu-id="45c09-129">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="45c09-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="45c09-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45c09-130">-ResourceId</span></span>
<span data-ttu-id="45c09-131">Az alkalmazás típusa ResourceId</span><span class="sxs-lookup"><span data-stu-id="45c09-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="45c09-132">-Verzió</span><span class="sxs-lookup"><span data-stu-id="45c09-132">-Version</span></span>
<span data-ttu-id="45c09-133">Adja meg az alkalmazás típusának verziószámát.</span><span class="sxs-lookup"><span data-stu-id="45c09-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="45c09-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45c09-134">-Confirm</span></span>
<span data-ttu-id="45c09-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45c09-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c09-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c09-136">-WhatIf</span></span>
<span data-ttu-id="45c09-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45c09-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c09-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45c09-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c09-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c09-139">CommonParameters</span></span>
<span data-ttu-id="45c09-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45c09-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c09-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="45c09-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c09-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45c09-142">INPUTS</span></span>

### <span data-ttu-id="45c09-143">System. String</span><span class="sxs-lookup"><span data-stu-id="45c09-143">System.String</span></span>

### <span data-ttu-id="45c09-144">Microsoft. Azure. Command. ServiceFabric. models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="45c09-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="45c09-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45c09-145">OUTPUTS</span></span>

### <span data-ttu-id="45c09-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45c09-146">System.Boolean</span></span>

## <span data-ttu-id="45c09-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45c09-147">NOTES</span></span>

## <span data-ttu-id="45c09-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45c09-148">RELATED LINKS</span></span>
