---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: e81224796d8f38f15d8c3a08e5b572c8f3aab117
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014686"
---
# <span data-ttu-id="e1296-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e1296-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="e1296-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e1296-102">SYNOPSIS</span></span>
<span data-ttu-id="e1296-103">Az Azure Security Center által felfedezett biztonsági megoldásokat kapja</span><span class="sxs-lookup"><span data-stu-id="e1296-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="e1296-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e1296-104">SYNTAX</span></span>

### <span data-ttu-id="e1296-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e1296-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1296-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e1296-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1296-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1296-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1296-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="e1296-108">DESCRIPTION</span></span>
<span data-ttu-id="e1296-109">Az Azure Security Center automatikusan felismeri a biztonsági megoldásokat, ezzel a parancsmaggal megtekintheti a felfedezett biztonsági megoldásokat</span><span class="sxs-lookup"><span data-stu-id="e1296-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="e1296-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e1296-110">EXAMPLES</span></span>

### <span data-ttu-id="e1296-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e1296-111">Example 1</span></span>
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

<span data-ttu-id="e1296-112">Az előfizetés összes felfedezett biztonsági megoldásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="e1296-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="e1296-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e1296-113">Example 2</span></span>
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

<span data-ttu-id="e1296-114">Speciálisan felfedezett biztonsági megoldás beszerzése</span><span class="sxs-lookup"><span data-stu-id="e1296-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="e1296-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e1296-115">PARAMETERS</span></span>

### <span data-ttu-id="e1296-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1296-116">-DefaultProfile</span></span>
<span data-ttu-id="e1296-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e1296-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1296-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="e1296-118">-Location</span></span>
<span data-ttu-id="e1296-119">Helyre.</span><span class="sxs-lookup"><span data-stu-id="e1296-119">Location.</span></span>

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

### <span data-ttu-id="e1296-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e1296-120">-Name</span></span>
<span data-ttu-id="e1296-121">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="e1296-121">Resource name.</span></span>

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

### <span data-ttu-id="e1296-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1296-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1296-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="e1296-123">Resource group name.</span></span>

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

### <span data-ttu-id="e1296-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1296-124">-ResourceId</span></span>
<span data-ttu-id="e1296-125">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e1296-125">Resource ID.</span></span>

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

### <span data-ttu-id="e1296-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1296-126">CommonParameters</span></span>
<span data-ttu-id="e1296-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e1296-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1296-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1296-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1296-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1296-129">INPUTS</span></span>

### <span data-ttu-id="e1296-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e1296-130">System.String</span></span>

## <span data-ttu-id="e1296-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1296-131">OUTPUTS</span></span>

### <span data-ttu-id="e1296-132">Microsoft. Azure. commands. Security. models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e1296-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="e1296-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e1296-133">NOTES</span></span>

## <span data-ttu-id="e1296-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1296-134">RELATED LINKS</span></span>
