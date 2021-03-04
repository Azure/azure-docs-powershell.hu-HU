---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricApplication.md
ms.openlocfilehash: 346664d4714836b9965088d946262257e76747e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924425"
---
# <span data-ttu-id="ba871-101">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ba871-101">Get-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ba871-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba871-102">SYNOPSIS</span></span>
<span data-ttu-id="ba871-103">A Service Fabric alkalmazás részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="ba871-103">Get Service Fabric application details.</span></span> <span data-ttu-id="ba871-104">Csak a telepített ARM támogatja.</span><span class="sxs-lookup"><span data-stu-id="ba871-104">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="ba871-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ba871-105">SYNTAX</span></span>

### <span data-ttu-id="ba871-106">ByResourceGroupAndCluster (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba871-106">ByResourceGroupAndCluster (Default)</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba871-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ba871-107">ByName</span></span>
```
Get-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba871-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba871-108">ByResourceId</span></span>
```
Get-AzServiceFabricApplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba871-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ba871-109">DESCRIPTION</span></span>
<span data-ttu-id="ba871-110">Ez a parancsmag az alkalmazás részleteit a megadott erőforráscsoportban és fürtben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ba871-110">This cmdlet gets the application details in the specified resource group and cluster.</span></span>

## <span data-ttu-id="ba871-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ba871-111">EXAMPLES</span></span>

### <span data-ttu-id="ba871-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="ba871-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="ba871-113">Ebben a példában a "testApp" alkalmazás erőforrás-adatait olvashatja be.</span><span class="sxs-lookup"><span data-stu-id="ba871-113">This example gets the application resource details for the application "testApp".</span></span>

### <span data-ttu-id="ba871-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="ba871-114">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> Get-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName
```

<span data-ttu-id="ba871-115">Ebben a példában a "testCluster" fürt alatti alkalmazások listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="ba871-115">This example gets a list of the applications under the cluster "testCluster".</span></span>

## <span data-ttu-id="ba871-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba871-116">PARAMETERS</span></span>

### <span data-ttu-id="ba871-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba871-117">-ClusterName</span></span>
<span data-ttu-id="ba871-118">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="ba871-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ba871-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba871-119">-DefaultProfile</span></span>
<span data-ttu-id="ba871-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba871-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba871-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ba871-121">-Name</span></span>
<span data-ttu-id="ba871-122">Adja meg az alkalmazás nevét.</span><span class="sxs-lookup"><span data-stu-id="ba871-122">Specify the name of the application.</span></span>

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

### <span data-ttu-id="ba871-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba871-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba871-124">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="ba871-124">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ba871-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba871-125">-ResourceId</span></span>
<span data-ttu-id="ba871-126">Arm ResourceId of the application.</span><span class="sxs-lookup"><span data-stu-id="ba871-126">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ba871-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba871-127">CommonParameters</span></span>
<span data-ttu-id="ba871-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba871-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba871-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba871-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba871-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ba871-130">INPUTS</span></span>

### <span data-ttu-id="ba871-131">System.String</span><span class="sxs-lookup"><span data-stu-id="ba871-131">System.String</span></span>

## <span data-ttu-id="ba871-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba871-132">OUTPUTS</span></span>

### <span data-ttu-id="ba871-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ba871-133">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ba871-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ba871-134">NOTES</span></span>

## <span data-ttu-id="ba871-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba871-135">RELATED LINKS</span></span>
