---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: af8f5d38777674d761b8b55c649b048c933f2c66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495252"
---
# <span data-ttu-id="49f98-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="49f98-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="49f98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="49f98-102">SYNOPSIS</span></span>
<span data-ttu-id="49f98-103">Csomópontok hozzáadása a fürt adott csomópont-típusához</span><span class="sxs-lookup"><span data-stu-id="49f98-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49f98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="49f98-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49f98-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="49f98-105">DESCRIPTION</span></span>
<span data-ttu-id="49f98-106">A **Add-AzureRmServiceFabricNode** segítségével csomópontokat adhat hozzá az adott csomópont-típushoz.</span><span class="sxs-lookup"><span data-stu-id="49f98-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="49f98-107">Csak meg kell adnia a csomópont típusához hozzáadni kívánt csomópontok számát.</span><span class="sxs-lookup"><span data-stu-id="49f98-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="49f98-108">Példák</span><span class="sxs-lookup"><span data-stu-id="49f98-108">EXAMPLES</span></span>

### <span data-ttu-id="49f98-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="49f98-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="49f98-110">Ez a parancs 2 csomópontot ad hozzá az "N1" csomópont típushoz.</span><span class="sxs-lookup"><span data-stu-id="49f98-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="49f98-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="49f98-111">PARAMETERS</span></span>

### <span data-ttu-id="49f98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f98-112">-DefaultProfile</span></span>
<span data-ttu-id="49f98-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49f98-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49f98-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="49f98-114">-Name</span></span>
<span data-ttu-id="49f98-115">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="49f98-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="49f98-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="49f98-116">-NodeType</span></span>
<span data-ttu-id="49f98-117">Csomópont típusa név.</span><span class="sxs-lookup"><span data-stu-id="49f98-117">Node type name.</span></span>

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

### <span data-ttu-id="49f98-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="49f98-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="49f98-119">VM-példány száma</span><span class="sxs-lookup"><span data-stu-id="49f98-119">VM instance number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49f98-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49f98-120">-ResourceGroupName</span></span>
<span data-ttu-id="49f98-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49f98-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="49f98-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="49f98-122">-Confirm</span></span>
<span data-ttu-id="49f98-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="49f98-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49f98-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49f98-124">-WhatIf</span></span>
<span data-ttu-id="49f98-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="49f98-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49f98-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="49f98-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49f98-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f98-127">CommonParameters</span></span>
<span data-ttu-id="49f98-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="49f98-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f98-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49f98-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f98-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="49f98-130">INPUTS</span></span>

### <span data-ttu-id="49f98-131">System. String</span><span class="sxs-lookup"><span data-stu-id="49f98-131">System.String</span></span>

## <span data-ttu-id="49f98-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49f98-132">OUTPUTS</span></span>

### <span data-ttu-id="49f98-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="49f98-133">System.Object</span></span>

## <span data-ttu-id="49f98-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="49f98-134">NOTES</span></span>

## <span data-ttu-id="49f98-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49f98-135">RELATED LINKS</span></span>

[<span data-ttu-id="49f98-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="49f98-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
