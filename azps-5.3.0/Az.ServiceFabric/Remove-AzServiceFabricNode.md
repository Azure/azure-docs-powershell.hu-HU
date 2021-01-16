---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: fd38b68c8133cbc498bbc50ffea84b48e58198a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479527"
---
# <span data-ttu-id="c81ad-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c81ad-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="c81ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c81ad-102">SYNOPSIS</span></span>
<span data-ttu-id="c81ad-103">Csomópontokat távolíthat el az adott csomóponttípusból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="c81ad-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="c81ad-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c81ad-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c81ad-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c81ad-105">DESCRIPTION</span></span>
<span data-ttu-id="c81ad-106">Az **Remove-AzServiceFabricNode** segítségével eltávolíthatja a csomópontokat egy adott csomóponttípusból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="c81ad-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="c81ad-107">Az eltávolítás csak akkor folytatódik, ha megfelel a fürt állapotát mutató metrikáknak.</span><span class="sxs-lookup"><span data-stu-id="c81ad-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="c81ad-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c81ad-108">EXAMPLES</span></span>

### <span data-ttu-id="c81ad-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="c81ad-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="c81ad-110">Ez a parancs eltávolít 2 csomópontot az "nt1" NodeType-ból.</span><span class="sxs-lookup"><span data-stu-id="c81ad-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="c81ad-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c81ad-111">PARAMETERS</span></span>

### <span data-ttu-id="c81ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81ad-112">-DefaultProfile</span></span>
<span data-ttu-id="c81ad-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c81ad-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c81ad-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c81ad-114">-Name</span></span>
<span data-ttu-id="c81ad-115">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="c81ad-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c81ad-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c81ad-116">-NodeType</span></span>
<span data-ttu-id="c81ad-117">Csomóponttípus neve</span><span class="sxs-lookup"><span data-stu-id="c81ad-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81ad-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="c81ad-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="c81ad-119">A hozzáadni megfelelő csomópontok száma</span><span class="sxs-lookup"><span data-stu-id="c81ad-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c81ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="c81ad-121">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="c81ad-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c81ad-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c81ad-122">-Confirm</span></span>
<span data-ttu-id="c81ad-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c81ad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81ad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81ad-124">-WhatIf</span></span>
<span data-ttu-id="c81ad-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c81ad-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81ad-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c81ad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81ad-127">CommonParameters</span></span>
<span data-ttu-id="c81ad-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c81ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81ad-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c81ad-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81ad-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c81ad-130">INPUTS</span></span>

### <span data-ttu-id="c81ad-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c81ad-131">System.Int32</span></span>

### <span data-ttu-id="c81ad-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c81ad-132">System.String</span></span>

## <span data-ttu-id="c81ad-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c81ad-133">OUTPUTS</span></span>

### <span data-ttu-id="c81ad-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="c81ad-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c81ad-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c81ad-135">NOTES</span></span>

## <span data-ttu-id="c81ad-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c81ad-136">RELATED LINKS</span></span>

[<span data-ttu-id="c81ad-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="c81ad-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
