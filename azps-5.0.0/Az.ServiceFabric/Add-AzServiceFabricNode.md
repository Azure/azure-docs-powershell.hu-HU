---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185679"
---
# <span data-ttu-id="f7cd7-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f7cd7-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="f7cd7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="f7cd7-103">Csomópontok hozzáadása a fürt adott csomópont-típusához</span><span class="sxs-lookup"><span data-stu-id="f7cd7-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="f7cd7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7cd7-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7cd7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7cd7-105">DESCRIPTION</span></span>
<span data-ttu-id="f7cd7-106">A **Add-AzServiceFabricNode** segítségével csomópontokat adhat hozzá az adott csomópont-típushoz.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="f7cd7-107">Csak meg kell adnia a csomópont típusához hozzáadni kívánt csomópontok számát.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="f7cd7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f7cd7-108">EXAMPLES</span></span>

### <span data-ttu-id="f7cd7-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7cd7-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="f7cd7-110">Ez a parancs 2 csomópontot ad hozzá az "N1" csomópont típushoz.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="f7cd7-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7cd7-111">PARAMETERS</span></span>

### <span data-ttu-id="f7cd7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7cd7-112">-DefaultProfile</span></span>
<span data-ttu-id="f7cd7-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7cd7-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7cd7-114">-Name</span></span>
<span data-ttu-id="f7cd7-115">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="f7cd7-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="f7cd7-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="f7cd7-116">-NodeType</span></span>
<span data-ttu-id="f7cd7-117">Csomópont típusa név</span><span class="sxs-lookup"><span data-stu-id="f7cd7-117">Node type name</span></span>

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

### <span data-ttu-id="f7cd7-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="f7cd7-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="f7cd7-119">A hozzáadni kívánt csomópontok száma</span><span class="sxs-lookup"><span data-stu-id="f7cd7-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="f7cd7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7cd7-120">-ResourceGroupName</span></span>
<span data-ttu-id="f7cd7-121">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="f7cd7-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7cd7-122">-Confirm</span></span>
<span data-ttu-id="f7cd7-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7cd7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7cd7-124">-WhatIf</span></span>
<span data-ttu-id="f7cd7-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7cd7-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7cd7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7cd7-127">CommonParameters</span></span>
<span data-ttu-id="f7cd7-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7cd7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7cd7-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f7cd7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7cd7-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7cd7-130">INPUTS</span></span>

### <span data-ttu-id="f7cd7-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f7cd7-131">System.Int32</span></span>

### <span data-ttu-id="f7cd7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f7cd7-132">System.String</span></span>

## <span data-ttu-id="f7cd7-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7cd7-133">OUTPUTS</span></span>

### <span data-ttu-id="f7cd7-134">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="f7cd7-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f7cd7-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7cd7-135">NOTES</span></span>

## <span data-ttu-id="f7cd7-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7cd7-136">RELATED LINKS</span></span>

[<span data-ttu-id="f7cd7-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f7cd7-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)