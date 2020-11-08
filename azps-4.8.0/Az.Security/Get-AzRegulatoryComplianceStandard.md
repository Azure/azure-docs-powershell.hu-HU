---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzRegulatoryComplianceStandard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzRegulatoryComplianceStandard.md
ms.openlocfilehash: a554a0adcdf8692f054becb5891cdd0c20203911
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183987"
---
# <span data-ttu-id="35398-101">Get-AzRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="35398-101">Get-AzRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="35398-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35398-102">SYNOPSIS</span></span>
<span data-ttu-id="35398-103">Megkapja a regulatoey megfelelőségi normáit</span><span class="sxs-lookup"><span data-stu-id="35398-103">Gets regulatoey compliance standards</span></span>

## <span data-ttu-id="35398-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35398-104">SYNTAX</span></span>

### <span data-ttu-id="35398-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35398-105">SubscriptionScope (Default)</span></span>
```
Get-AzRegulatoryComplianceStandard [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35398-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="35398-106">SubscriptionLevelResource</span></span>
```
Get-AzRegulatoryComplianceStandard -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35398-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="35398-107">ResourceId</span></span>
```
Get-AzRegulatoryComplianceStandard -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35398-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="35398-108">DESCRIPTION</span></span>
<span data-ttu-id="35398-109">Megtudhatja, hogy spcific-e a szabályok megfelelőségi satandard, vagy felsorolhatja az egyes előfizetések szerinti megfelelőségi szabványokat.</span><span class="sxs-lookup"><span data-stu-id="35398-109">Get a spcific regulatory compliance satandard details or list all regulatory compliance standards under specific subscription.</span></span>

## <span data-ttu-id="35398-110">Példák</span><span class="sxs-lookup"><span data-stu-id="35398-110">EXAMPLES</span></span>

### <span data-ttu-id="35398-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35398-111">Example 1</span></span>
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

<span data-ttu-id="35398-112">Az előfizetésben szereplő minden szabályozási megfelelőségi szabvány beszerzése.</span><span class="sxs-lookup"><span data-stu-id="35398-112">Get all regulatory compliance standards under a subscription.</span></span>

### <span data-ttu-id="35398-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="35398-113">Example 2</span></span>
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

<span data-ttu-id="35398-114">Az egyes szabályozási megfelelőségi szabványokat a szokásos név szerint részletezve érheti el.</span><span class="sxs-lookup"><span data-stu-id="35398-114">Get details of specific regulatory compliance standard according standard name.</span></span>

### <span data-ttu-id="35398-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="35398-115">Example 3</span></span>
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

<span data-ttu-id="35398-116">Az erőforrás-azonosító szerint meghatározott szabályozási megfelelőségi standardokat tudhat meg.</span><span class="sxs-lookup"><span data-stu-id="35398-116">Get details of specific regulatory compliance standard according resource id.</span></span>

## <span data-ttu-id="35398-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35398-117">PARAMETERS</span></span>

### <span data-ttu-id="35398-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35398-118">-DefaultProfile</span></span>
<span data-ttu-id="35398-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35398-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35398-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35398-120">-Name</span></span>
<span data-ttu-id="35398-121">Szokásos név.</span><span class="sxs-lookup"><span data-stu-id="35398-121">Standard name.</span></span>

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

### <span data-ttu-id="35398-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35398-122">-ResourceId</span></span>
<span data-ttu-id="35398-123">Annak a biztonsági erőforrásnak az azonosítója, amelyre a parancsot be szeretné hívni.</span><span class="sxs-lookup"><span data-stu-id="35398-123">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="35398-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35398-124">CommonParameters</span></span>
<span data-ttu-id="35398-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35398-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35398-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="35398-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35398-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35398-127">INPUTS</span></span>

### <span data-ttu-id="35398-128">System. String</span><span class="sxs-lookup"><span data-stu-id="35398-128">System.String</span></span>

## <span data-ttu-id="35398-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35398-129">OUTPUTS</span></span>

### <span data-ttu-id="35398-130">Microsoft. Azure. Command. SecurityCenter. models. RegulatoryCompliance. PSSecurityRegulatoryComplianceStandard</span><span class="sxs-lookup"><span data-stu-id="35398-130">Microsoft.Azure.Commands.SecurityCenter.Models.RegulatoryCompliance.PSSecurityRegulatoryComplianceStandard</span></span>

## <span data-ttu-id="35398-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35398-131">NOTES</span></span>

## <span data-ttu-id="35398-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35398-132">RELATED LINKS</span></span>
