---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195239"
---
# <span data-ttu-id="ae99b-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ae99b-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="ae99b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae99b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae99b-103">Egy CDN-profil erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae99b-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="ae99b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae99b-104">SYNTAX</span></span>

### <span data-ttu-id="ae99b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae99b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae99b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae99b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae99b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae99b-107">DESCRIPTION</span></span>
<span data-ttu-id="ae99b-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="ae99b-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ae99b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae99b-109">EXAMPLES</span></span>

### <span data-ttu-id="ae99b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ae99b-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ae99b-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="ae99b-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ae99b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae99b-112">PARAMETERS</span></span>

### <span data-ttu-id="ae99b-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ae99b-113">-CdnProfile</span></span>
<span data-ttu-id="ae99b-114">Az Azure CDN-profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="ae99b-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="ae99b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae99b-115">-DefaultProfile</span></span>
<span data-ttu-id="ae99b-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae99b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae99b-117">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="ae99b-117">-ProfileName</span></span>
<span data-ttu-id="ae99b-118">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="ae99b-118">The name of the profile.</span></span>

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

### <span data-ttu-id="ae99b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae99b-119">-ResourceGroupName</span></span>
<span data-ttu-id="ae99b-120">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="ae99b-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="ae99b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae99b-121">CommonParameters</span></span>
<span data-ttu-id="ae99b-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae99b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae99b-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ae99b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae99b-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae99b-124">INPUTS</span></span>

### <span data-ttu-id="ae99b-125">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ae99b-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ae99b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae99b-126">OUTPUTS</span></span>

### <span data-ttu-id="ae99b-127">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ae99b-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="ae99b-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae99b-128">NOTES</span></span>

## <span data-ttu-id="ae99b-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae99b-129">RELATED LINKS</span></span>
