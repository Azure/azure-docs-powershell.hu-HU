---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167771"
---
# <span data-ttu-id="fd416-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="fd416-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="fd416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd416-102">SYNOPSIS</span></span>
<span data-ttu-id="fd416-103">Információkat kap egy eseményindítóról a megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="fd416-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="fd416-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fd416-104">SYNTAX</span></span>

### <span data-ttu-id="fd416-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd416-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd416-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd416-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd416-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fd416-107">DESCRIPTION</span></span>
<span data-ttu-id="fd416-108">A **Get-AzDataShareTrigger** parancsmag információkat kap az adatmegosztási fiókon keresztüli megosztási előfizetés eseményindítóiról.</span><span class="sxs-lookup"><span data-stu-id="fd416-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="fd416-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fd416-109">EXAMPLES</span></span>

### <span data-ttu-id="fd416-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="fd416-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="fd416-111">Ez a parancs információkat kap az AdsTrigger eseményindítóról az előfizetés megosztásához szükséges AdsShareSubscription eseményről az adatmegosztási fiók WikiAds lapja alatt.</span><span class="sxs-lookup"><span data-stu-id="fd416-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="fd416-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd416-112">PARAMETERS</span></span>

### <span data-ttu-id="fd416-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd416-113">-AccountName</span></span>
<span data-ttu-id="fd416-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="fd416-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd416-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd416-115">-DefaultProfile</span></span>
<span data-ttu-id="fd416-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fd416-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd416-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fd416-117">-Name</span></span>
<span data-ttu-id="fd416-118">Azure data share trigger name</span><span class="sxs-lookup"><span data-stu-id="fd416-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd416-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd416-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd416-120">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="fd416-120">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd416-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd416-121">-ResourceId</span></span>
<span data-ttu-id="fd416-122">Az eseményindító erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="fd416-122">The resource id of the trigger</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd416-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="fd416-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="fd416-124">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="fd416-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd416-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd416-125">CommonParameters</span></span>
<span data-ttu-id="fd416-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd416-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd416-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd416-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd416-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd416-128">INPUTS</span></span>

### <span data-ttu-id="fd416-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fd416-129">System.String</span></span>

## <span data-ttu-id="fd416-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd416-130">OUTPUTS</span></span>

### <span data-ttu-id="fd416-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="fd416-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="fd416-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fd416-132">NOTES</span></span>

## <span data-ttu-id="fd416-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd416-133">RELATED LINKS</span></span>
