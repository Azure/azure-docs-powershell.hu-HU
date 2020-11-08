---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185858"
---
# <span data-ttu-id="7086f-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="7086f-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="7086f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7086f-102">SYNOPSIS</span></span>
<span data-ttu-id="7086f-103">Távolítsa el a VM kiterjesztést a Node típusból.</span><span class="sxs-lookup"><span data-stu-id="7086f-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="7086f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7086f-104">SYNTAX</span></span>

### <span data-ttu-id="7086f-105">ByObj (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7086f-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7086f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7086f-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7086f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7086f-107">DESCRIPTION</span></span>
<span data-ttu-id="7086f-108">A VM kiterjesztés eltávolítása a csomópont típusától név szerint.</span><span class="sxs-lookup"><span data-stu-id="7086f-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="7086f-109">Használja a [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) , és tekintse meg a VmExtensions tulajdonságot, és tekintse meg a csomópont típusának aktuális kiterjesztését.</span><span class="sxs-lookup"><span data-stu-id="7086f-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="7086f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7086f-110">EXAMPLES</span></span>

### <span data-ttu-id="7086f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7086f-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="7086f-112">A kiterjesztés eltávolítása a csomópont típusáról név szerint</span><span class="sxs-lookup"><span data-stu-id="7086f-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="7086f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7086f-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="7086f-114">A csomópont-típus kiterjesztését név szerint távolíthatja el a csövekkel.</span><span class="sxs-lookup"><span data-stu-id="7086f-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="7086f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7086f-115">PARAMETERS</span></span>

### <span data-ttu-id="7086f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7086f-116">-AsJob</span></span>
<span data-ttu-id="7086f-117">Futtassa a parancsmagot a háttérben, és a tevékenység visszaadása a folyamat nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="7086f-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7086f-118">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="7086f-118">-ClusterName</span></span>
<span data-ttu-id="7086f-119">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="7086f-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7086f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7086f-120">-DefaultProfile</span></span>
<span data-ttu-id="7086f-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7086f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7086f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7086f-122">-InputObject</span></span>
<span data-ttu-id="7086f-123">Csomópont típusa erőforrás</span><span class="sxs-lookup"><span data-stu-id="7086f-123">Node type resource</span></span>

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

### <span data-ttu-id="7086f-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7086f-124">-Name</span></span>
<span data-ttu-id="7086f-125">a kiterjesztés neve</span><span class="sxs-lookup"><span data-stu-id="7086f-125">extension name.</span></span>

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

### <span data-ttu-id="7086f-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="7086f-126">-NodeTypeName</span></span>
<span data-ttu-id="7086f-127">Adja meg a csomópont típusának a nevét.</span><span class="sxs-lookup"><span data-stu-id="7086f-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="7086f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7086f-128">-PassThru</span></span>
<span data-ttu-id="7086f-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7086f-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7086f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7086f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7086f-131">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="7086f-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7086f-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7086f-132">-Confirm</span></span>
<span data-ttu-id="7086f-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7086f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7086f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7086f-134">-WhatIf</span></span>
<span data-ttu-id="7086f-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7086f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7086f-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7086f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7086f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7086f-137">CommonParameters</span></span>
<span data-ttu-id="7086f-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7086f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7086f-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7086f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7086f-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7086f-140">INPUTS</span></span>

### <span data-ttu-id="7086f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7086f-141">System.String</span></span>

## <span data-ttu-id="7086f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7086f-142">OUTPUTS</span></span>

### <span data-ttu-id="7086f-143">Microsoft. Azure. Command. ServiceFabric. models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="7086f-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="7086f-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7086f-144">NOTES</span></span>

## <span data-ttu-id="7086f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7086f-145">RELATED LINKS</span></span>