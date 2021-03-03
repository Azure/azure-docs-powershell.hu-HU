---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: b056e5328c24270df6a95e33b079e7b907f29fa3
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685019"
---
# <span data-ttu-id="866e1-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="866e1-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="866e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="866e1-102">SYNOPSIS</span></span>
<span data-ttu-id="866e1-103">Frissítse a fürt egyik csomóponttípusának 10.10-es szintjéhez vagy VmSku-jának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="866e1-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="866e1-104">Emellett frissíti a service fabric VM-bővítményben lévő tárolási réteget is a társított virtuálisgép-méretkészleten.</span><span class="sxs-lookup"><span data-stu-id="866e1-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866e1-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="866e1-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="866e1-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="866e1-106">DESCRIPTION</span></span>
<span data-ttu-id="866e1-107">Az **Update-AzureRmServiceFabricDurability** segítségével frissítheti a fürt minőségének vagy termékváltozatának frissítését.</span><span class="sxs-lookup"><span data-stu-id="866e1-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="866e1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="866e1-108">EXAMPLES</span></span>

### <span data-ttu-id="866e1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="866e1-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="866e1-110">Ez a parancs ezüstre módosítja az "nt1" NodeType-réteget.</span><span class="sxs-lookup"><span data-stu-id="866e1-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="866e1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="866e1-111">PARAMETERS</span></span>

### <span data-ttu-id="866e1-112">–10.</span><span class="sxs-lookup"><span data-stu-id="866e1-112">-DurabilityLevel</span></span>
<span data-ttu-id="866e1-113">Adja meg a megőrzési szintet.</span><span class="sxs-lookup"><span data-stu-id="866e1-113">Specify durability level.</span></span>

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

### <span data-ttu-id="866e1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="866e1-114">-Name</span></span>
<span data-ttu-id="866e1-115">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="866e1-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="866e1-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="866e1-116">-NodeType</span></span>
<span data-ttu-id="866e1-117">Adja meg a Service Fabric csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="866e1-117">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="866e1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866e1-118">-ResourceGroupName</span></span>
<span data-ttu-id="866e1-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="866e1-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="866e1-120">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="866e1-120">-Sku</span></span>
<span data-ttu-id="866e1-121">Adja meg a csomóponttípus termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="866e1-121">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="866e1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="866e1-122">-Confirm</span></span>
<span data-ttu-id="866e1-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="866e1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866e1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866e1-124">-WhatIf</span></span>
<span data-ttu-id="866e1-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="866e1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="866e1-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="866e1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866e1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866e1-127">-DefaultProfile</span></span>
<span data-ttu-id="866e1-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="866e1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="866e1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866e1-129">CommonParameters</span></span>
<span data-ttu-id="866e1-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866e1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866e1-131">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866e1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866e1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="866e1-132">INPUTS</span></span>

### <span data-ttu-id="866e1-133">Microsoft.Azure.Commands.ServiceFabric.Models.Fogaraslevel</span><span class="sxs-lookup"><span data-stu-id="866e1-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="866e1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="866e1-134">System.String</span></span>

## <span data-ttu-id="866e1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="866e1-135">OUTPUTS</span></span>

### <span data-ttu-id="866e1-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span><span class="sxs-lookup"><span data-stu-id="866e1-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="866e1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="866e1-137">NOTES</span></span>

## <span data-ttu-id="866e1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="866e1-138">RELATED LINKS</span></span>

