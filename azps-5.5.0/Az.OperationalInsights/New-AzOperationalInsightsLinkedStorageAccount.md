---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154002"
---
# <span data-ttu-id="f9b56-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9b56-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="f9b56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9b56-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b56-103">Csatolt tárfiók létrehozása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="f9b56-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="f9b56-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f9b56-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b56-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f9b56-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b56-106">Csatolt tárfiók létrehozása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="f9b56-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="f9b56-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f9b56-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b56-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f9b56-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="f9b56-109">Csatolt tárterület hozzáadása munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="f9b56-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="f9b56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9b56-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b56-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="f9b56-111">-DataSourceType</span></span>
<span data-ttu-id="f9b56-112">Az adatforrás típusa a "CustomLogs" (AzureWatson) egyikének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f9b56-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="f9b56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b56-113">-DefaultProfile</span></span>
<span data-ttu-id="f9b56-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9b56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b56-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f9b56-115">-Force</span></span>
<span data-ttu-id="f9b56-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f9b56-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f9b56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b56-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9b56-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f9b56-118">The resource group name.</span></span>

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

### <span data-ttu-id="f9b56-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="f9b56-119">-StorageAccountIds</span></span>
<span data-ttu-id="f9b56-120">list of storage account id.</span><span class="sxs-lookup"><span data-stu-id="f9b56-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="f9b56-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f9b56-121">-WorkspaceName</span></span>
<span data-ttu-id="f9b56-122">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="f9b56-122">The workspace name.</span></span>

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

### <span data-ttu-id="f9b56-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9b56-123">-Confirm</span></span>
<span data-ttu-id="f9b56-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f9b56-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b56-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b56-125">-WhatIf</span></span>
<span data-ttu-id="f9b56-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f9b56-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b56-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f9b56-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b56-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b56-128">CommonParameters</span></span>
<span data-ttu-id="f9b56-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b56-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b56-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9b56-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b56-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9b56-131">INPUTS</span></span>

### <span data-ttu-id="f9b56-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f9b56-132">System.String</span></span>

## <span data-ttu-id="f9b56-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9b56-133">OUTPUTS</span></span>

### <span data-ttu-id="f9b56-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="f9b56-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="f9b56-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f9b56-135">NOTES</span></span>

## <span data-ttu-id="f9b56-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9b56-136">RELATED LINKS</span></span>
