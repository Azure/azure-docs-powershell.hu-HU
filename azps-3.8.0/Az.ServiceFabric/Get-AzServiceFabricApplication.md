---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: e78580f98ae0569a2104a4d39123070e7383fa6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014291"
---
# <span data-ttu-id="1974b-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1974b-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="1974b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1974b-102">SYNOPSIS</span></span>
<span data-ttu-id="1974b-103">A Service Fabric alkalmazás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="1974b-103">Get Service Fabric application details.</span></span>

## <span data-ttu-id="1974b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1974b-104">SYNTAX</span></span>

### <span data-ttu-id="1974b-105">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1974b-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1974b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1974b-106">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1974b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1974b-107">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1974b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1974b-108">DESCRIPTION</span></span>
<span data-ttu-id="1974b-109">Ez a parancsmag az alkalmazás adatait a megadott erőforráscsoport és fürtben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1974b-109">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="1974b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1974b-110">EXAMPLES</span></span>

### <span data-ttu-id="1974b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1974b-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="1974b-112">Ebben a példában a "testApp" alkalmazáshoz az alkalmazás-erőforrás adatait kapja.</span><span class="sxs-lookup"><span data-stu-id="1974b-112">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="1974b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1974b-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="1974b-114">Ebben a példában a "testCluster" szektorcsoport alatti alkalmazások listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="1974b-114">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="1974b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1974b-115">PARAMETERS</span></span>

### <span data-ttu-id="1974b-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1974b-116">-ClusterName</span></span>
<span data-ttu-id="1974b-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="1974b-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1974b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1974b-118">-DefaultProfile</span></span>
<span data-ttu-id="1974b-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1974b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1974b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1974b-120">-Name</span></span>
<span data-ttu-id="1974b-121">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="1974b-121">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1974b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1974b-122">-ResourceGroupName</span></span>
<span data-ttu-id="1974b-123">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="1974b-123">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1974b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1974b-124">-ResourceId</span></span>
<span data-ttu-id="1974b-125">A kar ResourceId az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="1974b-125">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="1974b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1974b-126">CommonParameters</span></span>
<span data-ttu-id="1974b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1974b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1974b-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1974b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1974b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1974b-129">INPUTS</span></span>

### <span data-ttu-id="1974b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1974b-130">System.String</span></span>

## <span data-ttu-id="1974b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1974b-131">OUTPUTS</span></span>

### <span data-ttu-id="1974b-132">Microsoft. Azure. Command. ServiceFabric. models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="1974b-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1974b-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1974b-133">NOTES</span></span>

## <span data-ttu-id="1974b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1974b-134">RELATED LINKS</span></span>
