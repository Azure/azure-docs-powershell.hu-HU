---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025388"
---
# <span data-ttu-id="1af2b-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="1af2b-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="1af2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1af2b-102">SYNOPSIS</span></span>
<span data-ttu-id="1af2b-103">Megtudhatja, hogyan kaphat információt a megosztási előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="1af2b-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="1af2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1af2b-104">SYNTAX</span></span>

### <span data-ttu-id="1af2b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1af2b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1af2b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1af2b-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1af2b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1af2b-107">DESCRIPTION</span></span>
<span data-ttu-id="1af2b-108">A **Get-AzDataShareTrigger** parancsmag információkat kaphat az adatmegosztási fiókból az aktiválásról.</span><span class="sxs-lookup"><span data-stu-id="1af2b-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="1af2b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1af2b-109">EXAMPLES</span></span>

### <span data-ttu-id="1af2b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1af2b-110">Example 1</span></span>
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

<span data-ttu-id="1af2b-111">Ez a parancs információt kap az AdsTrigger-előfizetés megosztási AdsShareSubscription az adatmegosztási fiók WikiAds csoportban.</span><span class="sxs-lookup"><span data-stu-id="1af2b-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="1af2b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1af2b-112">PARAMETERS</span></span>

### <span data-ttu-id="1af2b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1af2b-113">-AccountName</span></span>
<span data-ttu-id="1af2b-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="1af2b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="1af2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1af2b-115">-DefaultProfile</span></span>
<span data-ttu-id="1af2b-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1af2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1af2b-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1af2b-117">-Name</span></span>
<span data-ttu-id="1af2b-118">Azure Data Share – trigger neve</span><span class="sxs-lookup"><span data-stu-id="1af2b-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="1af2b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1af2b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1af2b-120">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="1af2b-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1af2b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1af2b-121">-ResourceId</span></span>
<span data-ttu-id="1af2b-122">Az indító erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="1af2b-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="1af2b-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1af2b-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="1af2b-124">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="1af2b-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="1af2b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1af2b-125">CommonParameters</span></span>
<span data-ttu-id="1af2b-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1af2b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1af2b-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1af2b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1af2b-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1af2b-128">INPUTS</span></span>

### <span data-ttu-id="1af2b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1af2b-129">System.String</span></span>

## <span data-ttu-id="1af2b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1af2b-130">OUTPUTS</span></span>

### <span data-ttu-id="1af2b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="1af2b-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="1af2b-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1af2b-132">NOTES</span></span>

## <span data-ttu-id="1af2b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1af2b-133">RELATED LINKS</span></span>
