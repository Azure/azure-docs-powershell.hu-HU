---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343314"
---
# <span data-ttu-id="85c65-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="85c65-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="85c65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c65-102">SYNOPSIS</span></span>
<span data-ttu-id="85c65-103">Frissítse a fürt egyik csomóponttípusának 10.10-es szintjéhez vagy VmSku-jának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="85c65-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="85c65-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="85c65-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c65-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="85c65-105">DESCRIPTION</span></span>
<span data-ttu-id="85c65-106">Az **Update-AzServiceFabricDurability** segítségével frissítheti a fürt minőségének vagy termékváltozatának frissítését.</span><span class="sxs-lookup"><span data-stu-id="85c65-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="85c65-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="85c65-107">EXAMPLES</span></span>

### <span data-ttu-id="85c65-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="85c65-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="85c65-109">Ez a parancs ezüstre módosítja az "nt1" NodeType-réteget.</span><span class="sxs-lookup"><span data-stu-id="85c65-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="85c65-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85c65-110">PARAMETERS</span></span>

### <span data-ttu-id="85c65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c65-111">-DefaultProfile</span></span>
<span data-ttu-id="85c65-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85c65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c65-113">–10.</span><span class="sxs-lookup"><span data-stu-id="85c65-113">-DurabilityLevel</span></span>
<span data-ttu-id="85c65-114">Adja meg a megőrzési szintet.</span><span class="sxs-lookup"><span data-stu-id="85c65-114">Specify durability level.</span></span>

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

### <span data-ttu-id="85c65-115">-Name</span><span class="sxs-lookup"><span data-stu-id="85c65-115">-Name</span></span>
<span data-ttu-id="85c65-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="85c65-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="85c65-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="85c65-117">-NodeType</span></span>
<span data-ttu-id="85c65-118">Adja meg a Service Fabric csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="85c65-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="85c65-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c65-119">-ResourceGroupName</span></span>
<span data-ttu-id="85c65-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="85c65-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="85c65-121">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="85c65-121">-Sku</span></span>
<span data-ttu-id="85c65-122">Adja meg a csomóponttípus termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="85c65-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="85c65-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85c65-123">-Confirm</span></span>
<span data-ttu-id="85c65-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="85c65-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c65-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c65-125">-WhatIf</span></span>
<span data-ttu-id="85c65-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="85c65-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85c65-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="85c65-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c65-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c65-128">CommonParameters</span></span>
<span data-ttu-id="85c65-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c65-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c65-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85c65-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c65-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85c65-131">INPUTS</span></span>

### <span data-ttu-id="85c65-132">System.String</span><span class="sxs-lookup"><span data-stu-id="85c65-132">System.String</span></span>

### <span data-ttu-id="85c65-133">Microsoft.Azure.Commands.ServiceFabric.Models.Fogaraslevel</span><span class="sxs-lookup"><span data-stu-id="85c65-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="85c65-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85c65-134">OUTPUTS</span></span>

### <span data-ttu-id="85c65-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="85c65-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="85c65-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="85c65-136">NOTES</span></span>

## <span data-ttu-id="85c65-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85c65-137">RELATED LINKS</span></span>
