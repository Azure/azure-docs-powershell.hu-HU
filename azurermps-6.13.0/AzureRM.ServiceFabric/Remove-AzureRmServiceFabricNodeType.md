---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 36cad62f67be4273d363277e52f4dc8d2c91373c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502896"
---
# <span data-ttu-id="85df1-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="85df1-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="85df1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85df1-102">SYNOPSIS</span></span>
<span data-ttu-id="85df1-103">Teljes csomópont-típus eltávolítása a fürtből</span><span class="sxs-lookup"><span data-stu-id="85df1-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85df1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85df1-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85df1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85df1-105">DESCRIPTION</span></span>
<span data-ttu-id="85df1-106">A **Remove-AzureRmServiceFabricNodeType** eltávolíthatja az összes csomópontot egy adott csomópont-típusból és egy fürtből származó csomópont típusból.</span><span class="sxs-lookup"><span data-stu-id="85df1-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="85df1-107">Ez a parancs nem használható az elsődleges csomópont-típus törlésére.</span><span class="sxs-lookup"><span data-stu-id="85df1-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="85df1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="85df1-108">EXAMPLES</span></span>

### <span data-ttu-id="85df1-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="85df1-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="85df1-110">Ez a parancs eltávolítja a NodeType "NT1" a fürtből.</span><span class="sxs-lookup"><span data-stu-id="85df1-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="85df1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85df1-111">PARAMETERS</span></span>

### <span data-ttu-id="85df1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85df1-112">-DefaultProfile</span></span>
<span data-ttu-id="85df1-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85df1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85df1-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="85df1-114">-Name</span></span>
<span data-ttu-id="85df1-115">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="85df1-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="85df1-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="85df1-116">-NodeType</span></span>
<span data-ttu-id="85df1-117">A csomópont típusa név.</span><span class="sxs-lookup"><span data-stu-id="85df1-117">The node type name.</span></span>

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

### <span data-ttu-id="85df1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85df1-118">-ResourceGroupName</span></span>
<span data-ttu-id="85df1-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85df1-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="85df1-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="85df1-120">-Confirm</span></span>
<span data-ttu-id="85df1-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="85df1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85df1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85df1-122">-WhatIf</span></span>
<span data-ttu-id="85df1-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="85df1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85df1-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85df1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85df1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85df1-125">CommonParameters</span></span>
<span data-ttu-id="85df1-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85df1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85df1-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85df1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85df1-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85df1-128">INPUTS</span></span>

### <span data-ttu-id="85df1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="85df1-129">System.String</span></span>
<span data-ttu-id="85df1-130">Paraméterek: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="85df1-130">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="85df1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85df1-131">OUTPUTS</span></span>

### <span data-ttu-id="85df1-132">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="85df1-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="85df1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85df1-133">NOTES</span></span>

## <span data-ttu-id="85df1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85df1-134">RELATED LINKS</span></span>
