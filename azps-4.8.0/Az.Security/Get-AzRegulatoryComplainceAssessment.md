---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplainceAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplainceAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplainceAssessment.md
ms.openlocfilehash: 1fdfa13f2389fe34b2866c303da432dc6238d728
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024470"
---
# <span data-ttu-id="c2222-101">Get-AzRegulatoryComplainceAssessment</span><span class="sxs-lookup"><span data-stu-id="c2222-101">Get-AzRegulatoryComplainceAssessment</span></span>

## <span data-ttu-id="c2222-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2222-102">SYNOPSIS</span></span>
<span data-ttu-id="c2222-103">Szabályozási megfelelőségi felméréseket kap</span><span class="sxs-lookup"><span data-stu-id="c2222-103">Gets regulatory compliance assessments</span></span>

## <span data-ttu-id="c2222-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2222-104">SYNTAX</span></span>

### <span data-ttu-id="c2222-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2222-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplainceAssessment [-Name <String>] -StandardName <String> -ControlName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2222-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2222-106">ResourceId</span></span>
```
Get-AzRegulatoryComplainceAssessment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2222-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2222-107">DESCRIPTION</span></span>
<span data-ttu-id="c2222-108">Tekintse meg a spcific-felmérés részleteit, vagy tekintse meg az összes felmérést a meghatározott szabályozási és megfelelőségi szabványoknak megfelelően.</span><span class="sxs-lookup"><span data-stu-id="c2222-108">Get a spcific assessment details or list all the assessments under specific control and regulatory compliance standard.</span></span>

## <span data-ttu-id="c2222-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2222-109">EXAMPLES</span></span>

### <span data-ttu-id="c2222-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c2222-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplainceAssessment -StandardName "SOC TSP" -ControlName "CC5.8"

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/0392
                        b393-395e-42bf-ba60-8d99efc4d2d4
Name                  : 0392b393-395e-42bf-ba60-8d99efc4d2d4
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-10596-5] Deny log on as a batch job (Windows Server 2008 R2 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/04c8
                        24de-a93c-49cf-bb22-997cdff9e9fc
Name                  : 04c824de-a93c-49cf-bb22-997cdff9e9fc
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-24406-1] Allow log on through Remote Desktop Services (Windows Server 2012 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/04e7
                        147b-0deb-9796-2e5c-0336343ceb3d
Name                  : 04e7147b-0deb-9796-2e5c-0336343ceb3d
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : External accounts with write permissions should be removed from your subscription
AssessmentType        : AssessmentResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 1
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/0515
                        45a4-179e-4c04-9e9b-8f33821ef36f
Name                  : 051545a4-179e-4c04-9e9b-8f33821ef36f
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-37659-0] Configure 'Allow log on locally' (Windows Server 2016 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Failed
PassedResources       : 1
FailedResources       : 1
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/101e
                        af81-3dd3-4867-8871-f649131a06a9
Name                  : 101eaf81-3dd3-4867-8871-f649131a06a9
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-38028-7] Audit Policy: Policy Change: Audit Policy Change (Windows Server 2012 R2
                        Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/103d
                        e8e8-643e-4b0e-b4a4-a85830239a53
Name                  : 103de8e8-643e-4b0e-b4a4-a85830239a53
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-37133-6] Ensure 'Audit Account Lockout' is set to 'Success and Failure' (Windows Server
                        2016 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Failed
PassedResources       : 1
FailedResources       : 1
SkippedResources      : 0

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/107b
                        8424-7ee8-4b6a-a859-b5256aa6596e
Name                  : 107b8424-7ee8-4b6a-a859-b5256aa6596e
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-37853-9] Audit Policy: System: IPsec Driver (Windows Server 2012 R2 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0
```

<span data-ttu-id="c2222-111">A megadott vezérlők és szabványok szerinti felmérések beszerzése</span><span class="sxs-lookup"><span data-stu-id="c2222-111">Get all assessments under specific control and standard.</span></span>

