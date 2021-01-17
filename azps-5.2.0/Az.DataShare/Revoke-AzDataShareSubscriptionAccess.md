---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360834"
---
# <span data-ttu-id="7131a-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="7131a-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="7131a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7131a-102">SYNOPSIS</span></span>
<span data-ttu-id="7131a-103">Előfizetés megosztásának visszavonása a forrás-megosztáshoz</span><span class="sxs-lookup"><span data-stu-id="7131a-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="7131a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7131a-104">SYNTAX</span></span>

### <span data-ttu-id="7131a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7131a-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7131a-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7131a-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7131a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7131a-107">DESCRIPTION</span></span>
<span data-ttu-id="7131a-108">Az **Revoke-AzDataShareSubscriptionAccess** parancsmag share-előfizetési hozzáférést biztosít a forrásmegosztáshoz</span><span class="sxs-lookup"><span data-stu-id="7131a-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="7131a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7131a-109">EXAMPLES</span></span>

### <span data-ttu-id="7131a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7131a-110">Example 1</span></span>
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

<span data-ttu-id="7131a-111">A 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 azonosító által azonosított megosztási előfizetés hozzáférésének visszavonása</span><span class="sxs-lookup"><span data-stu-id="7131a-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="7131a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7131a-112">PARAMETERS</span></span>

### <span data-ttu-id="7131a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7131a-113">-AccountName</span></span>
<span data-ttu-id="7131a-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="7131a-114">Azure data share account name</span></span>

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

### <span data-ttu-id="7131a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7131a-115">-AsJob</span></span>
<span data-ttu-id="7131a-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="7131a-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="7131a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7131a-117">-DefaultProfile</span></span>
<span data-ttu-id="7131a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7131a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7131a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7131a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7131a-120">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="7131a-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7131a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7131a-121">-ResourceId</span></span>
<span data-ttu-id="7131a-122">Az Azure-adat megosztásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7131a-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="7131a-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="7131a-123">-ShareName</span></span>
<span data-ttu-id="7131a-124">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="7131a-124">Azure data share name</span></span>

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

### <span data-ttu-id="7131a-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7131a-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="7131a-126">A szolgáltatói megosztási előfizetés megosztási előfizetésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="7131a-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="7131a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7131a-127">-Confirm</span></span>
<span data-ttu-id="7131a-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7131a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7131a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7131a-129">-WhatIf</span></span>
<span data-ttu-id="7131a-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7131a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7131a-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7131a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7131a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7131a-132">CommonParameters</span></span>
<span data-ttu-id="7131a-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7131a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7131a-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7131a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7131a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7131a-135">INPUTS</span></span>

### <span data-ttu-id="7131a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7131a-136">System.String</span></span>

## <span data-ttu-id="7131a-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7131a-137">OUTPUTS</span></span>

### <span data-ttu-id="7131a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="7131a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="7131a-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7131a-139">NOTES</span></span>

## <span data-ttu-id="7131a-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7131a-140">RELATED LINKS</span></span>
