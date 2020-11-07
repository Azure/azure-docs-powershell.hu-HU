---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 23553e939256b9124369afd79db29a50802dc6cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666731"
---
# <span data-ttu-id="6f1c6-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="6f1c6-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="6f1c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1c6-103">Információt kap az előfizetés megosztására az adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="6f1c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f1c6-104">SYNTAX</span></span>

### <span data-ttu-id="6f1c6-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f1c6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f1c6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f1c6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f1c6-107">DESCRIPTION</span></span>
<span data-ttu-id="6f1c6-108">A **Get-AzDataShareSubscription** parancsmag információkat nyújt az adatmegosztási fiókban való megosztási előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="6f1c6-109">Ha meg van határozva az előfizetés neve, a parancsmag információt ad az adott megosztási előfizetésről.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="6f1c6-110">Egyéb esetben a parancsmag a megosztási előfizetések listáját tartalmazza az adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="6f1c6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6f1c6-111">EXAMPLES</span></span>

### <span data-ttu-id="6f1c6-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6f1c6-112">Example 1</span></span>
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

<span data-ttu-id="6f1c6-113">Ez a parancs információkat nyújt az adatmegosztási fiók WikiAds az előfizetés AdsShareSubscription megosztásáról.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="6f1c6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-114">PARAMETERS</span></span>

### <span data-ttu-id="6f1c6-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6f1c6-115">-AccountName</span></span>
<span data-ttu-id="6f1c6-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="6f1c6-116">Azure data share account name</span></span>

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

### <span data-ttu-id="6f1c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1c6-117">-DefaultProfile</span></span>
<span data-ttu-id="6f1c6-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f1c6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f1c6-119">-Name</span></span>
<span data-ttu-id="6f1c6-120">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="6f1c6-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6f1c6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f1c6-121">-ResourceGroupName</span></span>
<span data-ttu-id="6f1c6-122">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="6f1c6-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6f1c6-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f1c6-123">-ResourceId</span></span>
<span data-ttu-id="6f1c6-124">Az Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6f1c6-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="6f1c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1c6-125">CommonParameters</span></span>
<span data-ttu-id="6f1c6-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f1c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1c6-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1c6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1c6-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-128">INPUTS</span></span>

### <span data-ttu-id="6f1c6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6f1c6-129">System.String</span></span>

## <span data-ttu-id="6f1c6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-130">OUTPUTS</span></span>

### <span data-ttu-id="6f1c6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="6f1c6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="6f1c6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f1c6-132">NOTES</span></span>

## <span data-ttu-id="6f1c6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-133">RELATED LINKS</span></span>