### <span data-ttu-id="c2222-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="c2222-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplainceAssessment -StandardName "SOC TSP" -ControlName "CC5.8" -Name "fe48038b-f73a-4264-b499-0ff9dfaab05c"

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/fe48
                        038b-f73a-4264-b499-0ff9dfaab05c
Name                  : fe48038b-f73a-4264-b499-0ff9dfaab05c
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-24187-7] Audit Policy: Logon-Logoff: Special Logon (Windows Server 2012 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0
```

<span data-ttu-id="c2222-113">A vizsgálati azonosító szerint meghatározott ellenőrzés és szabvány szerinti konkrét felmérést kaphat.</span><span class="sxs-lookup"><span data-stu-id="c2222-113">Get a specific assessment under specific control and standard according to assessment id.</span></span>

### <span data-ttu-id="c2222-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="c2222-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplainceAssessment -ResourceId"/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/fe48038b-f73a-4264-b499-0ff9dfaab05c"

Id                    : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComp
                        lianceStandards/SOC-TSP/regulatoryComplianceControls/CC5.8/regulatoryComplianceAssessments/fe48
                        038b-f73a-4264-b499-0ff9dfaab05c
Name                  : fe48038b-f73a-4264-b499-0ff9dfaab05c
Type                  : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls/regulatoryComplia
                        nceAssessments
Description           : [CCE-24187-7] Audit Policy: Logon-Logoff: Special Logon (Windows Server 2012 Datacenter)
AssessmentType        : RuleResult
AssessmentDetailsLink :
State                 : Passed
PassedResources       : 2
FailedResources       : 0
SkippedResources      : 0
```

<span data-ttu-id="c2222-115">Az erőforrás-azonosító szerint meghatározott vezérlők és szabványok szerint meghatározott felmérést kaphat.</span><span class="sxs-lookup"><span data-stu-id="c2222-115">Get a specific assessment under specific control and standard according to resource id.</span></span>

## <span data-ttu-id="c2222-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2222-116">PARAMETERS</span></span>

### <span data-ttu-id="c2222-117">-Vezérlőelemnév</span><span class="sxs-lookup"><span data-stu-id="c2222-117">-ControlName</span></span>
<span data-ttu-id="c2222-118">Vezérlő neve</span><span class="sxs-lookup"><span data-stu-id="c2222-118">Control Name.</span></span>

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

### <span data-ttu-id="c2222-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2222-119">-DefaultProfile</span></span>
<span data-ttu-id="c2222-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2222-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2222-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2222-121">-Name</span></span>
<span data-ttu-id="c2222-122">Assessment (azonosító)</span><span class="sxs-lookup"><span data-stu-id="c2222-122">Assessment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2222-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2222-123">-ResourceId</span></span>
<span data-ttu-id="c2222-124">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="c2222-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c2222-125">-StandardName</span><span class="sxs-lookup"><span data-stu-id="c2222-125">-StandardName</span></span>
<span data-ttu-id="c2222-126">Szokásos név.</span><span class="sxs-lookup"><span data-stu-id="c2222-126">Standard Name.</span></span>

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

### <span data-ttu-id="c2222-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2222-127">CommonParameters</span></span>
<span data-ttu-id="c2222-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2222-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2222-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c2222-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2222-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2222-130">INPUTS</span></span>

### <span data-ttu-id="c2222-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c2222-131">System.String</span></span>

## <span data-ttu-id="c2222-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2222-132">OUTPUTS</span></span>

### <span data-ttu-id="c2222-133">Microsoft. Azure. Command. SecurityCenter. models. RegulatoryCompliance. PSSecurityRegulatoryComplianceAssessment</span><span class="sxs-lookup"><span data-stu-id="c2222-133">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceAssessment</span></span>

## <span data-ttu-id="c2222-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2222-134">NOTES</span></span>

## <span data-ttu-id="c2222-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2222-135">RELATED LINKS</span></span>
