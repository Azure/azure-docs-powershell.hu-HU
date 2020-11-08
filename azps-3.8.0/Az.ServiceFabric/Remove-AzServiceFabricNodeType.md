---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: bc21812003ca7e71b9f7fa726aea766e924d2519
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011671"
---
# <span data-ttu-id="5e170-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5e170-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="5e170-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e170-102">SYNOPSIS</span></span>
<span data-ttu-id="5e170-103">Teljes csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="5e170-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="5e170-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e170-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e170-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e170-105">DESCRIPTION</span></span>
<span data-ttu-id="5e170-106">A **Remove-AzServiceFabricNodeType** eltávolíthatja az összes csomópontot egy adott csomópont-típusból és egy fürtből származó csomópont típusból.</span><span class="sxs-lookup"><span data-stu-id="5e170-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="5e170-107">Ez a parancs nem használható az elsődleges csomópont-típus törlésére.</span><span class="sxs-lookup"><span data-stu-id="5e170-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="5e170-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5e170-108">EXAMPLES</span></span>

### <span data-ttu-id="5e170-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5e170-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="5e170-110">Ez a parancs eltávolítja a NodeType "NT1" a fürtből.</span><span class="sxs-lookup"><span data-stu-id="5e170-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="5e170-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e170-111">PARAMETERS</span></span>

### <span data-ttu-id="5e170-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e170-112">-DefaultProfile</span></span>
<span data-ttu-id="5e170-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e170-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e170-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e170-114">-Name</span></span>
<span data-ttu-id="5e170-115">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="5e170-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="5e170-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="5e170-116">-NodeType</span></span>
<span data-ttu-id="5e170-117">A csomópont típusa név</span><span class="sxs-lookup"><span data-stu-id="5e170-117">The node type name</span></span>

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

### <span data-ttu-id="5e170-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e170-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e170-119">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="5e170-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5e170-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5e170-120">-Confirm</span></span>
<span data-ttu-id="5e170-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5e170-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e170-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e170-122">-WhatIf</span></span>
<span data-ttu-id="5e170-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5e170-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e170-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5e170-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e170-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e170-125">CommonParameters</span></span>
<span data-ttu-id="5e170-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e170-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e170-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e170-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e170-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e170-128">INPUTS</span></span>

### <span data-ttu-id="5e170-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5e170-129">System.String</span></span>

## <span data-ttu-id="5e170-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e170-130">OUTPUTS</span></span>

### <span data-ttu-id="5e170-131">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="5e170-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5e170-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e170-132">NOTES</span></span>

## <span data-ttu-id="5e170-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e170-133">RELATED LINKS</span></span>
