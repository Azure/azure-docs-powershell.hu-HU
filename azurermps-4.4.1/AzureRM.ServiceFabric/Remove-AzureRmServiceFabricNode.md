---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494668"
---
# <span data-ttu-id="de0fb-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="de0fb-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="de0fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="de0fb-102">SYNOPSIS</span></span>
<span data-ttu-id="de0fb-103">Csomópontok eltávolítása a megadott csomópont-típusból egy fürtből</span><span class="sxs-lookup"><span data-stu-id="de0fb-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de0fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="de0fb-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de0fb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="de0fb-105">DESCRIPTION</span></span>
<span data-ttu-id="de0fb-106">A **Remove-AzureRmServiceFabricNode** használatával eltávolíthatja a csomópontokat egy adott csomópontból a fürtből.</span><span class="sxs-lookup"><span data-stu-id="de0fb-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="de0fb-107">Az Eltávolítás csak akkor járjon le, ha az megfelel a fürtök állapotát jelző metrikának.</span><span class="sxs-lookup"><span data-stu-id="de0fb-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="de0fb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="de0fb-108">EXAMPLES</span></span>

### <span data-ttu-id="de0fb-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="de0fb-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="de0fb-110">Ez a parancs eltávolítja a 2 csomópontot a "NT1" NodeType.</span><span class="sxs-lookup"><span data-stu-id="de0fb-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="de0fb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="de0fb-111">PARAMETERS</span></span>

### <span data-ttu-id="de0fb-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="de0fb-112">-Name</span></span>
<span data-ttu-id="de0fb-113">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="de0fb-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="de0fb-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="de0fb-114">-NodeType</span></span>
<span data-ttu-id="de0fb-115">Csomópont típusa név.</span><span class="sxs-lookup"><span data-stu-id="de0fb-115">Node type name.</span></span>

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

### <span data-ttu-id="de0fb-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="de0fb-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="de0fb-117">Az eltávolítandó csomópontok száma.</span><span class="sxs-lookup"><span data-stu-id="de0fb-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="de0fb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de0fb-118">-ResourceGroupName</span></span>
<span data-ttu-id="de0fb-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de0fb-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="de0fb-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="de0fb-120">-Confirm</span></span>
<span data-ttu-id="de0fb-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="de0fb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de0fb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de0fb-122">-WhatIf</span></span>
<span data-ttu-id="de0fb-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="de0fb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de0fb-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de0fb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de0fb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de0fb-125">-DefaultProfile</span></span>
<span data-ttu-id="de0fb-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de0fb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de0fb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de0fb-127">CommonParameters</span></span>
<span data-ttu-id="de0fb-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="de0fb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de0fb-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de0fb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de0fb-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="de0fb-130">INPUTS</span></span>

### <span data-ttu-id="de0fb-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="de0fb-131">System.Int32</span></span>
<span data-ttu-id="de0fb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="de0fb-132">System.String</span></span>

## <span data-ttu-id="de0fb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de0fb-133">OUTPUTS</span></span>

### <span data-ttu-id="de0fb-134">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="de0fb-134">System.Object</span></span>

## <span data-ttu-id="de0fb-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="de0fb-135">NOTES</span></span>

## <span data-ttu-id="de0fb-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de0fb-136">RELATED LINKS</span></span>

[<span data-ttu-id="de0fb-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="de0fb-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
