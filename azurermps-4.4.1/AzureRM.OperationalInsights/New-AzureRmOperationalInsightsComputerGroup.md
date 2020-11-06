---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 8a54a735b41ef537a31f5e3e1ce2789d10e60af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496996"
---
# <span data-ttu-id="055ed-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="055ed-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="055ed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="055ed-102">SYNOPSIS</span></span>
<span data-ttu-id="055ed-103">Számítógép-csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="055ed-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="055ed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="055ed-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="055ed-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="055ed-105">DESCRIPTION</span></span>
<span data-ttu-id="055ed-106">A **New-AzureRmOperationalInsightsComputerGroup** parancsmag egy számítógép-csoportot hoz létre egy erőforrás-csoportban és-helyen.</span><span class="sxs-lookup"><span data-stu-id="055ed-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="055ed-107">Példák</span><span class="sxs-lookup"><span data-stu-id="055ed-107">EXAMPLES</span></span>

## <span data-ttu-id="055ed-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="055ed-108">PARAMETERS</span></span>

### <span data-ttu-id="055ed-109">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="055ed-109">-Category</span></span>
<span data-ttu-id="055ed-110">A számítógép csoport kategóriáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="055ed-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="055ed-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="055ed-111">-DisplayName</span></span>
<span data-ttu-id="055ed-112">A számítógép csoport megjelenítendő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="055ed-112">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="055ed-113">-Force</span><span class="sxs-lookup"><span data-stu-id="055ed-113">-Force</span></span>
<span data-ttu-id="055ed-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="055ed-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="055ed-115">-Query</span><span class="sxs-lookup"><span data-stu-id="055ed-115">-Query</span></span>
<span data-ttu-id="055ed-116">A számítógép csoport lekérdezését adja meg.</span><span class="sxs-lookup"><span data-stu-id="055ed-116">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="055ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="055ed-118">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="055ed-118">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="055ed-119">A parancsmag az erőforráscsoport számítógépcsoport csoportját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="055ed-119">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="055ed-120">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="055ed-120">-SavedSearchId</span></span>
<span data-ttu-id="055ed-121">A számítógép csoportjának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="055ed-121">Specifies the ID of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ed-122">-Verzió</span><span class="sxs-lookup"><span data-stu-id="055ed-122">-Version</span></span>
<span data-ttu-id="055ed-123">A verziót adja meg.</span><span class="sxs-lookup"><span data-stu-id="055ed-123">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ed-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="055ed-124">-WorkspaceName</span></span>
<span data-ttu-id="055ed-125">A munkaterület nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="055ed-125">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055ed-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="055ed-126">-Confirm</span></span>
<span data-ttu-id="055ed-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="055ed-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="055ed-128">-WhatIf</span></span>
<span data-ttu-id="055ed-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="055ed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="055ed-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="055ed-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055ed-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055ed-131">-DefaultProfile</span></span>
<span data-ttu-id="055ed-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="055ed-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="055ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055ed-133">CommonParameters</span></span>
<span data-ttu-id="055ed-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="055ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055ed-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="055ed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055ed-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="055ed-136">INPUTS</span></span>

## <span data-ttu-id="055ed-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="055ed-137">OUTPUTS</span></span>

## <span data-ttu-id="055ed-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="055ed-138">NOTES</span></span>

## <span data-ttu-id="055ed-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="055ed-139">RELATED LINKS</span></span>

