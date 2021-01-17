---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345809"
---
# <span data-ttu-id="4484c-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4484c-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="4484c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4484c-102">SYNOPSIS</span></span>
<span data-ttu-id="4484c-103">Csatolt tárfiók be- vagy listába való be- vagy listába</span><span class="sxs-lookup"><span data-stu-id="4484c-103">Get or list linked storage account</span></span>

## <span data-ttu-id="4484c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4484c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4484c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4484c-105">DESCRIPTION</span></span>
<span data-ttu-id="4484c-106">Csatolt tárfiók lekérte, és felsorolja az összes csatolt tárfiókot, ha nincs megadva a "-DataSourceType" érték.</span><span class="sxs-lookup"><span data-stu-id="4484c-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="4484c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4484c-107">EXAMPLES</span></span>

### <span data-ttu-id="4484c-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4484c-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="4484c-109">list linked storage accoounts for workspace {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="4484c-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="4484c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4484c-110">PARAMETERS</span></span>

### <span data-ttu-id="4484c-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="4484c-111">-DataSourceType</span></span>
<span data-ttu-id="4484c-112">Az adatforrás típusa a "CustomLogs" (AzureWatson) egyikének kell lennie.</span><span class="sxs-lookup"><span data-stu-id="4484c-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="4484c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4484c-113">-DefaultProfile</span></span>
<span data-ttu-id="4484c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4484c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4484c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4484c-115">-ResourceGroupName</span></span>
<span data-ttu-id="4484c-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4484c-116">The resource group name.</span></span>

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

### <span data-ttu-id="4484c-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4484c-117">-WorkspaceName</span></span>
<span data-ttu-id="4484c-118">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="4484c-118">The workspace name.</span></span>

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

### <span data-ttu-id="4484c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4484c-119">CommonParameters</span></span>
<span data-ttu-id="4484c-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4484c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4484c-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4484c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4484c-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4484c-122">INPUTS</span></span>

### <span data-ttu-id="4484c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4484c-123">System.String</span></span>

## <span data-ttu-id="4484c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4484c-124">OUTPUTS</span></span>

### <span data-ttu-id="4484c-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="4484c-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="4484c-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4484c-126">NOTES</span></span>

## <span data-ttu-id="4484c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4484c-127">RELATED LINKS</span></span>