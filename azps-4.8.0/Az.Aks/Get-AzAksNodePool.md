---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183413"
---
# <span data-ttu-id="a2f0a-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="a2f0a-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="a2f0a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f0a-103">A megadott szektorcsoportban hozzon létre egy jegyzet-gyűjtőt.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="a2f0a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2f0a-104">SYNTAX</span></span>

### <span data-ttu-id="a2f0a-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a2f0a-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2f0a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2f0a-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2f0a-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2f0a-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2f0a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2f0a-108">DESCRIPTION</span></span>
<span data-ttu-id="a2f0a-109">A megadott szektorcsoportban hozzon létre egy jegyzet-gyűjtőt.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="a2f0a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a2f0a-110">EXAMPLES</span></span>

### <span data-ttu-id="a2f0a-111">Az összes csomópont-készlet beolvasása adott fürtön belül</span><span class="sxs-lookup"><span data-stu-id="a2f0a-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="a2f0a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2f0a-112">PARAMETERS</span></span>

### <span data-ttu-id="a2f0a-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="a2f0a-113">-ClusterName</span></span>
<span data-ttu-id="a2f0a-114">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f0a-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="a2f0a-115">-ClusterObject</span></span>
<span data-ttu-id="a2f0a-116">A cluster objektum.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f0a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f0a-117">-DefaultProfile</span></span>
<span data-ttu-id="a2f0a-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2f0a-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a2f0a-119">-Id</span></span>
<span data-ttu-id="a2f0a-120">Node-készlet azonosítója a felügyelt Kubernetes-fürtben</span><span class="sxs-lookup"><span data-stu-id="a2f0a-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2f0a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2f0a-121">-Name</span></span>
<span data-ttu-id="a2f0a-122">A csomópont-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f0a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f0a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2f0a-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2f0a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f0a-125">CommonParameters</span></span>
<span data-ttu-id="a2f0a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2f0a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f0a-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a2f0a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f0a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2f0a-128">INPUTS</span></span>

### <span data-ttu-id="a2f0a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a2f0a-129">System.String</span></span>

## <span data-ttu-id="a2f0a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2f0a-130">OUTPUTS</span></span>

### <span data-ttu-id="a2f0a-131">Microsoft. Azure. Command. AK. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="a2f0a-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="a2f0a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2f0a-132">NOTES</span></span>

## <span data-ttu-id="a2f0a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2f0a-133">RELATED LINKS</span></span>
