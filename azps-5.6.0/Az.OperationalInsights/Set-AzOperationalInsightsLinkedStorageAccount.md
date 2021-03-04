---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1392e77ef6497265dde8bcf0a05a86529253f539
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937858"
---
# <span data-ttu-id="6eb08-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6eb08-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="6eb08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb08-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb08-103">Csatolt tárfiók beállítása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="6eb08-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="6eb08-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6eb08-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eb08-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6eb08-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb08-106">Csatolt tárfiók beállítása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="6eb08-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="6eb08-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6eb08-107">EXAMPLES</span></span>

### <span data-ttu-id="6eb08-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6eb08-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="6eb08-109">Csatolt tárterület beállítása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="6eb08-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="6eb08-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eb08-110">PARAMETERS</span></span>

### <span data-ttu-id="6eb08-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="6eb08-111">-DataSourceType</span></span>
<span data-ttu-id="6eb08-112">Az adatforrás típusa a "CustomLogs" (AzureWatson) egyikének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="6eb08-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb08-113">-DefaultProfile</span></span>
<span data-ttu-id="6eb08-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6eb08-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb08-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6eb08-115">-Force</span></span>
<span data-ttu-id="6eb08-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6eb08-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6eb08-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb08-117">-ResourceGroupName</span></span>
<span data-ttu-id="6eb08-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6eb08-118">The resource group name.</span></span>

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

### <span data-ttu-id="6eb08-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="6eb08-119">-StorageAccountIds</span></span>
<span data-ttu-id="6eb08-120">list of storage account id.</span><span class="sxs-lookup"><span data-stu-id="6eb08-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb08-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6eb08-121">-WorkspaceName</span></span>
<span data-ttu-id="6eb08-122">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6eb08-122">The workspace name.</span></span>

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

### <span data-ttu-id="6eb08-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eb08-123">-Confirm</span></span>
<span data-ttu-id="6eb08-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6eb08-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb08-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb08-125">-WhatIf</span></span>
<span data-ttu-id="6eb08-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6eb08-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eb08-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6eb08-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb08-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb08-128">CommonParameters</span></span>
<span data-ttu-id="6eb08-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eb08-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb08-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6eb08-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb08-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6eb08-131">INPUTS</span></span>

### <span data-ttu-id="6eb08-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6eb08-132">System.String</span></span>

## <span data-ttu-id="6eb08-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eb08-133">OUTPUTS</span></span>

### <span data-ttu-id="6eb08-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="6eb08-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="6eb08-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6eb08-135">NOTES</span></span>

## <span data-ttu-id="6eb08-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6eb08-136">RELATED LINKS</span></span>
