---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186880"
---
# <span data-ttu-id="4ecbf-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ecbf-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="4ecbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ecbf-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecbf-103">A munkaterülethez kapcsolt tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="4ecbf-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="4ecbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ecbf-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ecbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ecbf-105">DESCRIPTION</span></span>
<span data-ttu-id="4ecbf-106">A munkaterülethez kapcsolt tárolási fiók beállítása</span><span class="sxs-lookup"><span data-stu-id="4ecbf-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="4ecbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4ecbf-107">EXAMPLES</span></span>

### <span data-ttu-id="4ecbf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4ecbf-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="4ecbf-109">A munkaterület kapcsolt tárterületének beállítása</span><span class="sxs-lookup"><span data-stu-id="4ecbf-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="4ecbf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ecbf-110">PARAMETERS</span></span>

### <span data-ttu-id="4ecbf-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="4ecbf-111">-DataSourceType</span></span>
<span data-ttu-id="4ecbf-112">Az adatforrás típusa csak "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="4ecbf-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="4ecbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecbf-113">-DefaultProfile</span></span>
<span data-ttu-id="4ecbf-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ecbf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4ecbf-115">-Force</span></span>
<span data-ttu-id="4ecbf-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4ecbf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ecbf-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ecbf-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-118">The resource group name.</span></span>

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

### <span data-ttu-id="4ecbf-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="4ecbf-119">-StorageAccountIds</span></span>
<span data-ttu-id="4ecbf-120">a tárolási fiók azonosítójának listája.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="4ecbf-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ecbf-121">-WorkspaceName</span></span>
<span data-ttu-id="4ecbf-122">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-122">The workspace name.</span></span>

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

### <span data-ttu-id="4ecbf-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4ecbf-123">-Confirm</span></span>
<span data-ttu-id="4ecbf-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ecbf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ecbf-125">-WhatIf</span></span>
<span data-ttu-id="4ecbf-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ecbf-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ecbf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecbf-128">CommonParameters</span></span>
<span data-ttu-id="4ecbf-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ecbf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecbf-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ecbf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecbf-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ecbf-131">INPUTS</span></span>

### <span data-ttu-id="4ecbf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4ecbf-132">System.String</span></span>

## <span data-ttu-id="4ecbf-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ecbf-133">OUTPUTS</span></span>

### <span data-ttu-id="4ecbf-134">Microsoft. Azure. Command. OperationalInsights. models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="4ecbf-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="4ecbf-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ecbf-135">NOTES</span></span>

## <span data-ttu-id="4ecbf-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ecbf-136">RELATED LINKS</span></span>
