---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145834"
---
# <span data-ttu-id="e1b13-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="e1b13-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="e1b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1b13-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b13-103">Lekérte az előfizetés vmi/kiszolgálói csoportjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="e1b13-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="e1b13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1b13-104">SYNTAX</span></span>

### <span data-ttu-id="e1b13-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1b13-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1b13-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1b13-106">DESCRIPTION</span></span>
<span data-ttu-id="e1b13-107">Az adaptív alkalmazásvezérlőket az Azure Biztonsági központ automatikusan kiszámítja. Ezzel a parancsmaggal lekérte az adaptív alkalmazásvezérlők erőforrásainak listáját az előfizetés hatókörében.</span><span class="sxs-lookup"><span data-stu-id="e1b13-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="e1b13-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1b13-108">EXAMPLES</span></span>

### <span data-ttu-id="e1b13-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="e1b13-109">Example 1</span></span>
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
<span data-ttu-id="e1b13-110">Lekérte az előfizetés vmi/kiszolgálói csoportjainak listáját.</span><span class="sxs-lookup"><span data-stu-id="e1b13-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="e1b13-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1b13-111">PARAMETERS</span></span>

### <span data-ttu-id="e1b13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b13-112">-DefaultProfile</span></span>
<span data-ttu-id="e1b13-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1b13-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1b13-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1b13-114">-SubscriptionId</span></span>
<span data-ttu-id="e1b13-115">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e1b13-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="e1b13-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="e1b13-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="e1b13-117">A házirendszabályokat is foglalja bele.</span><span class="sxs-lookup"><span data-stu-id="e1b13-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="e1b13-118">-Summary</span><span class="sxs-lookup"><span data-stu-id="e1b13-118">-Summary</span></span>
<span data-ttu-id="e1b13-119">Eredményként összesített formában adja vissza a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="e1b13-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="e1b13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b13-120">CommonParameters</span></span>
<span data-ttu-id="e1b13-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b13-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1b13-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b13-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1b13-123">INPUTS</span></span>

### <span data-ttu-id="e1b13-124">System.String</span><span class="sxs-lookup"><span data-stu-id="e1b13-124">System.String</span></span>

### <span data-ttu-id="e1b13-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e1b13-125">System.Boolean</span></span>

## <span data-ttu-id="e1b13-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1b13-126">OUTPUTS</span></span>

### <span data-ttu-id="e1b13-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="e1b13-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="e1b13-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1b13-128">NOTES</span></span>

## <span data-ttu-id="e1b13-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1b13-129">RELATED LINKS</span></span>
