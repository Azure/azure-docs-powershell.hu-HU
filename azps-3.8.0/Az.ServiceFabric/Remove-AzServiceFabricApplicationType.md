---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: bba2ab235532f83b3955ff9a12016438e0e1960e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011684"
---
# <span data-ttu-id="e3da8-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e3da8-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="e3da8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3da8-102">SYNOPSIS</span></span>
<span data-ttu-id="e3da8-103">A szolgáltatás eltávolítása: az alkalmazás típusa a fürtben.</span><span class="sxs-lookup"><span data-stu-id="e3da8-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="e3da8-104">Ezzel a beállítással a program eltávolítja az összes típusú verziót az erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="e3da8-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="e3da8-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3da8-105">SYNTAX</span></span>

### <span data-ttu-id="e3da8-106">ByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3da8-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3da8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3da8-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3da8-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e3da8-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3da8-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3da8-109">DESCRIPTION</span></span>
<span data-ttu-id="e3da8-110">Ez a parancsmag eltávolítja a fürtöt, és eltávolítja az összes típusú verziót az ebben az erőforrásban, de az alatta lévő összes alkalmazást el kell távolítani a parancs futtatása előtt.</span><span class="sxs-lookup"><span data-stu-id="e3da8-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="e3da8-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e3da8-111">EXAMPLES</span></span>

### <span data-ttu-id="e3da8-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3da8-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="e3da8-113">Ebben a példában a "testAppType" és a benne lévő összes verzió törlődik.</span><span class="sxs-lookup"><span data-stu-id="e3da8-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="e3da8-114">Ha az ilyen típusú alkalmazások mindegyike létezik, a parancs kivételt fog kidobni.</span><span class="sxs-lookup"><span data-stu-id="e3da8-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="e3da8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3da8-115">PARAMETERS</span></span>

### <span data-ttu-id="e3da8-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e3da8-116">-ClusterName</span></span>
<span data-ttu-id="e3da8-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="e3da8-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e3da8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3da8-118">-DefaultProfile</span></span>
<span data-ttu-id="e3da8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3da8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3da8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e3da8-120">-Force</span></span>
<span data-ttu-id="e3da8-121">Eltávolítás kérés nélkül.</span><span class="sxs-lookup"><span data-stu-id="e3da8-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="e3da8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3da8-122">-InputObject</span></span>
<span data-ttu-id="e3da8-123">Az alkalmazás típusa erőforrás.</span><span class="sxs-lookup"><span data-stu-id="e3da8-123">The application type resource.</span></span>

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

### <span data-ttu-id="e3da8-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3da8-124">-Name</span></span>
<span data-ttu-id="e3da8-125">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="e3da8-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="e3da8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3da8-126">-PassThru</span></span>
<span data-ttu-id="e3da8-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e3da8-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e3da8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3da8-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3da8-129">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="e3da8-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e3da8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3da8-130">-ResourceId</span></span>
<span data-ttu-id="e3da8-131">A kar ResourceId az alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="e3da8-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="e3da8-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3da8-132">-Confirm</span></span>
<span data-ttu-id="e3da8-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3da8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3da8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3da8-134">-WhatIf</span></span>
<span data-ttu-id="e3da8-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3da8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3da8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3da8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3da8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3da8-137">CommonParameters</span></span>
<span data-ttu-id="e3da8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3da8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3da8-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3da8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3da8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3da8-140">INPUTS</span></span>

### <span data-ttu-id="e3da8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e3da8-141">System.String</span></span>

### <span data-ttu-id="e3da8-142">Microsoft. Azure. Command. ServiceFabric. models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="e3da8-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="e3da8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3da8-143">OUTPUTS</span></span>

### <span data-ttu-id="e3da8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3da8-144">System.Boolean</span></span>

## <span data-ttu-id="e3da8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3da8-145">NOTES</span></span>

## <span data-ttu-id="e3da8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3da8-146">RELATED LINKS</span></span>
