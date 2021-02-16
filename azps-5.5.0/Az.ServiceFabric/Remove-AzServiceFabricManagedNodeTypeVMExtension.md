---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150690"
---
# <span data-ttu-id="d87d5-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="d87d5-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="d87d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d87d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d87d5-103">Távolítsa el a vm-bővítményt a csomóponttípusból.</span><span class="sxs-lookup"><span data-stu-id="d87d5-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="d87d5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d87d5-104">SYNTAX</span></span>

### <span data-ttu-id="d87d5-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d87d5-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d87d5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d87d5-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d87d5-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d87d5-107">DESCRIPTION</span></span>
<span data-ttu-id="d87d5-108">Távolítsa el a vm bővítményt a csomóponttípusról név szerint.</span><span class="sxs-lookup"><span data-stu-id="d87d5-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="d87d5-109">A [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) használatával a VmExtensions tulajdonságot használva láthatja a csomóponttípus aktuális bővítményét.</span><span class="sxs-lookup"><span data-stu-id="d87d5-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="d87d5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d87d5-110">EXAMPLES</span></span>

### <span data-ttu-id="d87d5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="d87d5-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="d87d5-112">Távolítsa el a kiterjesztést a csomóponttípusról név szerint.</span><span class="sxs-lookup"><span data-stu-id="d87d5-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="d87d5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="d87d5-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="d87d5-114">Távolítsa el a kiterjesztést a csomóponttípusról név szerint, pipázással.</span><span class="sxs-lookup"><span data-stu-id="d87d5-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="d87d5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d87d5-115">PARAMETERS</span></span>

### <span data-ttu-id="d87d5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d87d5-116">-AsJob</span></span>
<span data-ttu-id="d87d5-117">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="d87d5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d87d5-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d87d5-118">-ClusterName</span></span>
<span data-ttu-id="d87d5-119">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="d87d5-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d87d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87d5-120">-DefaultProfile</span></span>
<span data-ttu-id="d87d5-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d87d5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d87d5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d87d5-122">-InputObject</span></span>
<span data-ttu-id="d87d5-123">Node type resource</span><span class="sxs-lookup"><span data-stu-id="d87d5-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d87d5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d87d5-124">-Name</span></span>
<span data-ttu-id="d87d5-125">bővítmény nevét.</span><span class="sxs-lookup"><span data-stu-id="d87d5-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d87d5-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="d87d5-126">-NodeTypeName</span></span>
<span data-ttu-id="d87d5-127">Adja meg a csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="d87d5-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d87d5-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d87d5-128">-PassThru</span></span>
<span data-ttu-id="d87d5-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d87d5-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d87d5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d87d5-130">-ResourceGroupName</span></span>
<span data-ttu-id="d87d5-131">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="d87d5-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d87d5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d87d5-132">-Confirm</span></span>
<span data-ttu-id="d87d5-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d87d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d87d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d87d5-134">-WhatIf</span></span>
<span data-ttu-id="d87d5-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d87d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d87d5-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d87d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d87d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87d5-137">CommonParameters</span></span>
<span data-ttu-id="d87d5-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d87d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87d5-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d87d5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87d5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d87d5-140">INPUTS</span></span>

### <span data-ttu-id="d87d5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d87d5-141">System.String</span></span>

## <span data-ttu-id="d87d5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d87d5-142">OUTPUTS</span></span>

### <span data-ttu-id="d87d5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d87d5-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="d87d5-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d87d5-144">NOTES</span></span>

## <span data-ttu-id="d87d5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d87d5-145">RELATED LINKS</span></span>
