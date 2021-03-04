---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: a7b3a60d97692d01eb8be374ab9670af4b331f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941850"
---
# <span data-ttu-id="a5216-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a5216-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="a5216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5216-102">SYNOPSIS</span></span>
<span data-ttu-id="a5216-103">Létrehoz egy új megosztási előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a5216-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="a5216-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a5216-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5216-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a5216-105">DESCRIPTION</span></span>
<span data-ttu-id="a5216-106">A **New-AzDataShareSubscription** parancsmag létrehoz egy megosztási előfizetést a megadott adatmegosztási fiókban és meghívóazonosítóban.</span><span class="sxs-lookup"><span data-stu-id="a5216-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="a5216-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a5216-107">EXAMPLES</span></span>

### <span data-ttu-id="a5216-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a5216-108">Example 1</span></span>
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

<span data-ttu-id="a5216-109">Ez a parancs új megosztási előfizetést hoz létre AdsShareSubscription invitaionId számára a WikiAds adatmegosztási fiók alatt.</span><span class="sxs-lookup"><span data-stu-id="a5216-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="a5216-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5216-110">PARAMETERS</span></span>

### <span data-ttu-id="a5216-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5216-111">-AccountName</span></span>
<span data-ttu-id="a5216-112">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="a5216-112">Azure data share account name</span></span>

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

### <span data-ttu-id="a5216-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5216-113">-DefaultProfile</span></span>
<span data-ttu-id="a5216-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5216-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5216-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="a5216-115">-InvitationId</span></span>
<span data-ttu-id="a5216-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="a5216-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="a5216-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a5216-117">-Name</span></span>
<span data-ttu-id="a5216-118">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="a5216-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a5216-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5216-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5216-120">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="a5216-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a5216-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="a5216-121">-SourceShareLocation</span></span>
<span data-ttu-id="a5216-122">Azure-adatok megosztásának helye</span><span class="sxs-lookup"><span data-stu-id="a5216-122">Azure data share location</span></span>

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

### <span data-ttu-id="a5216-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5216-123">-Confirm</span></span>
<span data-ttu-id="a5216-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a5216-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5216-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5216-125">-WhatIf</span></span>
<span data-ttu-id="a5216-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a5216-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5216-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5216-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5216-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5216-128">CommonParameters</span></span>
<span data-ttu-id="a5216-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5216-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5216-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5216-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5216-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5216-131">INPUTS</span></span>

### <span data-ttu-id="a5216-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5216-132">None</span></span>

## <span data-ttu-id="a5216-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5216-133">OUTPUTS</span></span>

### <span data-ttu-id="a5216-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="a5216-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="a5216-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a5216-135">NOTES</span></span>

## <span data-ttu-id="a5216-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5216-136">RELATED LINKS</span></span>
