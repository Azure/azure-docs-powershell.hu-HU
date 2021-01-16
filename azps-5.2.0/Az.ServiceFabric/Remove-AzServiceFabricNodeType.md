---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357907"
---
# <span data-ttu-id="a6e4c-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="a6e4c-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="a6e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e4c-103">Teljes csomóponttípus eltávolítása a fürtből.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="a6e4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a6e4c-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6e4c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a6e4c-105">DESCRIPTION</span></span>
<span data-ttu-id="a6e4c-106">Az **Remove-AzServiceFabricNodeType** használatával eltávolíthatja az összes csomópontot egy adott csomóponttípusból és a csomóponttípust egy fürtből.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="a6e4c-107">Ez a parancs nem használható az elsődleges csomóponttípus törléséhez.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="a6e4c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a6e4c-108">EXAMPLES</span></span>

### <span data-ttu-id="a6e4c-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="a6e4c-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="a6e4c-110">Ez a parancs eltávolítja a NodeType "nt1" típust a fürtből.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="a6e4c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6e4c-111">PARAMETERS</span></span>

### <span data-ttu-id="a6e4c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e4c-112">-DefaultProfile</span></span>
<span data-ttu-id="a6e4c-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6e4c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a6e4c-114">-Name</span></span>
<span data-ttu-id="a6e4c-115">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="a6e4c-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a6e4c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a6e4c-116">-NodeType</span></span>
<span data-ttu-id="a6e4c-117">A csomóponttípus neve</span><span class="sxs-lookup"><span data-stu-id="a6e4c-117">The node type name</span></span>

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

### <span data-ttu-id="a6e4c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e4c-118">-ResourceGroupName</span></span>
<span data-ttu-id="a6e4c-119">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a6e4c-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6e4c-120">-Confirm</span></span>
<span data-ttu-id="a6e4c-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6e4c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6e4c-122">-WhatIf</span></span>
<span data-ttu-id="a6e4c-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6e4c-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6e4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e4c-125">CommonParameters</span></span>
<span data-ttu-id="a6e4c-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6e4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e4c-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6e4c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e4c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6e4c-128">INPUTS</span></span>

### <span data-ttu-id="a6e4c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a6e4c-129">System.String</span></span>

## <span data-ttu-id="a6e4c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6e4c-130">OUTPUTS</span></span>

### <span data-ttu-id="a6e4c-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a6e4c-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a6e4c-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a6e4c-132">NOTES</span></span>

## <span data-ttu-id="a6e4c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6e4c-133">RELATED LINKS</span></span>
