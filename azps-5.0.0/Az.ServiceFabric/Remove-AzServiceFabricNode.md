---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 3580315755792aaaddf3b10e185413254784a3d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195317"
---
# <span data-ttu-id="044a5-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="044a5-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="044a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="044a5-102">SYNOPSIS</span></span>
<span data-ttu-id="044a5-103">Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből</span><span class="sxs-lookup"><span data-stu-id="044a5-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="044a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="044a5-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="044a5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="044a5-105">DESCRIPTION</span></span>
<span data-ttu-id="044a5-106">A **Remove-AzServiceFabricNode** használatával eltávolíthatja a csomópontokat egy adott csomópontból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="044a5-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="044a5-107">Az Eltávolítás csak akkor járjon le, ha az megfelel a fürtök állapotát jelző metrikának.</span><span class="sxs-lookup"><span data-stu-id="044a5-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="044a5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="044a5-108">EXAMPLES</span></span>

### <span data-ttu-id="044a5-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="044a5-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="044a5-110">Ez a parancs eltávolítja a 2 csomópontot a "NT1" NodeType.</span><span class="sxs-lookup"><span data-stu-id="044a5-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="044a5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="044a5-111">PARAMETERS</span></span>

### <span data-ttu-id="044a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="044a5-112">-DefaultProfile</span></span>
<span data-ttu-id="044a5-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="044a5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="044a5-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="044a5-114">-Name</span></span>
<span data-ttu-id="044a5-115">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="044a5-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="044a5-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="044a5-116">-NodeType</span></span>
<span data-ttu-id="044a5-117">Csomópont típusa név</span><span class="sxs-lookup"><span data-stu-id="044a5-117">Node type name</span></span>

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

### <span data-ttu-id="044a5-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="044a5-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="044a5-119">A hozzáadni kívánt csomópontok száma</span><span class="sxs-lookup"><span data-stu-id="044a5-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="044a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="044a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="044a5-121">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="044a5-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="044a5-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="044a5-122">-Confirm</span></span>
<span data-ttu-id="044a5-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="044a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="044a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="044a5-124">-WhatIf</span></span>
<span data-ttu-id="044a5-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="044a5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="044a5-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="044a5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="044a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="044a5-127">CommonParameters</span></span>
<span data-ttu-id="044a5-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="044a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="044a5-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="044a5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="044a5-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="044a5-130">INPUTS</span></span>

### <span data-ttu-id="044a5-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="044a5-131">System.Int32</span></span>

### <span data-ttu-id="044a5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="044a5-132">System.String</span></span>

## <span data-ttu-id="044a5-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="044a5-133">OUTPUTS</span></span>

### <span data-ttu-id="044a5-134">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="044a5-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="044a5-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="044a5-135">NOTES</span></span>

## <span data-ttu-id="044a5-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="044a5-136">RELATED LINKS</span></span>

[<span data-ttu-id="044a5-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="044a5-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
