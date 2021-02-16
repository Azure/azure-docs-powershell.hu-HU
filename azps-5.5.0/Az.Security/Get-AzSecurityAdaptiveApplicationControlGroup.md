---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158451"
---
# <span data-ttu-id="a9cf1-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="a9cf1-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="a9cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="a9cf1-103">Alkalmazásvezérlő VM/kiszolgálócsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="a9cf1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9cf1-104">SYNTAX</span></span>

### <span data-ttu-id="a9cf1-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9cf1-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9cf1-106">DESCRIPTION</span></span>
<span data-ttu-id="a9cf1-107">Az adaptív alkalmazásvezérlőket az Azure Biztonsági központ automatikusan kiszámítja. Ezzel a parancsmaggal lekérő alkalmazásvezérlő VM-/kiszolgálócsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="a9cf1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9cf1-108">EXAMPLES</span></span>

### <span data-ttu-id="a9cf1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="a9cf1-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="a9cf1-110">Alkalmazásvezérlő VM/kiszolgálócsoportot kap.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="a9cf1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9cf1-111">PARAMETERS</span></span>

### <span data-ttu-id="a9cf1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9cf1-112">-DefaultProfile</span></span>
<span data-ttu-id="a9cf1-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9cf1-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="a9cf1-114">-AscLocation</span></span>
<span data-ttu-id="a9cf1-115">Az a hely, ahol az ASC tárolja az előfizetés adatait.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="a9cf1-116">lekérhető a Helyek lekérése helyről.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9cf1-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a9cf1-117">-GroupName</span></span>
<span data-ttu-id="a9cf1-118">Egy alkalmazásvezérlő VM/kiszolgálócsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9cf1-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9cf1-119">-SubscriptionId</span></span>
<span data-ttu-id="a9cf1-120">Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="a9cf1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9cf1-121">CommonParameters</span></span>
<span data-ttu-id="a9cf1-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9cf1-123">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9cf1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9cf1-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9cf1-124">INPUTS</span></span>

### <span data-ttu-id="a9cf1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a9cf1-125">System.String</span></span>

## <span data-ttu-id="a9cf1-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9cf1-126">OUTPUTS</span></span>

### <span data-ttu-id="a9cf1-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="a9cf1-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="a9cf1-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9cf1-128">NOTES</span></span>

## <span data-ttu-id="a9cf1-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9cf1-129">RELATED LINKS</span></span>