---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025991"
---
# <span data-ttu-id="be5d1-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="be5d1-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="be5d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="be5d1-103">A felügyelt csomópont típusa erőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="be5d1-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="be5d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be5d1-104">SYNTAX</span></span>

### <span data-ttu-id="be5d1-105">ByName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="be5d1-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be5d1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be5d1-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be5d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="be5d1-107">DESCRIPTION</span></span>
<span data-ttu-id="be5d1-108">A felügyelt csomópont típusa erőforrás részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="be5d1-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="be5d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="be5d1-109">EXAMPLES</span></span>

### <span data-ttu-id="be5d1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="be5d1-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="be5d1-111">A csomópont típusa részletének beszerzése</span><span class="sxs-lookup"><span data-stu-id="be5d1-111">Get node type details.</span></span>

### <span data-ttu-id="be5d1-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="be5d1-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="be5d1-113">A megadott szektorcsoport alatti csomópont-típusok listája</span><span class="sxs-lookup"><span data-stu-id="be5d1-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="be5d1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be5d1-114">PARAMETERS</span></span>

### <span data-ttu-id="be5d1-115">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="be5d1-115">-ClusterName</span></span>
<span data-ttu-id="be5d1-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="be5d1-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="be5d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be5d1-117">-DefaultProfile</span></span>
<span data-ttu-id="be5d1-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be5d1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be5d1-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be5d1-119">-Name</span></span>
<span data-ttu-id="be5d1-120">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="be5d1-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="be5d1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be5d1-121">-ResourceGroupName</span></span>
<span data-ttu-id="be5d1-122">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="be5d1-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="be5d1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5d1-123">CommonParameters</span></span>
<span data-ttu-id="be5d1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be5d1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5d1-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="be5d1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5d1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be5d1-126">INPUTS</span></span>

### <span data-ttu-id="be5d1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="be5d1-127">System.String</span></span>

## <span data-ttu-id="be5d1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be5d1-128">OUTPUTS</span></span>

### <span data-ttu-id="be5d1-129">Microsoft. Azure. Command. ServiceFabric. models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="be5d1-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="be5d1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be5d1-130">NOTES</span></span>

## <span data-ttu-id="be5d1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be5d1-131">RELATED LINKS</span></span>
