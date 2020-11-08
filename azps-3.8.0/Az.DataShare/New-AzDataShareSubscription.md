---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 01cff184a2db4364536d4088103380f3f28b47a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011829"
---
# <span data-ttu-id="8d35f-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8d35f-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="8d35f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d35f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d35f-103">Új megosztási előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8d35f-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="8d35f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d35f-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d35f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d35f-105">DESCRIPTION</span></span>
<span data-ttu-id="8d35f-106">A **New-AzDataShareSubscription** parancsmag létrehoz egy megosztási előfizetést a megadott adatmegosztási fiókban és meghívás-azonosítóban.</span><span class="sxs-lookup"><span data-stu-id="8d35f-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="8d35f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8d35f-107">EXAMPLES</span></span>

### <span data-ttu-id="8d35f-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d35f-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="8d35f-109">Ez a parancs új megosztási előfizetési AdsShareSubscription hoz létre a invitaionId az adatmegosztási fiók WikiAds csoportban.</span><span class="sxs-lookup"><span data-stu-id="8d35f-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="8d35f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d35f-110">PARAMETERS</span></span>

### <span data-ttu-id="8d35f-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d35f-111">-AccountName</span></span>
<span data-ttu-id="8d35f-112">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="8d35f-112">Azure data share account name</span></span>

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

### <span data-ttu-id="8d35f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d35f-113">-DefaultProfile</span></span>
<span data-ttu-id="8d35f-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d35f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d35f-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="8d35f-115">-InvitationId</span></span>
<span data-ttu-id="8d35f-116">Azure Data Share invitationId</span><span class="sxs-lookup"><span data-stu-id="8d35f-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="8d35f-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d35f-117">-Name</span></span>
<span data-ttu-id="8d35f-118">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="8d35f-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8d35f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d35f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d35f-120">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="8d35f-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8d35f-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d35f-121">-Confirm</span></span>
<span data-ttu-id="8d35f-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d35f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d35f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d35f-123">-WhatIf</span></span>
<span data-ttu-id="8d35f-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d35f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d35f-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d35f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d35f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d35f-126">CommonParameters</span></span>
<span data-ttu-id="8d35f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d35f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d35f-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d35f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d35f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d35f-129">INPUTS</span></span>

### <span data-ttu-id="8d35f-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="8d35f-130">None</span></span>

## <span data-ttu-id="8d35f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d35f-131">OUTPUTS</span></span>

### <span data-ttu-id="8d35f-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8d35f-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8d35f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d35f-133">NOTES</span></span>

## <span data-ttu-id="8d35f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d35f-134">RELATED LINKS</span></span>
