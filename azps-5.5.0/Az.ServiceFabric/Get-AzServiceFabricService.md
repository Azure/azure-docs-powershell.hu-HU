---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricService.md
ms.openlocfilehash: d927ef9a8a1c3ef97976911b122f22e1948f2996
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165066"
---
# <span data-ttu-id="568ec-101">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="568ec-101">Get-AzServiceFabricService</span></span>

## <span data-ttu-id="568ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="568ec-102">SYNOPSIS</span></span>
<span data-ttu-id="568ec-103">A Service Fabric szolgáltatás részleteinek lekérte a megadott alkalmazás és fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="568ec-103">Get Service Fabric service details under the specified application and cluster.</span></span> <span data-ttu-id="568ec-104">Csak az ARM támogatott.</span><span class="sxs-lookup"><span data-stu-id="568ec-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="568ec-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="568ec-105">SYNTAX</span></span>

### <span data-ttu-id="568ec-106">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="568ec-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="568ec-107">ByName</span><span class="sxs-lookup"><span data-stu-id="568ec-107">ByName</span></span>
```
Get-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="568ec-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="568ec-108">ByResourceId</span></span>
```
Get-AzServiceFabricService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="568ec-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="568ec-109">DESCRIPTION</span></span>
<span data-ttu-id="568ec-110">Ez a parancsmag a szolgáltatás részleteit a megadott alkalmazásból és fürtből fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="568ec-110">This cmdlet will get the service details in the specified application and cluster.</span></span>

## <span data-ttu-id="568ec-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="568ec-111">EXAMPLES</span></span>

### <span data-ttu-id="568ec-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="568ec-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService"
PS C:\> Get-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="568ec-113">Ez a példa a "testApp~testService" szolgáltatás szolgáltatáserőforrás-adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="568ec-113">This example gets the service resource details for the service "testApp~testService".</span></span>

### <span data-ttu-id="568ec-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="568ec-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName
```

<span data-ttu-id="568ec-115">Ebben a példában a "testApp" alkalmazás alatt található szolgáltatások listája szerepel.</span><span class="sxs-lookup"><span data-stu-id="568ec-115">This example gets a list of the services under the application "testApp".</span></span>

## <span data-ttu-id="568ec-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="568ec-116">PARAMETERS</span></span>

### <span data-ttu-id="568ec-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="568ec-117">-ApplicationName</span></span>
<span data-ttu-id="568ec-118">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="568ec-118">Specify the name of the application.</span></span>

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

### <span data-ttu-id="568ec-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="568ec-119">-ClusterName</span></span>
<span data-ttu-id="568ec-120">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="568ec-120">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="568ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="568ec-121">-DefaultProfile</span></span>
<span data-ttu-id="568ec-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="568ec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="568ec-123">-Name</span><span class="sxs-lookup"><span data-stu-id="568ec-123">-Name</span></span>
<span data-ttu-id="568ec-124">Adja meg a szolgáltatás nevét.</span><span class="sxs-lookup"><span data-stu-id="568ec-124">Specify the name of the service.</span></span>

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

### <span data-ttu-id="568ec-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="568ec-125">-ResourceGroupName</span></span>
<span data-ttu-id="568ec-126">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="568ec-126">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="568ec-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="568ec-127">-ResourceId</span></span>
<span data-ttu-id="568ec-128">A szolgáltatás Erőforrásazonosítója arm.</span><span class="sxs-lookup"><span data-stu-id="568ec-128">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="568ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="568ec-129">CommonParameters</span></span>
<span data-ttu-id="568ec-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="568ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="568ec-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="568ec-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="568ec-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="568ec-132">INPUTS</span></span>

### <span data-ttu-id="568ec-133">System.String</span><span class="sxs-lookup"><span data-stu-id="568ec-133">System.String</span></span>

## <span data-ttu-id="568ec-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="568ec-134">OUTPUTS</span></span>

### <span data-ttu-id="568ec-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span><span class="sxs-lookup"><span data-stu-id="568ec-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="568ec-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="568ec-136">NOTES</span></span>

## <span data-ttu-id="568ec-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="568ec-137">RELATED LINKS</span></span>
