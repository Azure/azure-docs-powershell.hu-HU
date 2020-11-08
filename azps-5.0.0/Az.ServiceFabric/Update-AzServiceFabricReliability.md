---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: a63bcfe0f807f36ffae5c10e644322b1fb612325
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185848"
---
# <span data-ttu-id="28144-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="28144-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="28144-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28144-102">SYNOPSIS</span></span>
<span data-ttu-id="28144-103">A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="28144-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="28144-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28144-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28144-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="28144-105">DESCRIPTION</span></span>
<span data-ttu-id="28144-106">**Frissítse a AzServiceFabricReliability** a fürt elsődleges csomópont-típusának megbízhatóságát.</span><span class="sxs-lookup"><span data-stu-id="28144-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="28144-107">Példák</span><span class="sxs-lookup"><span data-stu-id="28144-107">EXAMPLES</span></span>

### <span data-ttu-id="28144-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="28144-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="28144-109">Ez a parancs az elsődleges csomópont típusának megbízhatósági rétegét ezüst értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="28144-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="28144-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28144-110">PARAMETERS</span></span>

### <span data-ttu-id="28144-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="28144-111">-AutoAddNode</span></span>
<span data-ttu-id="28144-112">A csomópontok számának automatikus hozzáadása a megbízhatóság módosításakor</span><span class="sxs-lookup"><span data-stu-id="28144-112">Add node count automatically when changing reliability</span></span>

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

### <span data-ttu-id="28144-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28144-113">-DefaultProfile</span></span>
<span data-ttu-id="28144-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="28144-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28144-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28144-115">-Name</span></span>
<span data-ttu-id="28144-116">A fürt nevének megadása</span><span class="sxs-lookup"><span data-stu-id="28144-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="28144-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="28144-117">-ReliabilityLevel</span></span>
<span data-ttu-id="28144-118">Megbízhatósági szint</span><span class="sxs-lookup"><span data-stu-id="28144-118">Reliability tier</span></span>

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

### <span data-ttu-id="28144-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28144-119">-ResourceGroupName</span></span>
<span data-ttu-id="28144-120">Adja meg az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="28144-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="28144-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28144-121">-Confirm</span></span>
<span data-ttu-id="28144-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28144-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28144-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28144-123">-WhatIf</span></span>
<span data-ttu-id="28144-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28144-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28144-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28144-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28144-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28144-126">CommonParameters</span></span>
<span data-ttu-id="28144-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28144-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28144-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="28144-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28144-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28144-129">INPUTS</span></span>

### <span data-ttu-id="28144-130">System. String</span><span class="sxs-lookup"><span data-stu-id="28144-130">System.String</span></span>

### <span data-ttu-id="28144-131">Microsoft. Azure. Command. ServiceFabric. models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="28144-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="28144-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="28144-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="28144-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28144-133">OUTPUTS</span></span>

### <span data-ttu-id="28144-134">Microsoft. Azure. Command. ServiceFabric. models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="28144-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="28144-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28144-135">NOTES</span></span>

## <span data-ttu-id="28144-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28144-136">RELATED LINKS</span></span>