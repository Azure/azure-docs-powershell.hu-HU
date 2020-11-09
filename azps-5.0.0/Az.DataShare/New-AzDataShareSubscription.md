---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297428"
---
# <span data-ttu-id="3e572-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3e572-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="3e572-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e572-102">SYNOPSIS</span></span>
<span data-ttu-id="3e572-103">Új megosztási előfizetést hoz létre.</span><span class="sxs-lookup"><span data-stu-id="3e572-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="3e572-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e572-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e572-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e572-105">DESCRIPTION</span></span>
<span data-ttu-id="3e572-106">A **New-AzDataShareSubscription** parancsmag létrehoz egy megosztási előfizetést a megadott adatmegosztási fiókban és meghívás-azonosítóban.</span><span class="sxs-lookup"><span data-stu-id="3e572-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="3e572-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3e572-107">EXAMPLES</span></span>

### <span data-ttu-id="3e572-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3e572-108">Example 1</span></span>
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

<span data-ttu-id="3e572-109">Ez a parancs új megosztási előfizetési AdsShareSubscription hoz létre a invitaionId az adatmegosztási fiók WikiAds csoportban.</span><span class="sxs-lookup"><span data-stu-id="3e572-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="3e572-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e572-110">PARAMETERS</span></span>

### <span data-ttu-id="3e572-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e572-111">-AccountName</span></span>
<span data-ttu-id="3e572-112">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="3e572-112">Azure data share account name</span></span>

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

### <span data-ttu-id="3e572-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e572-113">-DefaultProfile</span></span>
<span data-ttu-id="3e572-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e572-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e572-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="3e572-115">-InvitationId</span></span>
<span data-ttu-id="3e572-116">Azure Data Share invitationId</span><span class="sxs-lookup"><span data-stu-id="3e572-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="3e572-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3e572-117">-Name</span></span>
<span data-ttu-id="3e572-118">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="3e572-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="3e572-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e572-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e572-120">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="3e572-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3e572-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="3e572-121">-SourceShareLocation</span></span>
<span data-ttu-id="3e572-122">Azure Data Share-hely</span><span class="sxs-lookup"><span data-stu-id="3e572-122">Azure data share location</span></span>

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

### <span data-ttu-id="3e572-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e572-123">-Confirm</span></span>
<span data-ttu-id="3e572-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e572-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e572-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e572-125">-WhatIf</span></span>
<span data-ttu-id="3e572-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e572-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e572-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e572-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e572-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e572-128">CommonParameters</span></span>
<span data-ttu-id="3e572-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e572-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e572-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3e572-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e572-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e572-131">INPUTS</span></span>

### <span data-ttu-id="3e572-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="3e572-132">None</span></span>

## <span data-ttu-id="3e572-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e572-133">OUTPUTS</span></span>

### <span data-ttu-id="3e572-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="3e572-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="3e572-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e572-135">NOTES</span></span>

## <span data-ttu-id="3e572-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e572-136">RELATED LINKS</span></span>
