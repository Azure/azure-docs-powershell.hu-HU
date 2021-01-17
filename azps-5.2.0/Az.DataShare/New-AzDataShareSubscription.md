---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324362"
---
# <span data-ttu-id="b2c62-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="b2c62-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="b2c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2c62-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c62-103">Létrehoz egy új megosztási előfizetést.</span><span class="sxs-lookup"><span data-stu-id="b2c62-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="b2c62-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2c62-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2c62-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2c62-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c62-106">A **New-AzDataShareSubscription** parancsmag létrehoz egy megosztási előfizetést a megadott adatmegosztási fiókban és meghívóazonosítóban.</span><span class="sxs-lookup"><span data-stu-id="b2c62-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="b2c62-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2c62-107">EXAMPLES</span></span>

### <span data-ttu-id="b2c62-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b2c62-108">Example 1</span></span>
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

<span data-ttu-id="b2c62-109">Ezzel a paranccsal új megosztási előfizetést hoz létre a WikiAds adatmegosztási fiókban elérhető AdsShareSubscription for invitaionId szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="b2c62-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="b2c62-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2c62-110">PARAMETERS</span></span>

### <span data-ttu-id="b2c62-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b2c62-111">-AccountName</span></span>
<span data-ttu-id="b2c62-112">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="b2c62-112">Azure data share account name</span></span>

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

### <span data-ttu-id="b2c62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c62-113">-DefaultProfile</span></span>
<span data-ttu-id="b2c62-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2c62-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2c62-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="b2c62-115">-InvitationId</span></span>
<span data-ttu-id="b2c62-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="b2c62-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="b2c62-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2c62-117">-Name</span></span>
<span data-ttu-id="b2c62-118">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="b2c62-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b2c62-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2c62-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2c62-120">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="b2c62-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b2c62-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="b2c62-121">-SourceShareLocation</span></span>
<span data-ttu-id="b2c62-122">Azure-adatok megosztásának helye</span><span class="sxs-lookup"><span data-stu-id="b2c62-122">Azure data share location</span></span>

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

### <span data-ttu-id="b2c62-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2c62-123">-Confirm</span></span>
<span data-ttu-id="b2c62-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b2c62-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2c62-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2c62-125">-WhatIf</span></span>
<span data-ttu-id="b2c62-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b2c62-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2c62-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2c62-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2c62-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c62-128">CommonParameters</span></span>
<span data-ttu-id="b2c62-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c62-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c62-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2c62-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c62-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2c62-131">INPUTS</span></span>

### <span data-ttu-id="b2c62-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="b2c62-132">None</span></span>

## <span data-ttu-id="b2c62-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2c62-133">OUTPUTS</span></span>

### <span data-ttu-id="b2c62-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="b2c62-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="b2c62-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2c62-135">NOTES</span></span>

## <span data-ttu-id="b2c62-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2c62-136">RELATED LINKS</span></span>
