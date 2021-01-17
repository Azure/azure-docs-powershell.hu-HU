---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479805"
---
# <span data-ttu-id="6fdb0-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="6fdb0-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="6fdb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdb0-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdb0-103">Szabályozási megfelelőségi vezérlőket kap</span><span class="sxs-lookup"><span data-stu-id="6fdb0-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="6fdb0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6fdb0-104">SYNTAX</span></span>

### <span data-ttu-id="6fdb0-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fdb0-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fdb0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fdb0-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fdb0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6fdb0-107">DESCRIPTION</span></span>
<span data-ttu-id="6fdb0-108">Részletes információkat olvashat a szabályozásról, vagy felsorolhatja az adott szabályozási megfelelőségi szabványoknak megfelelő összes vezérlőt.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="6fdb0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6fdb0-109">EXAMPLES</span></span>

### <span data-ttu-id="6fdb0-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="6fdb0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.1
Name               : A1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Current processing capacity and usage are maintained, monitored, and evaluated to manage capacity
                     demand and to enable the implementation of additional capacity to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.2
Name               : A1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Environmental protections, software, data backup processes, and recovery infrastructure are
                     designed, developed, implemented, operated, maintained, and monitored to meet availability
                     commitments and requirements.
State              : Passed
PassedAssessments  : 3
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/A1.3
Name               : A1.3
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Recovery plan procedures supporting system recovery are tested to help meet the entity�s
                     availability commitments and system requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.1
Name               : C1.1
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information is protected during the system design, development, testing,
                     implementation, and change processes in accordance with confidentiality commitments and
                     requirements.
State              : Unsupported
PassedAssessments  : 0
FailedAssessments  : 0
SkippedAssessments : 0
```

<span data-ttu-id="6fdb0-111">Az összes vezérlő lekértése adott szabályozási szabvány szerint.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="6fdb0-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="6fdb0-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -StandardName "SOC TSP" -Name "C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="6fdb0-113">A vezérlő azonosítójának megfelelően lekérte az adott vezérlőadatokat.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="6fdb0-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="6fdb0-114">Example 3</span></span>
```powershell
PS C:\> Get-AzRegulatoryComplianceControl -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2"

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplia
                     nceStandards/SOC-TSP/regulatoryComplianceControls/C1.2
Name               : C1.2
Type               : Microsoft.Security/regulatoryComplianceStandards/regulatoryComplianceControls
Description        : Confidential information within the boundaries of the system is protected against unauthorized
                     access, use, and disclosure during input, processing, retention, output, and disposition in
                     accordance with confidentiality commitments and requirements.
State              : Failed
PassedAssessments  : 177
FailedAssessments  : 22
SkippedAssessments : 0
```

<span data-ttu-id="6fdb0-115">Az erőforrás-azonosítónak megfelelően lekérte az egyes vezérlőadatokat.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="6fdb0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fdb0-116">PARAMETERS</span></span>

### <span data-ttu-id="6fdb0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdb0-117">-DefaultProfile</span></span>
<span data-ttu-id="6fdb0-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdb0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6fdb0-119">-Name</span></span>
<span data-ttu-id="6fdb0-120">Vezérlőazonosító.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-120">Control Id.</span></span>

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

### <span data-ttu-id="6fdb0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fdb0-121">-ResourceId</span></span>
<span data-ttu-id="6fdb0-122">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="6fdb0-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="6fdb0-123">-StandardName</span></span>
<span data-ttu-id="6fdb0-124">Normál név.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-124">Standard Name.</span></span>

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

### <span data-ttu-id="6fdb0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdb0-125">CommonParameters</span></span>
<span data-ttu-id="6fdb0-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdb0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdb0-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fdb0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdb0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fdb0-128">INPUTS</span></span>

### <span data-ttu-id="6fdb0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6fdb0-129">System.String</span></span>

## <span data-ttu-id="6fdb0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fdb0-130">OUTPUTS</span></span>

### <span data-ttu-id="6fdb0-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="6fdb0-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="6fdb0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6fdb0-132">NOTES</span></span>

## <span data-ttu-id="6fdb0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fdb0-133">RELATED LINKS</span></span>
