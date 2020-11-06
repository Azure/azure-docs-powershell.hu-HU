---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: 15dfc29703e2d331920a1751bcd6671e77d84171
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497292"
---
# <span data-ttu-id="f7f1c-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f7f1c-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="f7f1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f1c-103">A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="f7f1c-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7f1c-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f1c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7f1c-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f1c-106">**Frissítse a AzureRmServiceFabricReliability** a fürt elsődleges csomópont-típusának megbízhatóságát.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="f7f1c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f7f1c-107">EXAMPLES</span></span>

### <span data-ttu-id="f7f1c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7f1c-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="f7f1c-109">Ez a parancs az elsődleges csomópont típusának megbízhatósági rétegét ezüst értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="f7f1c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7f1c-110">PARAMETERS</span></span>

### <span data-ttu-id="f7f1c-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="f7f1c-111">-AutoAddNode</span></span>
<span data-ttu-id="f7f1c-112">A csomópontok számának automatikus hozzáadása a megbízhatóság módosításakor.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-112">Add node count automatically when changing reliability.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f1c-113">-DefaultProfile</span></span>
<span data-ttu-id="f7f1c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f1c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7f1c-115">-Name</span></span>
<span data-ttu-id="f7f1c-116">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="f7f1c-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="f7f1c-117">-ReliabilityLevel</span></span>
<span data-ttu-id="f7f1c-118">Megbízhatósági szint</span><span class="sxs-lookup"><span data-stu-id="f7f1c-118">Reliability tier.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f1c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f1c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7f1c-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7f1c-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f7f1c-121">-Confirm</span></span>
<span data-ttu-id="f7f1c-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f1c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f1c-123">-WhatIf</span></span>
<span data-ttu-id="f7f1c-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7f1c-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f1c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f1c-126">CommonParameters</span></span>
<span data-ttu-id="f7f1c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7f1c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f1c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f1c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f1c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7f1c-129">INPUTS</span></span>

### <span data-ttu-id="f7f1c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f7f1c-130">System.String</span></span>

### <span data-ttu-id="f7f1c-131">Microsoft. Azure. Command. ServiceFabric. models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="f7f1c-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="f7f1c-132">Paraméterek: ReliabilityLevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7f1c-132">Parameters: ReliabilityLevel (ByValue)</span></span>

### <span data-ttu-id="f7f1c-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f7f1c-133">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="f7f1c-134">Paraméterek: AutoAddNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7f1c-134">Parameters: AutoAddNode (ByValue)</span></span>

## <span data-ttu-id="f7f1c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7f1c-135">OUTPUTS</span></span>

### <span data-ttu-id="f7f1c-136">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="f7f1c-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="f7f1c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7f1c-137">NOTES</span></span>

## <span data-ttu-id="f7f1c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7f1c-138">RELATED LINKS</span></span>
