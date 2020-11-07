---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: aca27be11fde78df8abad1d7cdcfeff4232b60d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679325"
---
# <span data-ttu-id="96800-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="96800-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="96800-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96800-102">SYNOPSIS</span></span>
<span data-ttu-id="96800-103">Csomópontok hozzáadása a fürt adott csomópont-típusához</span><span class="sxs-lookup"><span data-stu-id="96800-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96800-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96800-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToAdd <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96800-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96800-105">DESCRIPTION</span></span>
<span data-ttu-id="96800-106">A **Add-AzureRmServiceFabricNode** segítségével csomópontokat adhat hozzá az adott csomópont-típushoz.</span><span class="sxs-lookup"><span data-stu-id="96800-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="96800-107">Csak meg kell adnia a csomópont típusához hozzáadni kívánt csomópontok számát.</span><span class="sxs-lookup"><span data-stu-id="96800-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="96800-108">Példák</span><span class="sxs-lookup"><span data-stu-id="96800-108">EXAMPLES</span></span>

### <span data-ttu-id="96800-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="96800-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="96800-110">Ez a parancs 2 csomópontot ad hozzá az "N1" csomópont típushoz.</span><span class="sxs-lookup"><span data-stu-id="96800-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="96800-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96800-111">PARAMETERS</span></span>

### <span data-ttu-id="96800-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="96800-112">-Name</span></span>
<span data-ttu-id="96800-113">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="96800-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="96800-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="96800-114">-NodeType</span></span>
<span data-ttu-id="96800-115">Csomópont típusa név.</span><span class="sxs-lookup"><span data-stu-id="96800-115">Node type name.</span></span>

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

### <span data-ttu-id="96800-116">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="96800-116">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="96800-117">VM-példány száma</span><span class="sxs-lookup"><span data-stu-id="96800-117">VM instance number.</span></span>

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

### <span data-ttu-id="96800-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96800-118">-ResourceGroupName</span></span>
<span data-ttu-id="96800-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96800-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="96800-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="96800-120">-Confirm</span></span>
<span data-ttu-id="96800-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96800-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96800-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96800-122">-WhatIf</span></span>
<span data-ttu-id="96800-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="96800-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96800-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96800-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96800-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96800-125">-DefaultProfile</span></span>
<span data-ttu-id="96800-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96800-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96800-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96800-127">CommonParameters</span></span>
<span data-ttu-id="96800-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96800-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96800-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96800-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96800-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96800-130">INPUTS</span></span>

### <span data-ttu-id="96800-131">System. String</span><span class="sxs-lookup"><span data-stu-id="96800-131">System.String</span></span>

## <span data-ttu-id="96800-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96800-132">OUTPUTS</span></span>

### <span data-ttu-id="96800-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="96800-133">System.Object</span></span>

## <span data-ttu-id="96800-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96800-134">NOTES</span></span>

## <span data-ttu-id="96800-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96800-135">RELATED LINKS</span></span>

[<span data-ttu-id="96800-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="96800-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
