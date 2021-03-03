---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: aa53d34fcacca6515832eba9a6b302a4e56c7ccf
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685006"
---
# <span data-ttu-id="470bd-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="470bd-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="470bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470bd-102">SYNOPSIS</span></span>
<span data-ttu-id="470bd-103">Frissítse a fürt egyik csomóponttípusának 10.10-es szintjéhez vagy VmSku-jának frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="470bd-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="470bd-104">Emellett frissíti a service fabric VM-bővítményben lévő tárolási réteget is a társított virtuálisgép-méretkészleten.</span><span class="sxs-lookup"><span data-stu-id="470bd-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="470bd-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="470bd-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="470bd-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="470bd-106">DESCRIPTION</span></span>
<span data-ttu-id="470bd-107">Az **Update-AzureRmServiceFabricDurability** segítségével frissítheti a fürt minőségének vagy termékváltozatának frissítését.</span><span class="sxs-lookup"><span data-stu-id="470bd-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="470bd-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="470bd-108">EXAMPLES</span></span>

### <span data-ttu-id="470bd-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="470bd-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="470bd-110">Ez a parancs ezüstre módosítja az "nt1" NodeType-réteget.</span><span class="sxs-lookup"><span data-stu-id="470bd-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="470bd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="470bd-111">PARAMETERS</span></span>

### <span data-ttu-id="470bd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470bd-112">-DefaultProfile</span></span>
<span data-ttu-id="470bd-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="470bd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-114">–10.</span><span class="sxs-lookup"><span data-stu-id="470bd-114">-DurabilityLevel</span></span>
<span data-ttu-id="470bd-115">Adja meg a megőrzési szintet.</span><span class="sxs-lookup"><span data-stu-id="470bd-115">Specify durability level.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="470bd-116">-Name</span></span>
<span data-ttu-id="470bd-117">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="470bd-117">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="470bd-118">-NodeType</span></span>
<span data-ttu-id="470bd-119">Adja meg a Service Fabric csomóponttípus nevét.</span><span class="sxs-lookup"><span data-stu-id="470bd-119">Specify Service Fabric node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="470bd-120">-ResourceGroupName</span></span>
<span data-ttu-id="470bd-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="470bd-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-122">-Termékváltozat</span><span class="sxs-lookup"><span data-stu-id="470bd-122">-Sku</span></span>
<span data-ttu-id="470bd-123">Adja meg a csomóponttípus termékváltozatát.</span><span class="sxs-lookup"><span data-stu-id="470bd-123">Specify the SKU of the node type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="470bd-124">-Confirm</span></span>
<span data-ttu-id="470bd-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="470bd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="470bd-126">-WhatIf</span></span>
<span data-ttu-id="470bd-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="470bd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="470bd-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="470bd-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470bd-129">CommonParameters</span></span>
<span data-ttu-id="470bd-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470bd-131">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470bd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470bd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="470bd-132">INPUTS</span></span>

### <span data-ttu-id="470bd-133">Microsoft.Azure.Commands.ServiceFabric.Models.Fogaraslevel</span><span class="sxs-lookup"><span data-stu-id="470bd-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="470bd-134">System.String</span><span class="sxs-lookup"><span data-stu-id="470bd-134">System.String</span></span>

## <span data-ttu-id="470bd-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="470bd-135">OUTPUTS</span></span>

### <span data-ttu-id="470bd-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span><span class="sxs-lookup"><span data-stu-id="470bd-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="470bd-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="470bd-137">NOTES</span></span>

## <span data-ttu-id="470bd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="470bd-138">RELATED LINKS</span></span>

