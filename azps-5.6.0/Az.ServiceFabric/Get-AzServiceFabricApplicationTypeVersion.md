---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 9c9f1b3c88e49eca3be8a923324d195d3a773c1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929770"
---
# <span data-ttu-id="11c43-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11c43-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="11c43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11c43-102">SYNOPSIS</span></span>
<span data-ttu-id="11c43-103">A Service Fabric alkalmazás verziószámának részletei.</span><span class="sxs-lookup"><span data-stu-id="11c43-103">Get Service Fabric application type version details.</span></span> <span data-ttu-id="11c43-104">Csak az ARM telepített alkalmazástípus-verziók támogatottak.</span><span class="sxs-lookup"><span data-stu-id="11c43-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="11c43-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="11c43-105">SYNTAX</span></span>

### <span data-ttu-id="11c43-106">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11c43-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11c43-107">ByVersion</span><span class="sxs-lookup"><span data-stu-id="11c43-107">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11c43-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="11c43-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11c43-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="11c43-109">DESCRIPTION</span></span>
<span data-ttu-id="11c43-110">Ezzel a parancsmagtal lekérte az alkalmazástípus verziószámát a megadott erőforráscsoportban és -fürtben.</span><span class="sxs-lookup"><span data-stu-id="11c43-110">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="11c43-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="11c43-111">EXAMPLES</span></span>

### <span data-ttu-id="11c43-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="11c43-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="11c43-113">Ebben a példában a "testAppType" és a "v1" verziójú alkalmazástípust kapja meg, ha nem találja azt az erőforrást, amely kivételt fog tenni.</span><span class="sxs-lookup"><span data-stu-id="11c43-113">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="11c43-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="11c43-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="11c43-115">Ebben a példában a megadott fürt és típus alatt definiált alkalmazástípus-verziók listája szerepel.</span><span class="sxs-lookup"><span data-stu-id="11c43-115">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="11c43-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11c43-116">PARAMETERS</span></span>

### <span data-ttu-id="11c43-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11c43-117">-ClusterName</span></span>
<span data-ttu-id="11c43-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="11c43-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c43-119">-DefaultProfile</span></span>
<span data-ttu-id="11c43-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11c43-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c43-121">-Name</span><span class="sxs-lookup"><span data-stu-id="11c43-121">-Name</span></span>
<span data-ttu-id="11c43-122">Adja meg az alkalmazástípus nevét.</span><span class="sxs-lookup"><span data-stu-id="11c43-122">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c43-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c43-123">-ResourceGroupName</span></span>
<span data-ttu-id="11c43-124">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="11c43-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c43-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11c43-125">-ResourceId</span></span>
<span data-ttu-id="11c43-126">Arm ResourceId of the application type version.</span><span class="sxs-lookup"><span data-stu-id="11c43-126">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="11c43-127">-Version</span><span class="sxs-lookup"><span data-stu-id="11c43-127">-Version</span></span>
<span data-ttu-id="11c43-128">Adja meg az alkalmazástípus verzióját.</span><span class="sxs-lookup"><span data-stu-id="11c43-128">Specify the version of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVersion
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c43-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c43-129">CommonParameters</span></span>
<span data-ttu-id="11c43-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c43-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c43-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11c43-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c43-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11c43-132">INPUTS</span></span>

### <span data-ttu-id="11c43-133">System.String</span><span class="sxs-lookup"><span data-stu-id="11c43-133">System.String</span></span>

## <span data-ttu-id="11c43-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11c43-134">OUTPUTS</span></span>

### <span data-ttu-id="11c43-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="11c43-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="11c43-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="11c43-136">NOTES</span></span>

## <span data-ttu-id="11c43-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11c43-137">RELATED LINKS</span></span>
