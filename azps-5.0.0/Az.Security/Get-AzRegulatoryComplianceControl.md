---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceControl.md
ms.openlocfilehash: 11c6c1073f53ba4a4b93fdae02ae6f6eb22e0f04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303335"
---
# <span data-ttu-id="4fecb-101">Get-AzRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="4fecb-101">Get-AzRegulatoryComplianceControl</span></span>

## <span data-ttu-id="4fecb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4fecb-102">SYNOPSIS</span></span>
<span data-ttu-id="4fecb-103">Szabályozási megfelelőségi vezérlők</span><span class="sxs-lookup"><span data-stu-id="4fecb-103">Gets regulatory compliance controls</span></span>

## <span data-ttu-id="4fecb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4fecb-104">SYNTAX</span></span>

### <span data-ttu-id="4fecb-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4fecb-105">SubscriptionLevelResource (Default)</span></span>
```
Get-AzRegulatoryComplianceControl [-Name <String>] -StandardName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fecb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fecb-106">ResourceId</span></span>
```
Get-AzRegulatoryComplianceControl -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fecb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4fecb-107">DESCRIPTION</span></span>
<span data-ttu-id="4fecb-108">Beszerezhet egy spcific vezérlő adatait, vagy felsorolhatja az egyes szabályozási megfelelőségi standardok szerinti vezérlőelemeket.</span><span class="sxs-lookup"><span data-stu-id="4fecb-108">Get a spcific control details or list all the controls under specific regulatory compliance standard.</span></span>

## <span data-ttu-id="4fecb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4fecb-109">EXAMPLES</span></span>

### <span data-ttu-id="4fecb-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4fecb-110">Example 1</span></span>
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

<span data-ttu-id="4fecb-111">Az egyes szabályozási szabványok szerinti összes vezérlő beolvasása</span><span class="sxs-lookup"><span data-stu-id="4fecb-111">Get all controls under specific regulatory standard.</span></span>

### <span data-ttu-id="4fecb-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4fecb-112">Example 2</span></span>
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

<span data-ttu-id="4fecb-113">Konkrét vezérlő adatok beolvasása a vezérlő azonosítójának megfelelően.</span><span class="sxs-lookup"><span data-stu-id="4fecb-113">Get specific control details according to control id.</span></span>

### <span data-ttu-id="4fecb-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="4fecb-114">Example 3</span></span>
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

<span data-ttu-id="4fecb-115">Konkrét vezérlő adatok beolvasása az erőforrás-azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="4fecb-115">Get specific control details according to resource id.</span></span>

## <span data-ttu-id="4fecb-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4fecb-116">PARAMETERS</span></span>

### <span data-ttu-id="4fecb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fecb-117">-DefaultProfile</span></span>
<span data-ttu-id="4fecb-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4fecb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fecb-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4fecb-119">-Name</span></span>
<span data-ttu-id="4fecb-120">Vezérlő azonosítója</span><span class="sxs-lookup"><span data-stu-id="4fecb-120">Control Id.</span></span>

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

### <span data-ttu-id="4fecb-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fecb-121">-ResourceId</span></span>
<span data-ttu-id="4fecb-122">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="4fecb-122">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="4fecb-123">-StandardName</span><span class="sxs-lookup"><span data-stu-id="4fecb-123">-StandardName</span></span>
<span data-ttu-id="4fecb-124">Szokásos név.</span><span class="sxs-lookup"><span data-stu-id="4fecb-124">Standard Name.</span></span>

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

### <span data-ttu-id="4fecb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fecb-125">CommonParameters</span></span>
<span data-ttu-id="4fecb-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4fecb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fecb-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4fecb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fecb-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fecb-128">INPUTS</span></span>

### <span data-ttu-id="4fecb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4fecb-129">System.String</span></span>

## <span data-ttu-id="4fecb-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4fecb-130">OUTPUTS</span></span>

### <span data-ttu-id="4fecb-131">Microsoft. Azure. Command. SecurityCenter. models. RegulatoryCompliance. PSSecurityRegulatoryComplianceControl</span><span class="sxs-lookup"><span data-stu-id="4fecb-131">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceControl</span></span>

## <span data-ttu-id="4fecb-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4fecb-132">NOTES</span></span>

## <span data-ttu-id="4fecb-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4fecb-133">RELATED LINKS</span></span>
