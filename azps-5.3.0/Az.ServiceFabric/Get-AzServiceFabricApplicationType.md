---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 73e89bcb6ffb6f8c09a0ec53f203b6ed251fd3e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479573"
---
# <span data-ttu-id="9b67d-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="9b67d-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="9b67d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b67d-102">SYNOPSIS</span></span>
<span data-ttu-id="9b67d-103">A Service Fabric alkalmazás típusának részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="9b67d-103">Get Service Fabric application type details.</span></span> <span data-ttu-id="9b67d-104">Csak az ARM támogatott.</span><span class="sxs-lookup"><span data-stu-id="9b67d-104">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="9b67d-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b67d-105">SYNTAX</span></span>

### <span data-ttu-id="9b67d-106">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b67d-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b67d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="9b67d-107">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b67d-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b67d-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b67d-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b67d-109">DESCRIPTION</span></span>
<span data-ttu-id="9b67d-110">Ezzel a parancsmagtal lekérte az alkalmazástípus részleteit a megadott erőforráscsoportban és -fürtben.</span><span class="sxs-lookup"><span data-stu-id="9b67d-110">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="9b67d-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b67d-111">EXAMPLES</span></span>

### <span data-ttu-id="9b67d-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9b67d-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="9b67d-113">Ebben a példában az alkalmazástípus részleteit adhatja meg a megadott paraméterekkel, ha nem találja azt az erőforrást, amely kivételt tesz ki.</span><span class="sxs-lookup"><span data-stu-id="9b67d-113">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="9b67d-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9b67d-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="9b67d-115">Ebben a példában megjelenik a megadott fürt alatt definiált alkalmazástípusok listája.</span><span class="sxs-lookup"><span data-stu-id="9b67d-115">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="9b67d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b67d-116">PARAMETERS</span></span>

### <span data-ttu-id="9b67d-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9b67d-117">-ClusterName</span></span>
<span data-ttu-id="9b67d-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="9b67d-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9b67d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b67d-119">-DefaultProfile</span></span>
<span data-ttu-id="9b67d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b67d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b67d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9b67d-121">-Name</span></span>
<span data-ttu-id="9b67d-122">Az alkalmazástípus nevének megadása</span><span class="sxs-lookup"><span data-stu-id="9b67d-122">Specify the name of the application type</span></span>

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

### <span data-ttu-id="9b67d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b67d-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b67d-124">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="9b67d-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9b67d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b67d-125">-ResourceId</span></span>
<span data-ttu-id="9b67d-126">Arm ResourceId of the application type.</span><span class="sxs-lookup"><span data-stu-id="9b67d-126">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="9b67d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b67d-127">CommonParameters</span></span>
<span data-ttu-id="9b67d-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b67d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b67d-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b67d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b67d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b67d-130">INPUTS</span></span>

### <span data-ttu-id="9b67d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9b67d-131">System.String</span></span>

## <span data-ttu-id="9b67d-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b67d-132">OUTPUTS</span></span>

### <span data-ttu-id="9b67d-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="9b67d-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="9b67d-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b67d-134">NOTES</span></span>

## <span data-ttu-id="9b67d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b67d-135">RELATED LINKS</span></span>
