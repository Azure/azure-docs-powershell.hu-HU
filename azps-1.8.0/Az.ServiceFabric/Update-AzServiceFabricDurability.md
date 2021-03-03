---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 8aec0babd295e6208cd0b1b055880fcd71164592
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684875"
---
# <span data-ttu-id="67450-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="67450-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="67450-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67450-102">SYNOPSIS</span></span>
<span data-ttu-id="67450-103">Frissítse a fürt egyik csomóponttípusának 10.10-es szintjéhez vagy VmSku-jának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="67450-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="67450-104">Emellett frissíti a service fabric VM-bővítményben lévő tárolási réteget is a társított virtuálisgép-méretkészleten.</span><span class="sxs-lookup"><span data-stu-id="67450-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

## <span data-ttu-id="67450-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="67450-105">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67450-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="67450-106">DESCRIPTION</span></span>
<span data-ttu-id="67450-107">Az **Update-AzServiceFabricDurability** segítségével frissítheti a fürt minőségének vagy termékváltozatának frissítését.</span><span class="sxs-lookup"><span data-stu-id="67450-107">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="67450-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="67450-108">EXAMPLES</span></span>

### <span data-ttu-id="67450-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="67450-109">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="67450-110">Ez a parancs ezüstre módosítja az "nt1" NodeType-réteget.</span><span class="sxs-lookup"><span data-stu-id="67450-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="67450-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67450-111">PARAMETERS</span></span>

### <span data-ttu-id="67450-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67450-112">-DefaultProfile</span></span>
<span data-ttu-id="67450-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67450-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67450-114">–10.</span><span class="sxs-lookup"><span data-stu-id="67450-114">-DurabilityLevel</span></span>
<span data-ttu-id="67450-115">Adja meg a megőrzési szintet.</span><span class="sxs-lookup"><span data-stu-id="67450-115">Specify durability level.</span></span>

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

### <span data-ttu-id="67450-116">-Name</span><span class="sxs-lookup"><span data-stu-id="67450-116">-Name</span></span>
<span data-ttu-id="67450-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="67450-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="67450-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="67450-118">-NodeType</span></span>
<span data-ttu-id="67450-119">Adja meg a Service Fabric csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="67450-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="67450-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67450-120">-ResourceGroupName</span></span>
<span data-ttu-id="67450-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67450-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="67450-122">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="67450-122">-Sku</span></span>
<span data-ttu-id="67450-123">Adja meg a csomóponttípus termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="67450-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="67450-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67450-124">-Confirm</span></span>
<span data-ttu-id="67450-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="67450-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67450-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67450-126">-WhatIf</span></span>
<span data-ttu-id="67450-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="67450-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67450-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="67450-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67450-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67450-129">CommonParameters</span></span>
<span data-ttu-id="67450-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67450-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67450-131">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67450-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67450-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67450-132">INPUTS</span></span>

### <span data-ttu-id="67450-133">System.String</span><span class="sxs-lookup"><span data-stu-id="67450-133">System.String</span></span>

### <span data-ttu-id="67450-134">Microsoft.Azure.Commands.ServiceFabric.Models.Fogaraslevel</span><span class="sxs-lookup"><span data-stu-id="67450-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="67450-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67450-135">OUTPUTS</span></span>

### <span data-ttu-id="67450-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="67450-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="67450-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="67450-137">NOTES</span></span>

## <span data-ttu-id="67450-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67450-138">RELATED LINKS</span></span>
