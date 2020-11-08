---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187573"
---
# <span data-ttu-id="65dc4-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="65dc4-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="65dc4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="65dc4-103">Munkaterület-szolgáltatás leválasztása</span><span class="sxs-lookup"><span data-stu-id="65dc4-103">Unlink service for workspace</span></span>

## <span data-ttu-id="65dc4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65dc4-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65dc4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="65dc4-106">Munkaterület-szolgáltatás leválasztása</span><span class="sxs-lookup"><span data-stu-id="65dc4-106">Unlink service for workspace</span></span>

## <span data-ttu-id="65dc4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="65dc4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="65dc4-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="65dc4-109">Csatolt szolgáltatás leválasztása a munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="65dc4-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="65dc4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65dc4-110">PARAMETERS</span></span>

### <span data-ttu-id="65dc4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65dc4-111">-AsJob</span></span>
<span data-ttu-id="65dc4-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="65dc4-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65dc4-113">-DefaultProfile</span></span>
<span data-ttu-id="65dc4-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65dc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dc4-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="65dc4-115">-LinkedServiceName</span></span>
<span data-ttu-id="65dc4-116">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="65dc4-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65dc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="65dc4-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="65dc4-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dc4-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65dc4-119">-WorkspaceName</span></span>
<span data-ttu-id="65dc4-120">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="65dc4-120">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dc4-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65dc4-121">-Confirm</span></span>
<span data-ttu-id="65dc4-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65dc4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65dc4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65dc4-123">-WhatIf</span></span>
<span data-ttu-id="65dc4-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65dc4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65dc4-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65dc4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65dc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65dc4-126">CommonParameters</span></span>
<span data-ttu-id="65dc4-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65dc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65dc4-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65dc4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65dc4-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65dc4-129">INPUTS</span></span>

### <span data-ttu-id="65dc4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="65dc4-130">System.String</span></span>

## <span data-ttu-id="65dc4-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65dc4-131">OUTPUTS</span></span>

### <span data-ttu-id="65dc4-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65dc4-132">System.Boolean</span></span>

## <span data-ttu-id="65dc4-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65dc4-133">NOTES</span></span>

## <span data-ttu-id="65dc4-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65dc4-134">RELATED LINKS</span></span>
