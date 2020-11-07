---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 93e0aa57a418af038a397559959b40500ad58af3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666682"
---
# <span data-ttu-id="f30df-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="f30df-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="f30df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f30df-102">SYNOPSIS</span></span>
<span data-ttu-id="f30df-103">Az előfizetések megosztásának visszavonása hozzáférés a forrás megosztásához</span><span class="sxs-lookup"><span data-stu-id="f30df-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="f30df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f30df-104">SYNTAX</span></span>

### <span data-ttu-id="f30df-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f30df-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f30df-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f30df-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f30df-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f30df-107">DESCRIPTION</span></span>
<span data-ttu-id="f30df-108">A **Visszavonás-AzDataShareSubscriptionAccess** parancsmag előfizetéses hozzáférést ad a forrás megosztásához</span><span class="sxs-lookup"><span data-stu-id="f30df-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="f30df-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f30df-109">EXAMPLES</span></span>

### <span data-ttu-id="f30df-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f30df-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="f30df-111">A megosztási előfizetés hozzáférésének visszavonása azonosító 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 alapján</span><span class="sxs-lookup"><span data-stu-id="f30df-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="f30df-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f30df-112">PARAMETERS</span></span>

### <span data-ttu-id="f30df-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f30df-113">-AccountName</span></span>
<span data-ttu-id="f30df-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="f30df-114">Azure data share account name</span></span>

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

### <span data-ttu-id="f30df-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f30df-115">-AsJob</span></span>
<span data-ttu-id="f30df-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="f30df-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30df-117">-DefaultProfile</span></span>
<span data-ttu-id="f30df-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f30df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f30df-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30df-119">-ResourceGroupName</span></span>
<span data-ttu-id="f30df-120">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="f30df-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f30df-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f30df-121">-ResourceId</span></span>
<span data-ttu-id="f30df-122">Az Azure-adatmegosztás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="f30df-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="f30df-123">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="f30df-123">-ShareName</span></span>
<span data-ttu-id="f30df-124">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="f30df-124">Azure data share name</span></span>

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

### <span data-ttu-id="f30df-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f30df-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="f30df-126">A szolgáltató megosztási előfizetésének megosztása</span><span class="sxs-lookup"><span data-stu-id="f30df-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="f30df-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f30df-127">-Confirm</span></span>
<span data-ttu-id="f30df-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f30df-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f30df-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f30df-129">-WhatIf</span></span>
<span data-ttu-id="f30df-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f30df-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f30df-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f30df-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f30df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30df-132">CommonParameters</span></span>
<span data-ttu-id="f30df-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f30df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30df-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f30df-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30df-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30df-135">INPUTS</span></span>

### <span data-ttu-id="f30df-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f30df-136">System.String</span></span>

## <span data-ttu-id="f30df-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f30df-137">OUTPUTS</span></span>

### <span data-ttu-id="f30df-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="f30df-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="f30df-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f30df-139">NOTES</span></span>

## <span data-ttu-id="f30df-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f30df-140">RELATED LINKS</span></span>
