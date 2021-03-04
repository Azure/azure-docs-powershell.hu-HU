---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 34b55a5da226a3985cb6fe3bede244ee1e054726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934649"
---
# <span data-ttu-id="9e5d1-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="9e5d1-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="9e5d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5d1-103">Csomópontok hozzáadása a fürt adott csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="9e5d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9e5d1-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e5d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9e5d1-105">DESCRIPTION</span></span>
<span data-ttu-id="9e5d1-106">Az **Add-AzServiceFabricNode** segítségével csomópontokat adhat az adott csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="9e5d1-107">Csak meg kell adnia a csomóponttípushoz hozzáadni kívánt csomópontok számát.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="9e5d1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9e5d1-108">EXAMPLES</span></span>

### <span data-ttu-id="9e5d1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="9e5d1-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="9e5d1-110">Ez a parancs 2 csomópontot ad az "n1" csomóponttípushoz.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="9e5d1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e5d1-111">PARAMETERS</span></span>

### <span data-ttu-id="9e5d1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5d1-112">-DefaultProfile</span></span>
<span data-ttu-id="9e5d1-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e5d1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9e5d1-114">-Name</span></span>
<span data-ttu-id="9e5d1-115">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="9e5d1-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="9e5d1-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="9e5d1-116">-NodeType</span></span>
<span data-ttu-id="9e5d1-117">Csomóponttípus neve</span><span class="sxs-lookup"><span data-stu-id="9e5d1-117">Node type name</span></span>

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

### <span data-ttu-id="9e5d1-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="9e5d1-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="9e5d1-119">A hozzáadni megfelelő csomópontok száma</span><span class="sxs-lookup"><span data-stu-id="9e5d1-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="9e5d1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e5d1-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e5d1-121">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="9e5d1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e5d1-122">-Confirm</span></span>
<span data-ttu-id="9e5d1-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e5d1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e5d1-124">-WhatIf</span></span>
<span data-ttu-id="9e5d1-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e5d1-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e5d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5d1-127">CommonParameters</span></span>
<span data-ttu-id="9e5d1-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e5d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5d1-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e5d1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5d1-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e5d1-130">INPUTS</span></span>

### <span data-ttu-id="9e5d1-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9e5d1-131">System.Int32</span></span>

### <span data-ttu-id="9e5d1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9e5d1-132">System.String</span></span>

## <span data-ttu-id="9e5d1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e5d1-133">OUTPUTS</span></span>

### <span data-ttu-id="9e5d1-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="9e5d1-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="9e5d1-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9e5d1-135">NOTES</span></span>

## <span data-ttu-id="9e5d1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e5d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="9e5d1-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="9e5d1-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
