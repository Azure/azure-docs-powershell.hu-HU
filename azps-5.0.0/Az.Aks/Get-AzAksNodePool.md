---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187117"
---
# <span data-ttu-id="bb0be-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="bb0be-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="bb0be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb0be-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0be-103">A megadott szektorcsoportban hozzon létre egy jegyzet-gyűjtőt.</span><span class="sxs-lookup"><span data-stu-id="bb0be-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="bb0be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb0be-104">SYNTAX</span></span>

### <span data-ttu-id="bb0be-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bb0be-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb0be-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb0be-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb0be-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb0be-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb0be-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb0be-108">DESCRIPTION</span></span>
<span data-ttu-id="bb0be-109">A megadott szektorcsoportban hozzon létre egy jegyzet-gyűjtőt.</span><span class="sxs-lookup"><span data-stu-id="bb0be-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="bb0be-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bb0be-110">EXAMPLES</span></span>

### <span data-ttu-id="bb0be-111">Az összes csomópont-készlet beolvasása adott fürtön belül</span><span class="sxs-lookup"><span data-stu-id="bb0be-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="bb0be-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb0be-112">PARAMETERS</span></span>

### <span data-ttu-id="bb0be-113">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="bb0be-113">-ClusterName</span></span>
<span data-ttu-id="bb0be-114">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="bb0be-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="bb0be-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="bb0be-115">-ClusterObject</span></span>
<span data-ttu-id="bb0be-116">A cluster objektum.</span><span class="sxs-lookup"><span data-stu-id="bb0be-116">The cluster object.</span></span>

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

### <span data-ttu-id="bb0be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0be-117">-DefaultProfile</span></span>
<span data-ttu-id="bb0be-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bb0be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb0be-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="bb0be-119">-Id</span></span>
<span data-ttu-id="bb0be-120">Node-készlet azonosítója a felügyelt Kubernetes-fürtben</span><span class="sxs-lookup"><span data-stu-id="bb0be-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="bb0be-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bb0be-121">-Name</span></span>
<span data-ttu-id="bb0be-122">A csomópont-készlet neve.</span><span class="sxs-lookup"><span data-stu-id="bb0be-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="bb0be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb0be-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb0be-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="bb0be-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="bb0be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0be-125">CommonParameters</span></span>
<span data-ttu-id="bb0be-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb0be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0be-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bb0be-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0be-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb0be-128">INPUTS</span></span>

### <span data-ttu-id="bb0be-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bb0be-129">System.String</span></span>

## <span data-ttu-id="bb0be-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb0be-130">OUTPUTS</span></span>

### <span data-ttu-id="bb0be-131">Microsoft. Azure. Command. AK. models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="bb0be-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="bb0be-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb0be-132">NOTES</span></span>

## <span data-ttu-id="bb0be-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb0be-133">RELATED LINKS</span></span>
