---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146474"
---
# <span data-ttu-id="30751-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30751-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="30751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30751-102">SYNOPSIS</span></span>
<span data-ttu-id="30751-103">Csatolt tárfiók be- vagy listába való be- vagy listába</span><span class="sxs-lookup"><span data-stu-id="30751-103">Get or list linked storage account</span></span>

## <span data-ttu-id="30751-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="30751-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30751-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="30751-105">DESCRIPTION</span></span>
<span data-ttu-id="30751-106">Csatolt tárfiók lekérte, és felsorolja az összes csatolt tárfiókot, ha nincs megadva a "-DataSourceType" érték.</span><span class="sxs-lookup"><span data-stu-id="30751-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="30751-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="30751-107">EXAMPLES</span></span>

### <span data-ttu-id="30751-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="30751-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="30751-109">list linked storage accoounts for workspace {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="30751-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="30751-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30751-110">PARAMETERS</span></span>

### <span data-ttu-id="30751-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="30751-111">-DataSourceType</span></span>
<span data-ttu-id="30751-112">Az adatforrás típusa a "CustomLogs" (AzureWatson) egyikének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="30751-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="30751-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30751-113">-DefaultProfile</span></span>
<span data-ttu-id="30751-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="30751-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30751-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30751-115">-ResourceGroupName</span></span>
<span data-ttu-id="30751-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="30751-116">The resource group name.</span></span>

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

### <span data-ttu-id="30751-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="30751-117">-WorkspaceName</span></span>
<span data-ttu-id="30751-118">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="30751-118">The workspace name.</span></span>

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

### <span data-ttu-id="30751-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30751-119">CommonParameters</span></span>
<span data-ttu-id="30751-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30751-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30751-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30751-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30751-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30751-122">INPUTS</span></span>

### <span data-ttu-id="30751-123">System.String</span><span class="sxs-lookup"><span data-stu-id="30751-123">System.String</span></span>

## <span data-ttu-id="30751-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30751-124">OUTPUTS</span></span>

### <span data-ttu-id="30751-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="30751-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="30751-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="30751-126">NOTES</span></span>

## <span data-ttu-id="30751-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30751-127">RELATED LINKS</span></span>