---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 3d0f93a732739b94832a5e411580fb80958b27c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492849"
---
# <span data-ttu-id="16d46-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="16d46-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="16d46-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16d46-102">SYNOPSIS</span></span>
<span data-ttu-id="16d46-103">Egy CDN-profil erőforrás-felhasználását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="16d46-103">Gets the resource usage of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16d46-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16d46-104">SYNTAX</span></span>

### <span data-ttu-id="16d46-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="16d46-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16d46-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d46-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16d46-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="16d46-107">DESCRIPTION</span></span>
<span data-ttu-id="16d46-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="16d46-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="16d46-109">Példák</span><span class="sxs-lookup"><span data-stu-id="16d46-109">EXAMPLES</span></span>

### <span data-ttu-id="16d46-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="16d46-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="16d46-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="16d46-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="16d46-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16d46-112">PARAMETERS</span></span>

### <span data-ttu-id="16d46-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="16d46-113">-CdnProfile</span></span>
<span data-ttu-id="16d46-114">Az Azure CDN-profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="16d46-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="16d46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d46-115">-DefaultProfile</span></span>
<span data-ttu-id="16d46-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="16d46-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16d46-117">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="16d46-117">-ProfileName</span></span>
<span data-ttu-id="16d46-118">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="16d46-118">The name of the profile.</span></span>

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

### <span data-ttu-id="16d46-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d46-119">-ResourceGroupName</span></span>
<span data-ttu-id="16d46-120">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="16d46-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="16d46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d46-121">CommonParameters</span></span>
<span data-ttu-id="16d46-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16d46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d46-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d46-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d46-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16d46-124">INPUTS</span></span>

### <span data-ttu-id="16d46-125">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="16d46-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="16d46-126">Paraméterek: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="16d46-126">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="16d46-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16d46-127">OUTPUTS</span></span>

### <span data-ttu-id="16d46-128">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="16d46-128">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="16d46-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16d46-129">NOTES</span></span>

## <span data-ttu-id="16d46-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16d46-130">RELATED LINKS</span></span>
