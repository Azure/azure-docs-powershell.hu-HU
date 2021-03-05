---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: 51e2efb18a6c39e6d3206697d552f49f74648712
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015878"
---
# <span data-ttu-id="39d5e-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="39d5e-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="39d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="39d5e-103">A Service Fabric szolgáltatás részleteinek lekérte a megadott alkalmazás és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="39d5e-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="39d5e-104">Csak az ARM szolgáltatásokat támogatja.</span><span class="sxs-lookup"><span data-stu-id="39d5e-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="39d5e-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39d5e-105">SYNTAX</span></span>

### <span data-ttu-id="39d5e-106">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39d5e-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d5e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="39d5e-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d5e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39d5e-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39d5e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39d5e-109">DESCRIPTION</span></span>
<span data-ttu-id="39d5e-110">Ez a parancsmag a szolgáltatás részleteit a megadott alkalmazásból és fürtből fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="39d5e-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="39d5e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39d5e-111">EXAMPLES</span></span>

### <span data-ttu-id="39d5e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="39d5e-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="39d5e-113">Ez a példa a "testApp~testService" szolgáltatás szolgáltatáserőforrás-adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="39d5e-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="39d5e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="39d5e-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="39d5e-115">Ebben a példában a "testApp" alkalmazás alatt található szolgáltatások listája szerepel.</span><span class="sxs-lookup"><span data-stu-id="39d5e-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="39d5e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39d5e-116">PARAMETERS</span></span>

### <span data-ttu-id="39d5e-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="39d5e-117">-ApplicationName</span></span>
<span data-ttu-id="39d5e-118">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="39d5e-118">Specify the name of the application.</span></span>

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

### <span data-ttu-id="39d5e-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="39d5e-119">-ClusterName</span></span>
<span data-ttu-id="39d5e-120">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="39d5e-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="39d5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d5e-121">-DefaultProfile</span></span>
<span data-ttu-id="39d5e-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39d5e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d5e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="39d5e-123">-Name</span></span>
<span data-ttu-id="39d5e-124">Adja meg a szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="39d5e-124">Specify the name of the service.</span></span>

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

### <span data-ttu-id="39d5e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d5e-125">-ResourceGroupName</span></span>
<span data-ttu-id="39d5e-126">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="39d5e-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="39d5e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d5e-127">-ResourceId</span></span>
<span data-ttu-id="39d5e-128">A szolgáltatás Erőforrásazonosítója arm.</span><span class="sxs-lookup"><span data-stu-id="39d5e-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="39d5e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d5e-129">CommonParameters</span></span>
<span data-ttu-id="39d5e-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d5e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d5e-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39d5e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d5e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39d5e-132">INPUTS</span></span>

### <span data-ttu-id="39d5e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="39d5e-133">System.String</span></span>

## <span data-ttu-id="39d5e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d5e-134">OUTPUTS</span></span>

### <span data-ttu-id="39d5e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="39d5e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="39d5e-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39d5e-136">NOTES</span></span>

## <span data-ttu-id="39d5e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39d5e-137">RELATED LINKS</span></span>
