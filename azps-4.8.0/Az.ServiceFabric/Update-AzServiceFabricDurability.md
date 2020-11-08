---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183300"
---
# <span data-ttu-id="a281e-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="a281e-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="a281e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a281e-102">SYNOPSIS</span></span>
<span data-ttu-id="a281e-103">Módosítsa a VmSku tartóssági rétegét vagy egy csomópont típusát.</span><span class="sxs-lookup"><span data-stu-id="a281e-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="a281e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a281e-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a281e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a281e-105">DESCRIPTION</span></span>
<span data-ttu-id="a281e-106">A **AzServiceFabricDurability** frissítse a fürt tartósságát vagy SKU-ának frissítését.</span><span class="sxs-lookup"><span data-stu-id="a281e-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="a281e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a281e-107">EXAMPLES</span></span>

### <span data-ttu-id="a281e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a281e-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="a281e-109">Ez a parancs a "NT1" NodeType tartóssági rétegét ezüst értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="a281e-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="a281e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a281e-110">PARAMETERS</span></span>

### <span data-ttu-id="a281e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a281e-111">-DefaultProfile</span></span>
<span data-ttu-id="a281e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a281e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a281e-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a281e-113">-DurabilityLevel</span></span>
<span data-ttu-id="a281e-114">Adja meg a tartóssági szintet.</span><span class="sxs-lookup"><span data-stu-id="a281e-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a281e-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a281e-115">-Name</span></span>
<span data-ttu-id="a281e-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="a281e-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a281e-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a281e-117">-NodeType</span></span>
<span data-ttu-id="a281e-118">Adja meg a Service Fabric csomópont típusa nevet.</span><span class="sxs-lookup"><span data-stu-id="a281e-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="a281e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a281e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a281e-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a281e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a281e-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="a281e-121">-Sku</span></span>
<span data-ttu-id="a281e-122">Adja meg a csomópont típusának SKU-ot.</span><span class="sxs-lookup"><span data-stu-id="a281e-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a281e-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a281e-123">-Confirm</span></span>
<span data-ttu-id="a281e-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a281e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a281e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a281e-125">-WhatIf</span></span>
<span data-ttu-id="a281e-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a281e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a281e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a281e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a281e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a281e-128">CommonParameters</span></span>
<span data-ttu-id="a281e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a281e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a281e-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a281e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a281e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a281e-131">INPUTS</span></span>

### <span data-ttu-id="a281e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a281e-132">System.String</span></span>

### <span data-ttu-id="a281e-133">Microsoft. Azure. Command. ServiceFabric. models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="a281e-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="a281e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a281e-134">OUTPUTS</span></span>

### <span data-ttu-id="a281e-135">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a281e-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a281e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a281e-136">NOTES</span></span>

## <span data-ttu-id="a281e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a281e-137">RELATED LINKS</span></span>
