---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469145"
---
# <span data-ttu-id="607f4-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="607f4-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="607f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607f4-102">SYNOPSIS</span></span>
<span data-ttu-id="607f4-103">Hozzon létre jegyzetkészletet a megadott fürtben.</span><span class="sxs-lookup"><span data-stu-id="607f4-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="607f4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="607f4-104">SYNTAX</span></span>

### <span data-ttu-id="607f4-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="607f4-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="607f4-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="607f4-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="607f4-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="607f4-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="607f4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="607f4-108">DESCRIPTION</span></span>
<span data-ttu-id="607f4-109">Hozzon létre jegyzetkészletet a megadott fürtben.</span><span class="sxs-lookup"><span data-stu-id="607f4-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="607f4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="607f4-110">EXAMPLES</span></span>

### <span data-ttu-id="607f4-111">Az összes csomópontkészlet lekérte a megadott fürtön belül</span><span class="sxs-lookup"><span data-stu-id="607f4-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="607f4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="607f4-112">PARAMETERS</span></span>

### <span data-ttu-id="607f4-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="607f4-113">-ClusterName</span></span>
<span data-ttu-id="607f4-114">A felügyelt fürterőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="607f4-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="607f4-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="607f4-115">-ClusterObject</span></span>
<span data-ttu-id="607f4-116">A fürtobjektum.</span><span class="sxs-lookup"><span data-stu-id="607f4-116">The cluster object.</span></span>

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

### <span data-ttu-id="607f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607f4-117">-DefaultProfile</span></span>
<span data-ttu-id="607f4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="607f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="607f4-119">-Id</span><span class="sxs-lookup"><span data-stu-id="607f4-119">-Id</span></span>
<span data-ttu-id="607f4-120">A felügyelt Kubanetes-fürtben található csomópontkészlet azonosítója</span><span class="sxs-lookup"><span data-stu-id="607f4-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="607f4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="607f4-121">-Name</span></span>
<span data-ttu-id="607f4-122">A csomópontkészlet neve.</span><span class="sxs-lookup"><span data-stu-id="607f4-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="607f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="607f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="607f4-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="607f4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="607f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607f4-125">CommonParameters</span></span>
<span data-ttu-id="607f4-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607f4-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="607f4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607f4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="607f4-128">INPUTS</span></span>

### <span data-ttu-id="607f4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="607f4-129">System.String</span></span>

## <span data-ttu-id="607f4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="607f4-130">OUTPUTS</span></span>

### <span data-ttu-id="607f4-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="607f4-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="607f4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="607f4-132">NOTES</span></span>

## <span data-ttu-id="607f4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="607f4-133">RELATED LINKS</span></span>
