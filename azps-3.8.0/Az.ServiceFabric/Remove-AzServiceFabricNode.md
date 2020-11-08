---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 96706ef98a0b21bab06e2c6e8fae947dcd205271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011672"
---
# <span data-ttu-id="a6d0e-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a6d0e-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="a6d0e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d0e-103">Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből</span><span class="sxs-lookup"><span data-stu-id="a6d0e-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="a6d0e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6d0e-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6d0e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6d0e-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d0e-106">A **Remove-AzServiceFabricNode** használatával eltávolíthatja a csomópontokat egy adott csomópontból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="a6d0e-107">Az Eltávolítás csak akkor járjon le, ha az megfelel a fürtök állapotát jelző metrikának.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="a6d0e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a6d0e-108">EXAMPLES</span></span>

### <span data-ttu-id="a6d0e-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a6d0e-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="a6d0e-110">Ez a parancs eltávolítja a 2 csomópontot a "NT1" NodeType.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="a6d0e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6d0e-111">PARAMETERS</span></span>

### <span data-ttu-id="a6d0e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d0e-112">-DefaultProfile</span></span>
<span data-ttu-id="a6d0e-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6d0e-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a6d0e-114">-Name</span></span>
<span data-ttu-id="a6d0e-115">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="a6d0e-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a6d0e-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a6d0e-116">-NodeType</span></span>
<span data-ttu-id="a6d0e-117">Csomópont típusa név</span><span class="sxs-lookup"><span data-stu-id="a6d0e-117">Node type name</span></span>

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

### <span data-ttu-id="a6d0e-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="a6d0e-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="a6d0e-119">A hozzáadni kívánt csomópontok száma</span><span class="sxs-lookup"><span data-stu-id="a6d0e-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="a6d0e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d0e-120">-ResourceGroupName</span></span>
<span data-ttu-id="a6d0e-121">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a6d0e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a6d0e-122">-Confirm</span></span>
<span data-ttu-id="a6d0e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6d0e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6d0e-124">-WhatIf</span></span>
<span data-ttu-id="a6d0e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6d0e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a6d0e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6d0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d0e-127">CommonParameters</span></span>
<span data-ttu-id="a6d0e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6d0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d0e-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d0e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d0e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6d0e-130">INPUTS</span></span>

### <span data-ttu-id="a6d0e-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a6d0e-131">System.Int32</span></span>

### <span data-ttu-id="a6d0e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a6d0e-132">System.String</span></span>

## <span data-ttu-id="a6d0e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6d0e-133">OUTPUTS</span></span>

### <span data-ttu-id="a6d0e-134">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a6d0e-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a6d0e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6d0e-135">NOTES</span></span>

## <span data-ttu-id="a6d0e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6d0e-136">RELATED LINKS</span></span>

[<span data-ttu-id="a6d0e-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a6d0e-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
