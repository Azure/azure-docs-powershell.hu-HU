---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337493"
---
# <span data-ttu-id="4f929-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="4f929-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="4f929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f929-102">SYNOPSIS</span></span>
<span data-ttu-id="4f929-103">Az Azure Biztonsági központ által felfedezett biztonsági megoldások lekérte</span><span class="sxs-lookup"><span data-stu-id="4f929-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="4f929-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4f929-104">SYNTAX</span></span>

### <span data-ttu-id="4f929-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f929-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f929-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="4f929-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f929-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f929-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f929-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4f929-108">DESCRIPTION</span></span>
<span data-ttu-id="4f929-109">Az Azure Biztonsági központ automatikusan felfedezi a biztonsági megoldásokat, ezzel a parancsmaggal megtekintheti a felfedezett biztonsági megoldásokat.</span><span class="sxs-lookup"><span data-stu-id="4f929-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="4f929-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4f929-110">EXAMPLES</span></span>

### <span data-ttu-id="4f929-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4f929-111">Example 1</span></span>
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

<span data-ttu-id="4f929-112">Az előfizetésben felfedezett összes biztonsági megoldás lekérte</span><span class="sxs-lookup"><span data-stu-id="4f929-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="4f929-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4f929-113">Example 2</span></span>
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

<span data-ttu-id="4f929-114">Meghatározott felfedezett biztonsági megoldás lekérte</span><span class="sxs-lookup"><span data-stu-id="4f929-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="4f929-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f929-115">PARAMETERS</span></span>

### <span data-ttu-id="4f929-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f929-116">-DefaultProfile</span></span>
<span data-ttu-id="4f929-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f929-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f929-118">-Location</span><span class="sxs-lookup"><span data-stu-id="4f929-118">-Location</span></span>
<span data-ttu-id="4f929-119">Hely.</span><span class="sxs-lookup"><span data-stu-id="4f929-119">Location.</span></span>

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

### <span data-ttu-id="4f929-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4f929-120">-Name</span></span>
<span data-ttu-id="4f929-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4f929-121">Resource name.</span></span>

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

### <span data-ttu-id="4f929-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f929-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f929-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4f929-123">Resource group name.</span></span>

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

### <span data-ttu-id="4f929-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f929-124">-ResourceId</span></span>
<span data-ttu-id="4f929-125">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4f929-125">Resource ID.</span></span>

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

### <span data-ttu-id="4f929-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f929-126">CommonParameters</span></span>
<span data-ttu-id="4f929-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f929-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f929-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f929-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f929-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f929-129">INPUTS</span></span>

### <span data-ttu-id="4f929-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4f929-130">System.String</span></span>

## <span data-ttu-id="4f929-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f929-131">OUTPUTS</span></span>

### <span data-ttu-id="4f929-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="4f929-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="4f929-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4f929-133">NOTES</span></span>

## <span data-ttu-id="4f929-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f929-134">RELATED LINKS</span></span>
