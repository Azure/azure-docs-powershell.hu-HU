---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: ea86fb4a110d355a848b9fe58969d30ccb96e2da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300149"
---
# <span data-ttu-id="ebd1f-101">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ebd1f-101">Get-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="ebd1f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ebd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd1f-103">A szolgáltatás típusa: az alkalmazás típusa – verzió részletei.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-103">Get Service Fabric application type version details.</span></span>

## <span data-ttu-id="ebd1f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ebd1f-104">SYNTAX</span></span>

### <span data-ttu-id="ebd1f-105">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebd1f-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebd1f-106">ByVersion</span><span class="sxs-lookup"><span data-stu-id="ebd1f-106">ByVersion</span></span>
```
Get-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebd1f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebd1f-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebd1f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ebd1f-108">DESCRIPTION</span></span>
<span data-ttu-id="ebd1f-109">Ezzel a parancsmaggal lekérheti az alkalmazás típusának részleteit a megadott erőforráscsoport és fürtben.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-109">Use this cmdlet to get the application type version details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="ebd1f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ebd1f-110">EXAMPLES</span></span>

### <span data-ttu-id="ebd1f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ebd1f-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appTypeName = "v1"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version
```

<span data-ttu-id="ebd1f-112">Ebben a példában a "testAppType", "v1"-es verzióval rendelkező alkalmazást kapja, ha nem találja azt az erőforrást, amely kivételt fog kidobni.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-112">This example gets the application type "testAppType" with version "v1", if it doesn't find the resource it will throw an exception.</span></span>

### <span data-ttu-id="ebd1f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ebd1f-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Get-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName
```

<span data-ttu-id="ebd1f-114">Ez a példa bemutatja a megadott szektorcsoportban definiált alkalmazás-típusok listáját, és írja be a következőt:</span><span class="sxs-lookup"><span data-stu-id="ebd1f-114">This example gets a list of the application type versions defined under the specified cluster and type.</span></span>

## <span data-ttu-id="ebd1f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ebd1f-115">PARAMETERS</span></span>

### <span data-ttu-id="ebd1f-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="ebd1f-116">-ClusterName</span></span>
<span data-ttu-id="ebd1f-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ebd1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd1f-118">-DefaultProfile</span></span>
<span data-ttu-id="ebd1f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebd1f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ebd1f-120">-Name</span></span>
<span data-ttu-id="ebd1f-121">Adja meg az alkalmazás típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-121">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="ebd1f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebd1f-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebd1f-123">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ebd1f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebd1f-124">-ResourceId</span></span>
<span data-ttu-id="ebd1f-125">Az alkalmazás típusa ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebd1f-125">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="ebd1f-126">-Verzió</span><span class="sxs-lookup"><span data-stu-id="ebd1f-126">-Version</span></span>
<span data-ttu-id="ebd1f-127">Adja meg az alkalmazás típusának verziószámát.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-127">Specify the version of the application type.</span></span>

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

### <span data-ttu-id="ebd1f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd1f-128">CommonParameters</span></span>
<span data-ttu-id="ebd1f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ebd1f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd1f-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ebd1f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd1f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebd1f-131">INPUTS</span></span>

### <span data-ttu-id="ebd1f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ebd1f-132">System.String</span></span>

## <span data-ttu-id="ebd1f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebd1f-133">OUTPUTS</span></span>

### <span data-ttu-id="ebd1f-134">Microsoft. Azure. Command. ServiceFabric. models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ebd1f-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="ebd1f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ebd1f-135">NOTES</span></span>

## <span data-ttu-id="ebd1f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebd1f-136">RELATED LINKS</span></span>
