---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466700"
---
# <span data-ttu-id="eb1ea-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="eb1ea-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="eb1ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1ea-103">Munkaterülethez csatolt tárfiók törlése</span><span class="sxs-lookup"><span data-stu-id="eb1ea-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="eb1ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eb1ea-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb1ea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eb1ea-105">DESCRIPTION</span></span>
<span data-ttu-id="eb1ea-106">Munkaterülethez csatolt tárfiók törlése</span><span class="sxs-lookup"><span data-stu-id="eb1ea-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="eb1ea-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eb1ea-107">EXAMPLES</span></span>

### <span data-ttu-id="eb1ea-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="eb1ea-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="eb1ea-109">A(z) {workspace-name} "CustomLogs" típusú csatolt tárfiókjának törlése</span><span class="sxs-lookup"><span data-stu-id="eb1ea-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="eb1ea-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb1ea-110">PARAMETERS</span></span>

### <span data-ttu-id="eb1ea-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="eb1ea-111">-DataSourceType</span></span>
<span data-ttu-id="eb1ea-112">Az adatforrás típusa a "CustomLogs" (AzureWatson) egyikének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="eb1ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1ea-113">-DefaultProfile</span></span>
<span data-ttu-id="eb1ea-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb1ea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eb1ea-115">-Force</span></span>
<span data-ttu-id="eb1ea-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eb1ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb1ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb1ea-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-118">The resource group name.</span></span>

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

### <span data-ttu-id="eb1ea-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eb1ea-119">-WorkspaceName</span></span>
<span data-ttu-id="eb1ea-120">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-120">The workspace name.</span></span>

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

### <span data-ttu-id="eb1ea-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb1ea-121">-Confirm</span></span>
<span data-ttu-id="eb1ea-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb1ea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb1ea-123">-WhatIf</span></span>
<span data-ttu-id="eb1ea-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb1ea-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb1ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1ea-126">CommonParameters</span></span>
<span data-ttu-id="eb1ea-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb1ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1ea-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb1ea-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1ea-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb1ea-129">INPUTS</span></span>

### <span data-ttu-id="eb1ea-130">System.String</span><span class="sxs-lookup"><span data-stu-id="eb1ea-130">System.String</span></span>

## <span data-ttu-id="eb1ea-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb1ea-131">OUTPUTS</span></span>

### <span data-ttu-id="eb1ea-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb1ea-132">System.Boolean</span></span>

## <span data-ttu-id="eb1ea-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eb1ea-133">NOTES</span></span>

## <span data-ttu-id="eb1ea-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb1ea-134">RELATED LINKS</span></span>
