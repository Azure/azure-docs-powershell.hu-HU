---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: d33cc54102d06b3bd57784880280b6e035fce18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671411"
---
# <span data-ttu-id="38a75-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="38a75-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="38a75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38a75-102">SYNOPSIS</span></span>
<span data-ttu-id="38a75-103">Egy CDN-profil erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="38a75-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="38a75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38a75-104">SYNTAX</span></span>

### <span data-ttu-id="38a75-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38a75-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a75-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38a75-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38a75-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="38a75-107">DESCRIPTION</span></span>
<span data-ttu-id="38a75-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="38a75-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="38a75-109">Példák</span><span class="sxs-lookup"><span data-stu-id="38a75-109">EXAMPLES</span></span>

### <span data-ttu-id="38a75-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="38a75-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="38a75-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="38a75-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="38a75-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38a75-112">PARAMETERS</span></span>

### <span data-ttu-id="38a75-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="38a75-113">-CdnProfile</span></span>
<span data-ttu-id="38a75-114">Az Azure CDN-profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="38a75-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38a75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a75-115">-DefaultProfile</span></span>
<span data-ttu-id="38a75-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38a75-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38a75-117">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="38a75-117">-ProfileName</span></span>
<span data-ttu-id="38a75-118">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="38a75-118">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a75-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38a75-119">-ResourceGroupName</span></span>
<span data-ttu-id="38a75-120">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="38a75-120">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38a75-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a75-121">CommonParameters</span></span>
<span data-ttu-id="38a75-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38a75-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a75-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38a75-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a75-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38a75-124">INPUTS</span></span>

### <span data-ttu-id="38a75-125">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="38a75-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="38a75-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38a75-126">OUTPUTS</span></span>

### <span data-ttu-id="38a75-127">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="38a75-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="38a75-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38a75-128">NOTES</span></span>

## <span data-ttu-id="38a75-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38a75-129">RELATED LINKS</span></span>
