---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479824"
---
# <span data-ttu-id="4d80f-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="4d80f-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="4d80f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d80f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d80f-103">Az Azure Biztonsági központ által felfedezett biztonsági megoldások lekérte</span><span class="sxs-lookup"><span data-stu-id="4d80f-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="4d80f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4d80f-104">SYNTAX</span></span>

### <span data-ttu-id="4d80f-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d80f-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d80f-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="4d80f-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d80f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d80f-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d80f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4d80f-108">DESCRIPTION</span></span>
<span data-ttu-id="4d80f-109">Az Azure Biztonsági központ automatikusan felfedezi a biztonsági megoldásokat, ezzel a parancsmaggal megtekintheti a felfedezett biztonsági megoldásokat.</span><span class="sxs-lookup"><span data-stu-id="4d80f-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="4d80f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4d80f-110">EXAMPLES</span></span>

### <span data-ttu-id="4d80f-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="4d80f-111">Example 1</span></span>
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

<span data-ttu-id="4d80f-112">Az előfizetésben felfedezett összes biztonsági megoldás lekérte</span><span class="sxs-lookup"><span data-stu-id="4d80f-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="4d80f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4d80f-113">Example 2</span></span>
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

<span data-ttu-id="4d80f-114">Meghatározott felfedezett biztonsági megoldás lekérte</span><span class="sxs-lookup"><span data-stu-id="4d80f-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="4d80f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d80f-115">PARAMETERS</span></span>

### <span data-ttu-id="4d80f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d80f-116">-DefaultProfile</span></span>
<span data-ttu-id="4d80f-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d80f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d80f-118">-Location</span><span class="sxs-lookup"><span data-stu-id="4d80f-118">-Location</span></span>
<span data-ttu-id="4d80f-119">Hely.</span><span class="sxs-lookup"><span data-stu-id="4d80f-119">Location.</span></span>

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

### <span data-ttu-id="4d80f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d80f-120">-Name</span></span>
<span data-ttu-id="4d80f-121">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4d80f-121">Resource name.</span></span>

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

### <span data-ttu-id="4d80f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d80f-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d80f-123">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4d80f-123">Resource group name.</span></span>

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

### <span data-ttu-id="4d80f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d80f-124">-ResourceId</span></span>
<span data-ttu-id="4d80f-125">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4d80f-125">Resource ID.</span></span>

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

### <span data-ttu-id="4d80f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d80f-126">CommonParameters</span></span>
<span data-ttu-id="4d80f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d80f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d80f-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d80f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d80f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d80f-129">INPUTS</span></span>

### <span data-ttu-id="4d80f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4d80f-130">System.String</span></span>

## <span data-ttu-id="4d80f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d80f-131">OUTPUTS</span></span>

### <span data-ttu-id="4d80f-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="4d80f-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="4d80f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4d80f-133">NOTES</span></span>

## <span data-ttu-id="4d80f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d80f-134">RELATED LINKS</span></span>
