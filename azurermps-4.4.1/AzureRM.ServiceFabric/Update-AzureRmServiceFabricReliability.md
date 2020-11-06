---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: c8ee3324f7f6e7653d86bef747bdb9831982474e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494661"
---
# <span data-ttu-id="25578-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="25578-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="25578-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="25578-102">SYNOPSIS</span></span>
<span data-ttu-id="25578-103">A fürt elsődleges csomópont-típusának megbízhatósági szintjeinek frissítése</span><span class="sxs-lookup"><span data-stu-id="25578-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25578-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="25578-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25578-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="25578-105">DESCRIPTION</span></span>
<span data-ttu-id="25578-106">**Frissítse a AzureRmServiceFabricReliability** a fürt elsődleges csomópont-típusának megbízhatóságát.</span><span class="sxs-lookup"><span data-stu-id="25578-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="25578-107">Példák</span><span class="sxs-lookup"><span data-stu-id="25578-107">EXAMPLES</span></span>

### <span data-ttu-id="25578-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="25578-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="25578-109">Ez a parancs az elsődleges csomópont típusának megbízhatósági rétegét ezüst értékre módosítja.</span><span class="sxs-lookup"><span data-stu-id="25578-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="25578-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="25578-110">PARAMETERS</span></span>

### <span data-ttu-id="25578-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="25578-111">-AutoAddNode</span></span>
<span data-ttu-id="25578-112">A csomópontok számának automatikus hozzáadása a megbízhatóság módosításakor.</span><span class="sxs-lookup"><span data-stu-id="25578-112">Add node count automatically when changing reliability.</span></span>

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

### <span data-ttu-id="25578-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="25578-113">-Name</span></span>
<span data-ttu-id="25578-114">Adja meg a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="25578-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="25578-115">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="25578-115">-ReliabilityLevel</span></span>
<span data-ttu-id="25578-116">Megbízhatósági szint</span><span class="sxs-lookup"><span data-stu-id="25578-116">Reliability tier.</span></span>

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

### <span data-ttu-id="25578-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25578-117">-ResourceGroupName</span></span>
<span data-ttu-id="25578-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="25578-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="25578-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="25578-119">-Confirm</span></span>
<span data-ttu-id="25578-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="25578-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25578-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25578-121">-WhatIf</span></span>
<span data-ttu-id="25578-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="25578-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25578-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="25578-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25578-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25578-124">-DefaultProfile</span></span>
<span data-ttu-id="25578-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="25578-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25578-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25578-126">CommonParameters</span></span>
<span data-ttu-id="25578-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="25578-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25578-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25578-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25578-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="25578-129">INPUTS</span></span>

### <span data-ttu-id="25578-130">Microsoft. Azure. Command. ServiceFabric. models. ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="25578-130">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="25578-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25578-131">System.Management.Automation.SwitchParameter</span></span>

<span data-ttu-id="25578-132">System. String</span><span class="sxs-lookup"><span data-stu-id="25578-132">System.String</span></span>

## <span data-ttu-id="25578-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="25578-133">OUTPUTS</span></span>

### <span data-ttu-id="25578-134">Microsoft. Azure. Command. ServiceFabric. models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="25578-134">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="25578-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="25578-135">NOTES</span></span>

## <span data-ttu-id="25578-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="25578-136">RELATED LINKS</span></span>

