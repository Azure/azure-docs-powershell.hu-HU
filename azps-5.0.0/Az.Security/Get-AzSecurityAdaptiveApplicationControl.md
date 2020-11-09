---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302441"
---
# <span data-ttu-id="b34b1-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="b34b1-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="b34b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b34b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b34b1-103">Az előfizetéshez tartozó Application Control VM/Server csoportok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b34b1-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="b34b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b34b1-104">SYNTAX</span></span>

### <span data-ttu-id="b34b1-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b34b1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b34b1-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="b34b1-106">DESCRIPTION</span></span>
<span data-ttu-id="b34b1-107">A program automatikusan kiszámítja az adaptív alkalmazások vezérlőit az Azure Security Center segítségével, ezzel a parancsmaggal lekérheti az adaptív alkalmazások listáját az előfizetések terjedelmében.</span><span class="sxs-lookup"><span data-stu-id="b34b1-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="b34b1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b34b1-108">EXAMPLES</span></span>

### <span data-ttu-id="b34b1-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b34b1-109">Example 1</span></span>
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
<span data-ttu-id="b34b1-110">Az előfizetéshez tartozó Application Control VM/Server csoportok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b34b1-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="b34b1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b34b1-111">PARAMETERS</span></span>

### <span data-ttu-id="b34b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34b1-112">-DefaultProfile</span></span>
<span data-ttu-id="b34b1-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b34b1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b34b1-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b34b1-114">-SubscriptionId</span></span>
<span data-ttu-id="b34b1-115">Azure-előfizetési azonosító</span><span class="sxs-lookup"><span data-stu-id="b34b1-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="b34b1-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="b34b1-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="b34b1-117">Adja meg a házirend-szabályokat.</span><span class="sxs-lookup"><span data-stu-id="b34b1-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="b34b1-118">– Összefoglalás</span><span class="sxs-lookup"><span data-stu-id="b34b1-118">-Summary</span></span>
<span data-ttu-id="b34b1-119">A kimenet visszaadása összegzett formában</span><span class="sxs-lookup"><span data-stu-id="b34b1-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="b34b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34b1-120">CommonParameters</span></span>
<span data-ttu-id="b34b1-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b34b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34b1-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34b1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34b1-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b34b1-123">INPUTS</span></span>

### <span data-ttu-id="b34b1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b34b1-124">System.String</span></span>

### <span data-ttu-id="b34b1-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b34b1-125">System.Boolean</span></span>

## <span data-ttu-id="b34b1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b34b1-126">OUTPUTS</span></span>

### <span data-ttu-id="b34b1-127">Microsoft. Azure. commands. Security. models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="b34b1-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="b34b1-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b34b1-128">NOTES</span></span>

## <span data-ttu-id="b34b1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b34b1-129">RELATED LINKS</span></span>
