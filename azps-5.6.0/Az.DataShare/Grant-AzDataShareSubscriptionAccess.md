---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 00b82731e807aa2351d66744b889f56f440226b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006773"
---
# <span data-ttu-id="7867e-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="7867e-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="7867e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7867e-102">SYNOPSIS</span></span>
<span data-ttu-id="7867e-103">Visszavont megosztási előfizetési hozzáférés a forrás megosztáshoz</span><span class="sxs-lookup"><span data-stu-id="7867e-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="7867e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7867e-104">SYNTAX</span></span>

### <span data-ttu-id="7867e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7867e-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7867e-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7867e-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7867e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7867e-107">DESCRIPTION</span></span>
<span data-ttu-id="7867e-108">A **Grant-AzDataShareSubscriptionAccess** parancsmag share-előfizetési hozzáférést biztosít a forrásmegosztáshoz</span><span class="sxs-lookup"><span data-stu-id="7867e-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="7867e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7867e-109">EXAMPLES</span></span>

### <span data-ttu-id="7867e-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7867e-110">Example 1</span></span>
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

<span data-ttu-id="7867e-111">Hozzáférést biztosít a 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 azonosítóval azonosított megosztási előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="7867e-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="7867e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7867e-112">PARAMETERS</span></span>

### <span data-ttu-id="7867e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7867e-113">-AccountName</span></span>
<span data-ttu-id="7867e-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="7867e-114">Azure data share account name</span></span>

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

### <span data-ttu-id="7867e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7867e-115">-DefaultProfile</span></span>
<span data-ttu-id="7867e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7867e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7867e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7867e-117">-ResourceGroupName</span></span>
<span data-ttu-id="7867e-118">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="7867e-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7867e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7867e-119">-ResourceId</span></span>
<span data-ttu-id="7867e-120">Az Azure-adat megosztásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7867e-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="7867e-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7867e-121">-ShareName</span></span>
<span data-ttu-id="7867e-122">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="7867e-122">Azure data share name</span></span>

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

### <span data-ttu-id="7867e-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7867e-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="7867e-124">A szolgáltatói megosztási előfizetés megosztási előfizetésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="7867e-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="7867e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7867e-125">-Confirm</span></span>
<span data-ttu-id="7867e-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7867e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7867e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7867e-127">-WhatIf</span></span>
<span data-ttu-id="7867e-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7867e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7867e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7867e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7867e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7867e-130">CommonParameters</span></span>
<span data-ttu-id="7867e-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7867e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7867e-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7867e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7867e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7867e-133">INPUTS</span></span>

### <span data-ttu-id="7867e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7867e-134">System.String</span></span>

## <span data-ttu-id="7867e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7867e-135">OUTPUTS</span></span>

### <span data-ttu-id="7867e-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="7867e-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="7867e-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7867e-137">NOTES</span></span>

## <span data-ttu-id="7867e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7867e-138">RELATED LINKS</span></span>
