---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 6cc9b19f892ed15caf675b22935328354fa47dcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503872"
---
# <span data-ttu-id="b2947-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="b2947-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="b2947-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2947-102">SYNOPSIS</span></span>
<span data-ttu-id="b2947-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="b2947-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2947-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2947-104">SYNTAX</span></span>

### <span data-ttu-id="b2947-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2947-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2947-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2947-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2947-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2947-107">DESCRIPTION</span></span>
<span data-ttu-id="b2947-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="b2947-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="b2947-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2947-109">EXAMPLES</span></span>

### <span data-ttu-id="b2947-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b2947-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b2947-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="b2947-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="b2947-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2947-112">PARAMETERS</span></span>

### <span data-ttu-id="b2947-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b2947-113">-CdnProfile</span></span>
<span data-ttu-id="b2947-114">Az Azure CDN-profil objektuma.</span><span class="sxs-lookup"><span data-stu-id="b2947-114">The Azure CDN profile object.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2947-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2947-115">-DefaultProfile</span></span>
<span data-ttu-id="b2947-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2947-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2947-117">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="b2947-117">-ProfileName</span></span>
<span data-ttu-id="b2947-118">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="b2947-118">The name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2947-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2947-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2947-120">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="b2947-120">The resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2947-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2947-121">CommonParameters</span></span>
<span data-ttu-id="b2947-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2947-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2947-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2947-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2947-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2947-124">INPUTS</span></span>

### <span data-ttu-id="b2947-125">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b2947-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b2947-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2947-126">OUTPUTS</span></span>

### <span data-ttu-id="b2947-127">Microsoft. Azure. Command. CDN. models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="b2947-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="b2947-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2947-128">NOTES</span></span>

## <span data-ttu-id="b2947-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2947-129">RELATED LINKS</span></span>

