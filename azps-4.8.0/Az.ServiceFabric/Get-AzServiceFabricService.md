---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 1dfd9e0aa2bc6b7c5d52ccfed756f2a96a3f307c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183314"
---
# <span data-ttu-id="1d5fa-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="1d5fa-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="1d5fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1d5fa-103">A szolgáltatás szerkezete szolgáltatás adatai a megadott alkalmazásban és fürtben.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-103">Get Service Fabric service details under the specified application and cluster.</span></span>

## <span data-ttu-id="1d5fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d5fa-104">SYNTAX</span></span>

### <span data-ttu-id="1d5fa-105">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d5fa-105">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d5fa-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1d5fa-106">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d5fa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d5fa-107">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d5fa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d5fa-108">DESCRIPTION</span></span>
<span data-ttu-id="1d5fa-109">Ez a parancsmag a megadott alkalmazásban és fürtben a szolgáltatás adatait fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-109">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="1d5fa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1d5fa-110">EXAMPLES</span></span>

### <span data-ttu-id="1d5fa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1d5fa-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="1d5fa-112">Ez a példa beilleszti a szolgáltatás erőforrásának adatait a "testApp ~ testService" szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-112">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="1d5fa-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="1d5fa-113">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="1d5fa-114">Ebben a példában a szolgáltatások listája szerepel a "testApp" alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-114">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="1d5fa-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d5fa-115">PARAMETERS</span></span>

### <span data-ttu-id="1d5fa-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="1d5fa-116">-ApplicationName</span></span>
<span data-ttu-id="1d5fa-117">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-117">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndCluster, ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d5fa-118">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="1d5fa-118">-ClusterName</span></span>
<span data-ttu-id="1d5fa-119">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1d5fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d5fa-120">-DefaultProfile</span></span>
<span data-ttu-id="1d5fa-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d5fa-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d5fa-122">-Name</span></span>
<span data-ttu-id="1d5fa-123">Adja meg a szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-123">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d5fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d5fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="1d5fa-125">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-125">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1d5fa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d5fa-126">-ResourceId</span></span>
<span data-ttu-id="1d5fa-127">A szolgáltatás ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-127">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="1d5fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d5fa-128">CommonParameters</span></span>
<span data-ttu-id="1d5fa-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d5fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d5fa-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1d5fa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d5fa-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d5fa-131">INPUTS</span></span>

### <span data-ttu-id="1d5fa-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1d5fa-132">System.String</span></span>

## <span data-ttu-id="1d5fa-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d5fa-133">OUTPUTS</span></span>

### <span data-ttu-id="1d5fa-134">Microsoft. Azure. Command. ServiceFabric. models. PSService</span><span class="sxs-lookup"><span data-stu-id="1d5fa-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="1d5fa-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d5fa-135">NOTES</span></span>

## <span data-ttu-id="1d5fa-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d5fa-136">RELATED LINKS</span></span>
