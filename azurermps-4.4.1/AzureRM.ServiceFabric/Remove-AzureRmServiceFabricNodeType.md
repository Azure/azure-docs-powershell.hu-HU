---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 3da05194d74de1fe547beb66dea420a7f0e90155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494667"
---
# <span data-ttu-id="5ffa4-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="5ffa4-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="5ffa4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ffa4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffa4-103">Teljes csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="5ffa4-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ffa4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ffa4-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ffa4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ffa4-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffa4-106">A **Remove-AzureRmServiceFabricNodeType** eltávolíthatja az összes csomópontot egy adott csomópont-típusból és egy fürtből származó csomópont típusból.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="5ffa4-107">Ez a parancs nem használható az elsődleges csomópont-típus törlésére.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="5ffa4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5ffa4-108">EXAMPLES</span></span>

### <span data-ttu-id="5ffa4-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5ffa4-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="5ffa4-110">Ez a parancs eltávolítja a NodeType "NT1" a fürtből.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="5ffa4-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ffa4-111">PARAMETERS</span></span>

### <span data-ttu-id="5ffa4-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ffa4-112">-Name</span></span>
<span data-ttu-id="5ffa4-113">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5ffa4-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="5ffa4-114">-NodeType</span></span>
<span data-ttu-id="5ffa4-115">A csomópont típusa név.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-115">The node type name.</span></span>

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

### <span data-ttu-id="5ffa4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ffa4-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ffa4-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5ffa4-118">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ffa4-118">-Confirm</span></span>
<span data-ttu-id="5ffa4-119">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ffa4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ffa4-120">-WhatIf</span></span>
<span data-ttu-id="5ffa4-121">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ffa4-122">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ffa4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffa4-123">-DefaultProfile</span></span>
<span data-ttu-id="5ffa4-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ffa4-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ffa4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffa4-125">CommonParameters</span></span>
<span data-ttu-id="5ffa4-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ffa4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffa4-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ffa4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffa4-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ffa4-128">INPUTS</span></span>

### <span data-ttu-id="5ffa4-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5ffa4-129">System.String</span></span>

## <span data-ttu-id="5ffa4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ffa4-130">OUTPUTS</span></span>

### <span data-ttu-id="5ffa4-131">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="5ffa4-131">System.Object</span></span>

## <span data-ttu-id="5ffa4-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ffa4-132">NOTES</span></span>

## <span data-ttu-id="5ffa4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ffa4-133">RELATED LINKS</span></span>

