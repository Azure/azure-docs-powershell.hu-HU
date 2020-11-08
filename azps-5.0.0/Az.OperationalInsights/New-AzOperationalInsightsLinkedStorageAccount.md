---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188081"
---
# <span data-ttu-id="5744d-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5744d-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5744d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5744d-102">SYNOPSIS</span></span>
<span data-ttu-id="5744d-103">Kapcsolt tárolási fiók létrehozása a munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="5744d-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="5744d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5744d-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5744d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5744d-105">DESCRIPTION</span></span>
<span data-ttu-id="5744d-106">Kapcsolt tárolási fiók létrehozása a munkaterülethez</span><span class="sxs-lookup"><span data-stu-id="5744d-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="5744d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5744d-107">EXAMPLES</span></span>

### <span data-ttu-id="5744d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5744d-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="5744d-109">Kapcsolt tárterület felvétele a munkaterületre</span><span class="sxs-lookup"><span data-stu-id="5744d-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="5744d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5744d-110">PARAMETERS</span></span>

### <span data-ttu-id="5744d-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="5744d-111">-DataSourceType</span></span>
<span data-ttu-id="5744d-112">Az adatforrás típusa csak "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="5744d-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="5744d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5744d-113">-DefaultProfile</span></span>
<span data-ttu-id="5744d-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5744d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5744d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5744d-115">-Force</span></span>
<span data-ttu-id="5744d-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5744d-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5744d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5744d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5744d-118">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="5744d-118">The resource group name.</span></span>

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

### <span data-ttu-id="5744d-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="5744d-119">-StorageAccountIds</span></span>
<span data-ttu-id="5744d-120">a tárolási fiók azonosítójának listája.</span><span class="sxs-lookup"><span data-stu-id="5744d-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="5744d-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5744d-121">-WorkspaceName</span></span>
<span data-ttu-id="5744d-122">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="5744d-122">The workspace name.</span></span>

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

### <span data-ttu-id="5744d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5744d-123">-Confirm</span></span>
<span data-ttu-id="5744d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5744d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5744d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5744d-125">-WhatIf</span></span>
<span data-ttu-id="5744d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5744d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5744d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5744d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5744d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5744d-128">CommonParameters</span></span>
<span data-ttu-id="5744d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5744d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5744d-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5744d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5744d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5744d-131">INPUTS</span></span>

### <span data-ttu-id="5744d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5744d-132">System.String</span></span>

## <span data-ttu-id="5744d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5744d-133">OUTPUTS</span></span>

### <span data-ttu-id="5744d-134">Microsoft. Azure. Command. OperationalInsights. models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="5744d-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="5744d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5744d-135">NOTES</span></span>

## <span data-ttu-id="5744d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5744d-136">RELATED LINKS</span></span>
