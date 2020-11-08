---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationType.md
ms.openlocfilehash: dcbb85e9c7b8f1a98acec094043ec03b562e33d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014294"
---
# <span data-ttu-id="979fb-101">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="979fb-101">Get-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="979fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="979fb-102">SYNOPSIS</span></span>
<span data-ttu-id="979fb-103">A szolgáltatás anyagának beszerzése alkalmazás típusa – részletek</span><span class="sxs-lookup"><span data-stu-id="979fb-103">Get Service Fabric application type details.</span></span>

## <span data-ttu-id="979fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="979fb-104">SYNTAX</span></span>

### <span data-ttu-id="979fb-105">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="979fb-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="979fb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="979fb-106">ByName</span></span>
```
Get-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="979fb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="979fb-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationType -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="979fb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="979fb-108">DESCRIPTION</span></span>
<span data-ttu-id="979fb-109">Ezzel a parancsmaggal beolvashatja az alkalmazás típusának adatait a megadott erőforráscsoport és fürt számára.</span><span class="sxs-lookup"><span data-stu-id="979fb-109">Use this cmdlet to get the application type details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="979fb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="979fb-110">EXAMPLES</span></span>

### <span data-ttu-id="979fb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="979fb-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="979fb-112">Ez a példa az alkalmazás típusának adatait a megadott paraméterekkel kapja meg, ha nem találja az erőforrást, akkor kivételt fog kidobni.</span><span class="sxs-lookup"><span data-stu-id="979fb-112">This example will get the application type details with the parameters specified, if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="979fb-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="979fb-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="979fb-114">Ebben a példában a megadott fürtben megadott alkalmazások típusait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="979fb-114">This example will get a list of the application types defined under the specified cluster.</span></span>

## <span data-ttu-id="979fb-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="979fb-115">PARAMETERS</span></span>

### <span data-ttu-id="979fb-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="979fb-116">-ClusterName</span></span>
<span data-ttu-id="979fb-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="979fb-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="979fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="979fb-118">-DefaultProfile</span></span>
<span data-ttu-id="979fb-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="979fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="979fb-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="979fb-120">-Name</span></span>
<span data-ttu-id="979fb-121">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="979fb-121">Specify the name of the application type</span></span>

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

### <span data-ttu-id="979fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="979fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="979fb-123">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="979fb-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="979fb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="979fb-124">-ResourceId</span></span>
<span data-ttu-id="979fb-125">A kar ResourceId az alkalmazás típusa.</span><span class="sxs-lookup"><span data-stu-id="979fb-125">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="979fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="979fb-126">CommonParameters</span></span>
<span data-ttu-id="979fb-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="979fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="979fb-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="979fb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="979fb-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="979fb-129">INPUTS</span></span>

### <span data-ttu-id="979fb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="979fb-130">System.String</span></span>

## <span data-ttu-id="979fb-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="979fb-131">OUTPUTS</span></span>

### <span data-ttu-id="979fb-132">Microsoft. Azure. Command. ServiceFabric. models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="979fb-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="979fb-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="979fb-133">NOTES</span></span>

## <span data-ttu-id="979fb-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="979fb-134">RELATED LINKS</span></span>
