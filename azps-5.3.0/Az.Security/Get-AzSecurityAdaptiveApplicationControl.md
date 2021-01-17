---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479804"
---
# <span data-ttu-id="bff34-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="bff34-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="bff34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff34-102">SYNOPSIS</span></span>
<span data-ttu-id="bff34-103">Lekérte az előfizetés vmi/kiszolgálói csoportjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="bff34-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="bff34-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bff34-104">SYNTAX</span></span>

### <span data-ttu-id="bff34-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bff34-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bff34-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bff34-106">DESCRIPTION</span></span>
<span data-ttu-id="bff34-107">Az adaptív alkalmazásvezérlőket az Azure Biztonsági központ automatikusan kiszámítja. Ezzel a parancsmaggal lekérte az adaptív alkalmazásvezérlők erőforrásainak listáját az előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="bff34-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="bff34-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bff34-108">EXAMPLES</span></span>

### <span data-ttu-id="bff34-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="bff34-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="bff34-110">Lekérte az előfizetés vmi/kiszolgálói csoportjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="bff34-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="bff34-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bff34-111">PARAMETERS</span></span>

### <span data-ttu-id="bff34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff34-112">-DefaultProfile</span></span>
<span data-ttu-id="bff34-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bff34-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bff34-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bff34-114">-SubscriptionId</span></span>
<span data-ttu-id="bff34-115">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="bff34-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff34-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="bff34-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="bff34-117">A házirendszabályokat is foglalja bele.</span><span class="sxs-lookup"><span data-stu-id="bff34-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff34-118">-Summary</span><span class="sxs-lookup"><span data-stu-id="bff34-118">-Summary</span></span>
<span data-ttu-id="bff34-119">Eredményként összesített formában adja vissza a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="bff34-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff34-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff34-120">CommonParameters</span></span>
<span data-ttu-id="bff34-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff34-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff34-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff34-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff34-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bff34-123">INPUTS</span></span>

### <span data-ttu-id="bff34-124">System.String</span><span class="sxs-lookup"><span data-stu-id="bff34-124">System.String</span></span>

### <span data-ttu-id="bff34-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bff34-125">System.Boolean</span></span>

## <span data-ttu-id="bff34-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bff34-126">OUTPUTS</span></span>

### <span data-ttu-id="bff34-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="bff34-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="bff34-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bff34-128">NOTES</span></span>

## <span data-ttu-id="bff34-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bff34-129">RELATED LINKS</span></span>
