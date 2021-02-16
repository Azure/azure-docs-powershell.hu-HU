---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158387"
---
# <span data-ttu-id="2ce2d-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2ce2d-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="2ce2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ce2d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce2d-103">Fürterőforrás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2ce2d-103">Remove cluster resource.</span></span>

## <span data-ttu-id="2ce2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2ce2d-104">SYNTAX</span></span>

### <span data-ttu-id="2ce2d-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ce2d-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ce2d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2ce2d-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ce2d-107">ById</span><span class="sxs-lookup"><span data-stu-id="2ce2d-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ce2d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2ce2d-108">DESCRIPTION</span></span>
<span data-ttu-id="2ce2d-109">Távolítsa el a fürtöt, ezzel a fürt alatt található csomóponttípusokat is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="2ce2d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2ce2d-110">EXAMPLES</span></span>

### <span data-ttu-id="2ce2d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2ce2d-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="2ce2d-112">Fürt eltávolítása gombra.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-112">Remove cluster.</span></span>

### <span data-ttu-id="2ce2d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2ce2d-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="2ce2d-114">A fürt eltávolítása pipázással.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="2ce2d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ce2d-115">PARAMETERS</span></span>

### <span data-ttu-id="2ce2d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ce2d-116">-AsJob</span></span>
<span data-ttu-id="2ce2d-117">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce2d-118">-DefaultProfile</span></span>
<span data-ttu-id="2ce2d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce2d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ce2d-120">-InputObject</span></span>
<span data-ttu-id="2ce2d-121">Felügyelt fürterőforrás</span><span class="sxs-lookup"><span data-stu-id="2ce2d-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2ce2d-122">-Name</span></span>
<span data-ttu-id="2ce2d-123">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ce2d-124">-PassThru</span></span>
<span data-ttu-id="2ce2d-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2ce2d-125">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ce2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="2ce2d-127">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ce2d-128">-ResourceId</span></span>
<span data-ttu-id="2ce2d-129">Felügyelt fürt erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2ce2d-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ce2d-130">-Confirm</span></span>
<span data-ttu-id="2ce2d-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ce2d-132">-WhatIf</span></span>
<span data-ttu-id="2ce2d-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ce2d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce2d-135">CommonParameters</span></span>
<span data-ttu-id="2ce2d-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce2d-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ce2d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce2d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ce2d-138">INPUTS</span></span>

### <span data-ttu-id="2ce2d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2ce2d-139">System.String</span></span>

## <span data-ttu-id="2ce2d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ce2d-140">OUTPUTS</span></span>

### <span data-ttu-id="2ce2d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ce2d-141">System.Boolean</span></span>

## <span data-ttu-id="2ce2d-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2ce2d-142">NOTES</span></span>

## <span data-ttu-id="2ce2d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ce2d-143">RELATED LINKS</span></span>
