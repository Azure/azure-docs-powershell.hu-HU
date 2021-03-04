---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 15ba499908a4a631a22f9064b1938d3b32fdafd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920426"
---
# <span data-ttu-id="90247-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="90247-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="90247-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90247-102">SYNOPSIS</span></span>
<span data-ttu-id="90247-103">A felügyelt csomópont típusú erőforrás részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="90247-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="90247-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90247-104">SYNTAX</span></span>

### <span data-ttu-id="90247-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="90247-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90247-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="90247-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90247-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90247-107">DESCRIPTION</span></span>
<span data-ttu-id="90247-108">A felügyelt csomópont típusú erőforrás részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="90247-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="90247-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90247-109">EXAMPLES</span></span>

### <span data-ttu-id="90247-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="90247-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="90247-111">Csomóponttípus részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="90247-111">Get node type details.</span></span>

### <span data-ttu-id="90247-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="90247-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="90247-113">A csomóponttípusok listájának lekérte a megadott fürt alatt.</span><span class="sxs-lookup"><span data-stu-id="90247-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="90247-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90247-114">PARAMETERS</span></span>

### <span data-ttu-id="90247-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="90247-115">-ClusterName</span></span>
<span data-ttu-id="90247-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="90247-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90247-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90247-117">-DefaultProfile</span></span>
<span data-ttu-id="90247-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90247-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90247-119">-Name</span><span class="sxs-lookup"><span data-stu-id="90247-119">-Name</span></span>
<span data-ttu-id="90247-120">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="90247-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90247-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90247-121">-ResourceGroupName</span></span>
<span data-ttu-id="90247-122">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="90247-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90247-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90247-123">CommonParameters</span></span>
<span data-ttu-id="90247-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90247-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90247-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90247-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90247-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90247-126">INPUTS</span></span>

### <span data-ttu-id="90247-127">System.String</span><span class="sxs-lookup"><span data-stu-id="90247-127">System.String</span></span>

## <span data-ttu-id="90247-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90247-128">OUTPUTS</span></span>

### <span data-ttu-id="90247-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="90247-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="90247-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90247-130">NOTES</span></span>

## <span data-ttu-id="90247-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90247-131">RELATED LINKS</span></span>
