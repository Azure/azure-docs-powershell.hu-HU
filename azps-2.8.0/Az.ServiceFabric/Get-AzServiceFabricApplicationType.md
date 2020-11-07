---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: 78cec82383c257e325c35d0987de73f37aff253d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838010"
---
# <span data-ttu-id="b71b3-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="b71b3-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="b71b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b71b3-102">SYNOPSIS</span></span>
<span data-ttu-id="b71b3-103">A szolgáltatás anyagának beszerzése alkalmazás típusa – részletek</span><span class="sxs-lookup"><span data-stu-id="b71b3-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="b71b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b71b3-104">SYNTAX</span></span>

### <span data-ttu-id="b71b3-105">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b71b3-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b71b3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b71b3-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b71b3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b71b3-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b71b3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b71b3-108">DESCRIPTION</span></span>
<span data-ttu-id="b71b3-109">Ezzel a parancsmaggal beolvashatja az alkalmazás típusának adatait a megadott erőforráscsoport és fürt számára.</span><span class="sxs-lookup"><span data-stu-id="b71b3-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="b71b3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b71b3-110">EXAMPLES</span></span>

### <span data-ttu-id="b71b3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b71b3-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="b71b3-112">Ez a példa az alkalmazás típusának adatait a megadott paraméterekkel kapja meg, ha nem találja az erőforrást, akkor kivételt fog kidobni.</span><span class="sxs-lookup"><span data-stu-id="b71b3-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="b71b3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="b71b3-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="b71b3-114">Ebben a példában a megadott fürtben megadott alkalmazások típusait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b71b3-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="b71b3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b71b3-115">PARAMETERS</span></span>

### <span data-ttu-id="b71b3-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b71b3-116">-ClusterName</span></span>
<span data-ttu-id="b71b3-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="b71b3-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b71b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71b3-118">-DefaultProfile</span></span>
<span data-ttu-id="b71b3-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b71b3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b71b3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b71b3-120">-Name</span></span>
<span data-ttu-id="b71b3-121">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="b71b3-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="b71b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="b71b3-123">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="b71b3-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b71b3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b71b3-124">-ResourceId</span></span>
<span data-ttu-id="b71b3-125">A kar ResourceId az alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="b71b3-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="b71b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71b3-126">CommonParameters</span></span>
<span data-ttu-id="b71b3-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b71b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71b3-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b71b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71b3-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b71b3-129">INPUTS</span></span>

### <span data-ttu-id="b71b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b71b3-130">System.String</span></span>

## <span data-ttu-id="b71b3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b71b3-131">OUTPUTS</span></span>

### <span data-ttu-id="b71b3-132">Microsoft. Azure. Command. ServiceFabric. models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="b71b3-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="b71b3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b71b3-133">NOTES</span></span>

## <span data-ttu-id="b71b3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b71b3-134">RELATED LINKS</span></span>
