---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377339"
---
# <span data-ttu-id="179a1-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="179a1-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="179a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="179a1-102">SYNOPSIS</span></span>
<span data-ttu-id="179a1-103">Visszavont megosztási előfizetési hozzáférés a forrás megosztáshoz</span><span class="sxs-lookup"><span data-stu-id="179a1-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="179a1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="179a1-104">SYNTAX</span></span>

### <span data-ttu-id="179a1-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="179a1-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="179a1-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="179a1-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="179a1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="179a1-107">DESCRIPTION</span></span>
<span data-ttu-id="179a1-108">A **Grant-AzDataShareSubscriptionAccess** parancsmag share-előfizetési hozzáférést biztosít a forrásmegosztáshoz</span><span class="sxs-lookup"><span data-stu-id="179a1-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="179a1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="179a1-109">EXAMPLES</span></span>

### <span data-ttu-id="179a1-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="179a1-110">Example 1</span></span>
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

<span data-ttu-id="179a1-111">Hozzáférést biztosít a 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 azonosítóval azonosított megosztási előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="179a1-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="179a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="179a1-112">PARAMETERS</span></span>

### <span data-ttu-id="179a1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="179a1-113">-AccountName</span></span>
<span data-ttu-id="179a1-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="179a1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="179a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179a1-115">-DefaultProfile</span></span>
<span data-ttu-id="179a1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="179a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="179a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="179a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="179a1-118">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="179a1-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="179a1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="179a1-119">-ResourceId</span></span>
<span data-ttu-id="179a1-120">Az Azure-adat megosztásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="179a1-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="179a1-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="179a1-121">-ShareName</span></span>
<span data-ttu-id="179a1-122">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="179a1-122">Azure data share name</span></span>

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

### <span data-ttu-id="179a1-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="179a1-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="179a1-124">A szolgáltatói megosztási előfizetés megosztási előfizetésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="179a1-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="179a1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="179a1-125">-Confirm</span></span>
<span data-ttu-id="179a1-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="179a1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="179a1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="179a1-127">-WhatIf</span></span>
<span data-ttu-id="179a1-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="179a1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="179a1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="179a1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="179a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179a1-130">CommonParameters</span></span>
<span data-ttu-id="179a1-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="179a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179a1-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="179a1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179a1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="179a1-133">INPUTS</span></span>

### <span data-ttu-id="179a1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="179a1-134">System.String</span></span>

## <span data-ttu-id="179a1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="179a1-135">OUTPUTS</span></span>

### <span data-ttu-id="179a1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="179a1-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="179a1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="179a1-137">NOTES</span></span>

## <span data-ttu-id="179a1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="179a1-138">RELATED LINKS</span></span>
