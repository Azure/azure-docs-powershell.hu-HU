---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityLocation.md
ms.openlocfilehash: 034681ad8ce4fbd30b10b959eda024f1a375c366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492739"
---
# <span data-ttu-id="d4732-101">Get-AzureRmSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="d4732-101">Get-AzureRmSecurityLocation</span></span>

## <span data-ttu-id="d4732-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4732-102">SYNOPSIS</span></span>
<span data-ttu-id="d4732-103">Annak a helynek a helye, ahol az Azure Security Center automatikusan menti az adott előfizetéshez tartozó adatot</span><span class="sxs-lookup"><span data-stu-id="d4732-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4732-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4732-104">SYNTAX</span></span>

### <span data-ttu-id="d4732-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4732-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4732-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d4732-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4732-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4732-107">ResourceId</span></span>
```
Get-AzureRmSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4732-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4732-108">DESCRIPTION</span></span>
<span data-ttu-id="d4732-109">Az Azure Security Center automatikusan úgy dönt, hogy egy helyre menti az adatait.</span><span class="sxs-lookup"><span data-stu-id="d4732-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="d4732-110">Ezzel a parancsmaggal felfedezheti ezt a helyet.</span><span class="sxs-lookup"><span data-stu-id="d4732-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="d4732-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d4732-111">EXAMPLES</span></span>

### <span data-ttu-id="d4732-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d4732-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="d4732-113">Megkapja azt a helyet, ahol az Azure Security Center menti a számított biztonsági adatmennyiséget.</span><span class="sxs-lookup"><span data-stu-id="d4732-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="d4732-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4732-114">PARAMETERS</span></span>

### <span data-ttu-id="d4732-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4732-115">-DefaultProfile</span></span>
<span data-ttu-id="d4732-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4732-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4732-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d4732-117">-Name</span></span>
<span data-ttu-id="d4732-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="d4732-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4732-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4732-119">-ResourceId</span></span>
<span data-ttu-id="d4732-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="d4732-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4732-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4732-121">CommonParameters</span></span>
<span data-ttu-id="d4732-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4732-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4732-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4732-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4732-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4732-124">INPUTS</span></span>

### <span data-ttu-id="d4732-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d4732-125">System.String</span></span>

## <span data-ttu-id="d4732-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4732-126">OUTPUTS</span></span>

### <span data-ttu-id="d4732-127">Microsoft. Azure. commands. Security. models. Locations. PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="d4732-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="d4732-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4732-128">NOTES</span></span>

## <span data-ttu-id="d4732-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4732-129">RELATED LINKS</span></span>
