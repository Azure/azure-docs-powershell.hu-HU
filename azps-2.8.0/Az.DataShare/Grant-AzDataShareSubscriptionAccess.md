---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: befe472f3340ae41e669ffa584e500051a7728d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666720"
---
# <span data-ttu-id="ae5c1-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="ae5c1-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="ae5c1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5c1-103">Visszavont megosztási előfizetéshez való hozzáférés támogatása a forrás megosztásához</span><span class="sxs-lookup"><span data-stu-id="ae5c1-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="ae5c1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae5c1-104">SYNTAX</span></span>

### <span data-ttu-id="ae5c1-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae5c1-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae5c1-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae5c1-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae5c1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae5c1-107">DESCRIPTION</span></span>
<span data-ttu-id="ae5c1-108">A **Grant-AzDataShareSubscriptionAccess** parancsmag előfizetéses hozzáféréssel ruházza fel a források megosztását</span><span class="sxs-lookup"><span data-stu-id="ae5c1-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="ae5c1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae5c1-109">EXAMPLES</span></span>

### <span data-ttu-id="ae5c1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ae5c1-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="ae5c1-111">Hozzáférést biztosít az azonosító 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 által azonosított előfizetés megosztásához</span><span class="sxs-lookup"><span data-stu-id="ae5c1-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="ae5c1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae5c1-112">PARAMETERS</span></span>

### <span data-ttu-id="ae5c1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ae5c1-113">-AccountName</span></span>
<span data-ttu-id="ae5c1-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="ae5c1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="ae5c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5c1-115">-DefaultProfile</span></span>
<span data-ttu-id="ae5c1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae5c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae5c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae5c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae5c1-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="ae5c1-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ae5c1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae5c1-119">-ResourceId</span></span>
<span data-ttu-id="ae5c1-120">Az Azure-adatmegosztás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="ae5c1-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="ae5c1-121">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="ae5c1-121">-ShareName</span></span>
<span data-ttu-id="ae5c1-122">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="ae5c1-122">Azure data share name</span></span>

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

### <span data-ttu-id="ae5c1-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae5c1-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="ae5c1-124">A szolgáltató megosztási előfizetésének megosztása</span><span class="sxs-lookup"><span data-stu-id="ae5c1-124">The share subscription id of the provider share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5c1-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae5c1-125">-Confirm</span></span>
<span data-ttu-id="ae5c1-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae5c1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5c1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5c1-127">-WhatIf</span></span>
<span data-ttu-id="ae5c1-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae5c1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae5c1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae5c1-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5c1-130">CommonParameters</span></span>
<span data-ttu-id="ae5c1-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae5c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5c1-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5c1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5c1-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae5c1-133">INPUTS</span></span>

### <span data-ttu-id="ae5c1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ae5c1-134">System.String</span></span>

## <span data-ttu-id="ae5c1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae5c1-135">OUTPUTS</span></span>

### <span data-ttu-id="ae5c1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="ae5c1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="ae5c1-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae5c1-137">NOTES</span></span>

## <span data-ttu-id="ae5c1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae5c1-138">RELATED LINKS</span></span>
