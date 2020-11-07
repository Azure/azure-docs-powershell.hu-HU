---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d5fca22bf289c42681d9af18a9eaff28587f1922
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838848"
---
# <span data-ttu-id="3139f-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3139f-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="3139f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3139f-102">SYNOPSIS</span></span>
<span data-ttu-id="3139f-103">Az Azure Security Center által felfedezett biztonsági megoldásokat kapja</span><span class="sxs-lookup"><span data-stu-id="3139f-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="3139f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3139f-104">SYNTAX</span></span>

### <span data-ttu-id="3139f-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3139f-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3139f-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="3139f-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3139f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3139f-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3139f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3139f-108">DESCRIPTION</span></span>
<span data-ttu-id="3139f-109">Az Azure Security Center automatikusan felismeri a biztonsági megoldásokat, ezzel a parancsmaggal megtekintheti a felfedezett biztonsági megoldásokat</span><span class="sxs-lookup"><span data-stu-id="3139f-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="3139f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3139f-110">EXAMPLES</span></span>

### <span data-ttu-id="3139f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3139f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="3139f-112">Az előfizetés összes felfedezett biztonsági megoldásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="3139f-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="3139f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3139f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="3139f-114">Speciálisan felfedezett biztonsági megoldás beszerzése</span><span class="sxs-lookup"><span data-stu-id="3139f-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="3139f-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3139f-115">PARAMETERS</span></span>

### <span data-ttu-id="3139f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3139f-116">-DefaultProfile</span></span>
<span data-ttu-id="3139f-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3139f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3139f-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="3139f-118">-Location</span></span>
<span data-ttu-id="3139f-119">Helyre.</span><span class="sxs-lookup"><span data-stu-id="3139f-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3139f-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3139f-120">-Name</span></span>
<span data-ttu-id="3139f-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="3139f-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3139f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3139f-122">-ResourceGroupName</span></span>
<span data-ttu-id="3139f-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="3139f-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3139f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3139f-124">-ResourceId</span></span>
<span data-ttu-id="3139f-125">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="3139f-125">Resource ID.</span></span>

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

### <span data-ttu-id="3139f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3139f-126">CommonParameters</span></span>
<span data-ttu-id="3139f-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3139f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3139f-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3139f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3139f-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3139f-129">INPUTS</span></span>

### <span data-ttu-id="3139f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3139f-130">System.String</span></span>

## <span data-ttu-id="3139f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3139f-131">OUTPUTS</span></span>

### <span data-ttu-id="3139f-132">Microsoft. Azure. commands. Security. models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="3139f-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="3139f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3139f-133">NOTES</span></span>

## <span data-ttu-id="3139f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3139f-134">RELATED LINKS</span></span>
