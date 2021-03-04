---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 0082f5625351b8bb8e832ad60eb76837f09ccd47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929777"
---
# <span data-ttu-id="33c2e-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="33c2e-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="33c2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="33c2e-103">A Service Fabric alkalmazás típusának részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="33c2e-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="33c2e-104">Csak az ARM támogatott.</span><span class="sxs-lookup"><span data-stu-id="33c2e-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="33c2e-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="33c2e-105">SYNTAX</span></span>

### <span data-ttu-id="33c2e-106">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="33c2e-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c2e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="33c2e-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c2e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33c2e-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33c2e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="33c2e-109">DESCRIPTION</span></span>
<span data-ttu-id="33c2e-110">Ezzel a parancsmagtal lekérte az alkalmazástípus részleteit a megadott erőforráscsoportban és -fürtben.</span><span class="sxs-lookup"><span data-stu-id="33c2e-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="33c2e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="33c2e-111">EXAMPLES</span></span>

### <span data-ttu-id="33c2e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="33c2e-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="33c2e-113">Ebben a példában az alkalmazástípus részleteit adhatja meg a megadott paraméterekkel, ha nem találja azt az erőforrást, amely kivételt ad.</span><span class="sxs-lookup"><span data-stu-id="33c2e-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="33c2e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="33c2e-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="33c2e-115">Ebben a példában megjelenik a megadott fürt alatt definiált alkalmazástípusok listája.</span><span class="sxs-lookup"><span data-stu-id="33c2e-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="33c2e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33c2e-116">PARAMETERS</span></span>

### <span data-ttu-id="33c2e-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="33c2e-117">-ClusterName</span></span>
<span data-ttu-id="33c2e-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="33c2e-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c2e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c2e-119">-DefaultProfile</span></span>
<span data-ttu-id="33c2e-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="33c2e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c2e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="33c2e-121">-Name</span></span>
<span data-ttu-id="33c2e-122">Az alkalmazástípus nevének megadása</span><span class="sxs-lookup"><span data-stu-id="33c2e-122">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33c2e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c2e-123">-ResourceGroupName</span></span>
<span data-ttu-id="33c2e-124">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="33c2e-124">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c2e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33c2e-125">-ResourceId</span></span>
<span data-ttu-id="33c2e-126">Arm ResourceId of the application type.</span><span class="sxs-lookup"><span data-stu-id="33c2e-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="33c2e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c2e-127">CommonParameters</span></span>
<span data-ttu-id="33c2e-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c2e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c2e-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33c2e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c2e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="33c2e-130">INPUTS</span></span>

### <span data-ttu-id="33c2e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="33c2e-131">System.String</span></span>

## <span data-ttu-id="33c2e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="33c2e-132">OUTPUTS</span></span>

### <span data-ttu-id="33c2e-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="33c2e-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="33c2e-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="33c2e-134">NOTES</span></span>

## <span data-ttu-id="33c2e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="33c2e-135">RELATED LINKS</span></span>
