---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355169"
---
# <span data-ttu-id="712b2-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="712b2-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="712b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="712b2-102">SYNOPSIS</span></span>
<span data-ttu-id="712b2-103">A megfelelőségi szabványokat is megfelelteti</span><span class="sxs-lookup"><span data-stu-id="712b2-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="712b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="712b2-104">SYNTAX</span></span>

### <span data-ttu-id="712b2-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="712b2-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="712b2-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="712b2-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="712b2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="712b2-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="712b2-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="712b2-108">DESCRIPTION</span></span>
<span data-ttu-id="712b2-109">Részletes információkat olvashat a szabályozási megfelelőségről, vagy felsorolja az adott előfizetéshez szükséges összes szabályozási megfelelőségi szabványt.</span><span class="sxs-lookup"><span data-stu-id="712b2-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="712b2-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="712b2-110">EXAMPLES</span></span>

### <span data-ttu-id="712b2-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="712b2-111">Example 1</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/Azure-CIS-1.1.0
Name                : Azure-CIS-1.1.0
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 20
FailedControls      : 4
SkippedControls     : 0
UnsupportedControls : 87

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/ISO-27001
Name                : ISO-27001
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 9
FailedControls      : 10
SkippedControls     : 2
UnsupportedControls : 93

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/PCI-DSS-3.2.1
Name                : PCI-DSS-3.2.1
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 13
FailedControls      : 32
SkippedControls     : 0
UnsupportedControls : 187

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="712b2-112">Szerezze be az összes szabályozási megfelelőségi szabványt egy előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="712b2-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="712b2-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="712b2-113">Example 2</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -Name "SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="712b2-114">A szabványos névnek megfelelően lekérte az egyes szabályozási megfelelőségi szabványok részleteit.</span><span class="sxs-lookup"><span data-stu-id="712b2-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="712b2-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="712b2-115">Example 3</span></span>
```powershell
PS C:\>Get-AzRegulatoryComplianceStandard -ResourceId "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryComplianceStandards/SOC-TSP"

Id                  : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/regulatoryCompli
                      anceStandards/SOC-TSP
Name                : SOC-TSP
Type                : Microsoft.Security/regulatoryComplianceStandards
State               : Failed
PassedControls      : 2
FailedControls      : 11
SkippedControls     : 0
UnsupportedControls : 24
```

<span data-ttu-id="712b2-116">Az erőforrás-azonosítónak megfelelően részletes információkat olvashat az adott szabályozási megfelelőségi szabványról.</span><span class="sxs-lookup"><span data-stu-id="712b2-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="712b2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="712b2-117">PARAMETERS</span></span>

### <span data-ttu-id="712b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712b2-118">-DefaultProfile</span></span>
<span data-ttu-id="712b2-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="712b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="712b2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="712b2-120">-Name</span></span>
<span data-ttu-id="712b2-121">Normál név.</span><span class="sxs-lookup"><span data-stu-id="712b2-121">Standard name.</span></span>

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

### <span data-ttu-id="712b2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="712b2-122">-ResourceId</span></span>
<span data-ttu-id="712b2-123">Annak a biztonsági erőforrásnak az azonosítója, amelyről meg szeretné hívni a parancsot.</span><span class="sxs-lookup"><span data-stu-id="712b2-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="712b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712b2-124">CommonParameters</span></span>
<span data-ttu-id="712b2-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="712b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712b2-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="712b2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712b2-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="712b2-127">INPUTS</span></span>

### <span data-ttu-id="712b2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="712b2-128">System.String</span></span>

## <span data-ttu-id="712b2-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="712b2-129">OUTPUTS</span></span>

### <span data-ttu-id="712b2-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="712b2-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="712b2-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="712b2-131">NOTES</span></span>

## <span data-ttu-id="712b2-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="712b2-132">RELATED LINKS</span></span>
