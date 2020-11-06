---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 15138ee817cddb992f5b6bbe0beccee10620ffdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497000"
---
# <span data-ttu-id="0a18b-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="0a18b-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="0a18b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a18b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a18b-103">Az Azure-tevékenység naplójának gyűjtése az adott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="0a18b-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a18b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a18b-104">SYNTAX</span></span>

### <span data-ttu-id="0a18b-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a18b-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a18b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0a18b-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a18b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a18b-107">DESCRIPTION</span></span>
<span data-ttu-id="0a18b-108">A New-AzureRmOperationalInsightsAzureActivityLogDataSource a log Analytics segítségével begyűjtheti az Azure Activity naplót az adott előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="0a18b-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="0a18b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0a18b-109">EXAMPLES</span></span>

### <span data-ttu-id="0a18b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0a18b-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0a18b-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="0a18b-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="0a18b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a18b-112">PARAMETERS</span></span>

### <span data-ttu-id="0a18b-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="0a18b-113">-BackfillStartTime</span></span>
<span data-ttu-id="0a18b-114">Választhat, hogy egy héttel ezelőtt backfill a naplókat.</span><span class="sxs-lookup"><span data-stu-id="0a18b-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a18b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0a18b-115">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a18b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a18b-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a18b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a18b-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a18b-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a18b-118">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a18b-119">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="0a18b-119">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a18b-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a18b-120">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a18b-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0a18b-121">-Confirm</span></span>
<span data-ttu-id="0a18b-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0a18b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a18b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a18b-123">-WhatIf</span></span>
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

### <span data-ttu-id="0a18b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a18b-124">-DefaultProfile</span></span>
<span data-ttu-id="0a18b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a18b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a18b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a18b-126">CommonParameters</span></span>
<span data-ttu-id="0a18b-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a18b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a18b-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a18b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a18b-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a18b-129">INPUTS</span></span>

### <span data-ttu-id="0a18b-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a18b-130">PSWorkspace</span></span>
<span data-ttu-id="0a18b-131">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0a18b-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0a18b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a18b-132">OUTPUTS</span></span>

### <span data-ttu-id="0a18b-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0a18b-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0a18b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a18b-134">NOTES</span></span>

## <span data-ttu-id="0a18b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a18b-135">RELATED LINKS</span></span>

