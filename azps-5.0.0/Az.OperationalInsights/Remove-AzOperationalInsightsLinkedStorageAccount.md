---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188079"
---
# <span data-ttu-id="4507a-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4507a-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="4507a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4507a-102">SYNOPSIS</span></span>
<span data-ttu-id="4507a-103">A munkaterülethez kapcsolt tárolási fiók törlése</span><span class="sxs-lookup"><span data-stu-id="4507a-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="4507a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4507a-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4507a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4507a-105">DESCRIPTION</span></span>
<span data-ttu-id="4507a-106">A munkaterülethez kapcsolt tárolási fiók törlése</span><span class="sxs-lookup"><span data-stu-id="4507a-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="4507a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4507a-107">EXAMPLES</span></span>

### <span data-ttu-id="4507a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4507a-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="4507a-109">A "CustomLogs" ({munkaterület-Name}) típussal rendelkező kapcsolt tárolási fiók törlése</span><span class="sxs-lookup"><span data-stu-id="4507a-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="4507a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4507a-110">PARAMETERS</span></span>

### <span data-ttu-id="4507a-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="4507a-111">-DataSourceType</span></span>
<span data-ttu-id="4507a-112">Az adatforrás típusa csak "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="4507a-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4507a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4507a-113">-DefaultProfile</span></span>
<span data-ttu-id="4507a-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4507a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4507a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4507a-115">-Force</span></span>
<span data-ttu-id="4507a-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4507a-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4507a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4507a-117">-ResourceGroupName</span></span>
<span data-ttu-id="4507a-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4507a-118">The resource group name.</span></span>

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

### <span data-ttu-id="4507a-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4507a-119">-WorkspaceName</span></span>
<span data-ttu-id="4507a-120">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="4507a-120">The workspace name.</span></span>

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

### <span data-ttu-id="4507a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4507a-121">-Confirm</span></span>
<span data-ttu-id="4507a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4507a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4507a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4507a-123">-WhatIf</span></span>
<span data-ttu-id="4507a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4507a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4507a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4507a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4507a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4507a-126">CommonParameters</span></span>
<span data-ttu-id="4507a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4507a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4507a-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4507a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4507a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4507a-129">INPUTS</span></span>

### <span data-ttu-id="4507a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4507a-130">System.String</span></span>

## <span data-ttu-id="4507a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4507a-131">OUTPUTS</span></span>

### <span data-ttu-id="4507a-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4507a-132">System.Boolean</span></span>

## <span data-ttu-id="4507a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4507a-133">NOTES</span></span>

## <span data-ttu-id="4507a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4507a-134">RELATED LINKS</span></span>
