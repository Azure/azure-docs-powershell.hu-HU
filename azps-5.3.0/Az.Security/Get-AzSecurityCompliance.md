---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityCompliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
ms.openlocfilehash: 6009ec12b50e1960cbe241bf936d9cfedf2fea2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479788"
---
# <span data-ttu-id="c38f0-101">Get-AzSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="c38f0-101">Get-AzSecurityCompliance</span></span>

## <span data-ttu-id="c38f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c38f0-102">SYNOPSIS</span></span>
<span data-ttu-id="c38f0-103">Előfizetés biztonsági megfelelőségének biztosítása időben</span><span class="sxs-lookup"><span data-stu-id="c38f0-103">Get the security compliance of a subscription over time</span></span>

## <span data-ttu-id="c38f0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c38f0-104">SYNTAX</span></span>

### <span data-ttu-id="c38f0-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c38f0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c38f0-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c38f0-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c38f0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c38f0-107">ResourceId</span></span>
```
Get-AzSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c38f0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c38f0-108">DESCRIPTION</span></span>
<span data-ttu-id="c38f0-109">Az előfizetés biztonsági megfelelőségét az előfizetés aktuális egészséges és nem biztonságos erőforrásainak aránya alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c38f0-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="c38f0-110">A rendszer minden nap kiszámítja a biztonsági megfelelőség számítását, és menti az előzményeket.</span><span class="sxs-lookup"><span data-stu-id="c38f0-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="c38f0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c38f0-111">EXAMPLES</span></span>

### <span data-ttu-id="c38f0-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="c38f0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-19Z
Name                       : 2018-08-19Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 19/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-18Z
Name                       : 2018-08-18Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 18/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-17Z
Name                       : 2018-08-17Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 17/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-16Z
Name                       : 2018-08-16Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 16/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-15Z
Name                       : 2018-08-15Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 15/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-14Z
Name                       : 2018-08-14Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 14/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-13Z
Name                       : 2018-08-13Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 13/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-12Z
Name                       : 2018-08-12Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 12/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-11Z
Name                       : 2018-08-11Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 11/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-10Z
Name                       : 2018-08-10Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 10/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-09Z
Name                       : 2018-08-09Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 09/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-08Z
Name                       : 2018-08-08Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 08/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-07Z
Name                       : 2018-08-07Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 07/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="c38f0-113">Megkapja az előfizetés biztonsági megfelelőségét az elmúlt 14 napra</span><span class="sxs-lookup"><span data-stu-id="c38f0-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="c38f0-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="c38f0-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="c38f0-115">Egy adott napon megkapja az előfizetés biztonsági megfelelőségét</span><span class="sxs-lookup"><span data-stu-id="c38f0-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="c38f0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c38f0-116">PARAMETERS</span></span>

### <span data-ttu-id="c38f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c38f0-117">-DefaultProfile</span></span>
<span data-ttu-id="c38f0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c38f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c38f0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c38f0-119">-Name</span></span>
<span data-ttu-id="c38f0-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="c38f0-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c38f0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c38f0-121">-ResourceId</span></span>
<span data-ttu-id="c38f0-122">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c38f0-122">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c38f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c38f0-123">CommonParameters</span></span>
<span data-ttu-id="c38f0-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c38f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c38f0-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c38f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c38f0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c38f0-126">INPUTS</span></span>

### <span data-ttu-id="c38f0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c38f0-127">System.String</span></span>

## <span data-ttu-id="c38f0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c38f0-128">OUTPUTS</span></span>

### <span data-ttu-id="c38f0-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="c38f0-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="c38f0-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c38f0-130">NOTES</span></span>

## <span data-ttu-id="c38f0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c38f0-131">RELATED LINKS</span></span>
