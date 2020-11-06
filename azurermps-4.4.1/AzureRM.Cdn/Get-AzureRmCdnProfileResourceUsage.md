---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505640"
---
# <span data-ttu-id="2f1aa-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="2f1aa-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="2f1aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f1aa-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1aa-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="2f1aa-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f1aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f1aa-104">SYNTAX</span></span>

### <span data-ttu-id="2f1aa-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2f1aa-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f1aa-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="2f1aa-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f1aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f1aa-107">DESCRIPTION</span></span>
<span data-ttu-id="2f1aa-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="2f1aa-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2f1aa-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2f1aa-109">EXAMPLES</span></span>

### <span data-ttu-id="2f1aa-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2f1aa-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2f1aa-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="2f1aa-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="2f1aa-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f1aa-112">PARAMETERS</span></span>

### <span data-ttu-id="2f1aa-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2f1aa-113">-CdnProfile</span></span>
<span data-ttu-id="2f1aa-114">Az Azure CDN-profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="2f1aa-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f1aa-115">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="2f1aa-115">-ProfileName</span></span>
<span data-ttu-id="2f1aa-116">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="2f1aa-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f1aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f1aa-118">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="2f1aa-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f1aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1aa-119">-DefaultProfile</span></span>
<span data-ttu-id="2f1aa-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2f1aa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f1aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1aa-121">CommonParameters</span></span>
<span data-ttu-id="2f1aa-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f1aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1aa-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1aa-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f1aa-124">INPUTS</span></span>

### <span data-ttu-id="2f1aa-125">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="2f1aa-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="2f1aa-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f1aa-126">OUTPUTS</span></span>

### <span data-ttu-id="2f1aa-127">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="2f1aa-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="2f1aa-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f1aa-128">NOTES</span></span>

## <span data-ttu-id="2f1aa-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f1aa-129">RELATED LINKS</span></span>

