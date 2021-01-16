---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377409"
---
# <span data-ttu-id="c4ca3-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c4ca3-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="c4ca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ca3-103">Információkat kap az előfizetés megosztásáról az adat-megosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c4ca3-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="c4ca3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4ca3-104">SYNTAX</span></span>

### <span data-ttu-id="c4ca3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4ca3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4ca3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4ca3-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4ca3-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4ca3-107">DESCRIPTION</span></span>
<span data-ttu-id="c4ca3-108">A **Get-AzDataShareSubscription** parancsmag információkat nyújt az adatmegosztási fiókban való előfizetés megosztásáról.</span><span class="sxs-lookup"><span data-stu-id="c4ca3-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="c4ca3-109">Ha meg van biztosítanak egy megosztási előfizetés nevét, a parancsmag információkat ad az adott megosztási előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="c4ca3-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="c4ca3-110">Ellenkező esetben a parancsmag felsorolja a megosztási előfizetéseket az adat-megosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c4ca3-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="c4ca3-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4ca3-111">EXAMPLES</span></span>

### <span data-ttu-id="c4ca3-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c4ca3-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="c4ca3-113">Ez a parancs információkat nyújt a Share Subscription AdsShareSubscription szolgáltatásról a WikiAds adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="c4ca3-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="c4ca3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4ca3-114">PARAMETERS</span></span>

### <span data-ttu-id="c4ca3-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4ca3-115">-AccountName</span></span>
<span data-ttu-id="c4ca3-116">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="c4ca3-116">Azure data share account name</span></span>

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

### <span data-ttu-id="c4ca3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ca3-117">-DefaultProfile</span></span>
<span data-ttu-id="c4ca3-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4ca3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ca3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ca3-119">-Name</span></span>
<span data-ttu-id="c4ca3-120">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="c4ca3-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c4ca3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ca3-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4ca3-122">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="c4ca3-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c4ca3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4ca3-123">-ResourceId</span></span>
<span data-ttu-id="c4ca3-124">Az Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c4ca3-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="c4ca3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ca3-125">CommonParameters</span></span>
<span data-ttu-id="c4ca3-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ca3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ca3-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4ca3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ca3-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4ca3-128">INPUTS</span></span>

### <span data-ttu-id="c4ca3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c4ca3-129">System.String</span></span>

## <span data-ttu-id="c4ca3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4ca3-130">OUTPUTS</span></span>

### <span data-ttu-id="c4ca3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="c4ca3-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="c4ca3-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4ca3-132">NOTES</span></span>

## <span data-ttu-id="c4ca3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4ca3-133">RELATED LINKS</span></span>
