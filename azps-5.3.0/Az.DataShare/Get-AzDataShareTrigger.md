---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377340"
---
# <span data-ttu-id="acff0-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="acff0-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="acff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acff0-102">SYNOPSIS</span></span>
<span data-ttu-id="acff0-103">Információkat kap egy eseményindítóról a megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="acff0-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="acff0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="acff0-104">SYNTAX</span></span>

### <span data-ttu-id="acff0-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="acff0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acff0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acff0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acff0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="acff0-107">DESCRIPTION</span></span>
<span data-ttu-id="acff0-108">A **Get-AzDataShareTrigger** parancsmag információkat kap az adatmegosztási fiókon keresztüli megosztási előfizetés eseményindítóiról.</span><span class="sxs-lookup"><span data-stu-id="acff0-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="acff0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="acff0-109">EXAMPLES</span></span>

### <span data-ttu-id="acff0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="acff0-110">Example 1</span></span>
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

<span data-ttu-id="acff0-111">Ez a parancs információkat kap az AdsTrigger eseményindítóról a share-előfizetéshez elérhető AdsShareSubscription eseményről az adatmegosztási fiók WikiAds lapja alatt.</span><span class="sxs-lookup"><span data-stu-id="acff0-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="acff0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acff0-112">PARAMETERS</span></span>

### <span data-ttu-id="acff0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="acff0-113">-AccountName</span></span>
<span data-ttu-id="acff0-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="acff0-114">Azure data share account name</span></span>

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

### <span data-ttu-id="acff0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acff0-115">-DefaultProfile</span></span>
<span data-ttu-id="acff0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="acff0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acff0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="acff0-117">-Name</span></span>
<span data-ttu-id="acff0-118">Azure data share trigger name</span><span class="sxs-lookup"><span data-stu-id="acff0-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="acff0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acff0-119">-ResourceGroupName</span></span>
<span data-ttu-id="acff0-120">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="acff0-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="acff0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acff0-121">-ResourceId</span></span>
<span data-ttu-id="acff0-122">Az eseményindító erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="acff0-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="acff0-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="acff0-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="acff0-124">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="acff0-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="acff0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acff0-125">CommonParameters</span></span>
<span data-ttu-id="acff0-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acff0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acff0-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acff0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acff0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acff0-128">INPUTS</span></span>

### <span data-ttu-id="acff0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="acff0-129">System.String</span></span>

## <span data-ttu-id="acff0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="acff0-130">OUTPUTS</span></span>

### <span data-ttu-id="acff0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="acff0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="acff0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="acff0-132">NOTES</span></span>

## <span data-ttu-id="acff0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="acff0-133">RELATED LINKS</span></span>
