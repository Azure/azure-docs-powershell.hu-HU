---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: a94d879573be2d640269510283e341cbad8aa052
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011168"
---
# <span data-ttu-id="e8ce3-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="e8ce3-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="e8ce3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e8ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ce3-103">Információkat kap a fogyasztói megosztási előfizetésekről a szolgáltató oldalán.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="e8ce3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e8ce3-104">SYNTAX</span></span>

### <span data-ttu-id="e8ce3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e8ce3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ce3-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ce3-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ce3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e8ce3-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ce3-108">A **Get-AzDataShareProviderSubscription** parancsmag információkat kap a fogyasztói megosztási előfizetésekről a szolgáltató oldalán.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="e8ce3-109">Ha a megosztás subscrption azonosítót adja meg, ez a parancsmag információkat kap a megosztási előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="e8ce3-110">Ha nem adja meg a megosztási előfizetés azonosítóját, ez a parancsmag információkat kap a megosztáshoz társított összes ügyfél-megosztási előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="e8ce3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="e8ce3-111">EXAMPLES</span></span>

### <span data-ttu-id="e8ce3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e8ce3-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="e8ce3-113">Ez a parancs információkat nyújt a megosztási AdsShare az adatmegosztási fiók-WikiAds társított fogyasztói megosztási előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="e8ce3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e8ce3-114">PARAMETERS</span></span>

### <span data-ttu-id="e8ce3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8ce3-115">-AccountName</span></span>
<span data-ttu-id="e8ce3-116">Azure DataShare-fiók neve</span><span class="sxs-lookup"><span data-stu-id="e8ce3-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="e8ce3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ce3-117">-DefaultProfile</span></span>
<span data-ttu-id="e8ce3-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ce3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ce3-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8ce3-120">Az Azure DataShare-fiók erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="e8ce3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8ce3-121">-ResourceId</span></span>
<span data-ttu-id="e8ce3-122">A megosztás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="e8ce3-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ce3-123">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="e8ce3-123">-ShareName</span></span>
<span data-ttu-id="e8ce3-124">Azure DataShare név.</span><span class="sxs-lookup"><span data-stu-id="e8ce3-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="e8ce3-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e8ce3-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="e8ce3-126">A fogyasztói megosztásra szóló előfizetés azonosítója</span><span class="sxs-lookup"><span data-stu-id="e8ce3-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ce3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ce3-127">CommonParameters</span></span>
<span data-ttu-id="e8ce3-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e8ce3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ce3-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ce3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ce3-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ce3-130">INPUTS</span></span>

### <span data-ttu-id="e8ce3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ce3-131">System.String</span></span>

## <span data-ttu-id="e8ce3-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e8ce3-132">OUTPUTS</span></span>

### <span data-ttu-id="e8ce3-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="e8ce3-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="e8ce3-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e8ce3-134">NOTES</span></span>

## <span data-ttu-id="e8ce3-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e8ce3-135">RELATED LINKS</span></span>
