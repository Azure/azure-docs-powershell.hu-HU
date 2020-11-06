---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503251"
---
# <span data-ttu-id="4e67d-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e67d-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="4e67d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4e67d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e67d-103">Kap egy CDN-profilt.</span><span class="sxs-lookup"><span data-stu-id="4e67d-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e67d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4e67d-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e67d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4e67d-105">DESCRIPTION</span></span>
<span data-ttu-id="4e67d-106">A **Get-AzureRMCdnProfile** parancsmag Azure Content Delivery Network (CDN) profilját és kapcsolódó információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4e67d-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="4e67d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4e67d-107">EXAMPLES</span></span>

## <span data-ttu-id="4e67d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4e67d-108">PARAMETERS</span></span>

### <span data-ttu-id="4e67d-109">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="4e67d-109">-ProfileName</span></span>
<span data-ttu-id="4e67d-110">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4e67d-110">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e67d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e67d-111">-ResourceGroupName</span></span>
<span data-ttu-id="4e67d-112">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="4e67d-112">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e67d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e67d-113">-DefaultProfile</span></span>
<span data-ttu-id="4e67d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4e67d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e67d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e67d-115">CommonParameters</span></span>
<span data-ttu-id="4e67d-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4e67d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e67d-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e67d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e67d-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e67d-118">INPUTS</span></span>

## <span data-ttu-id="4e67d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4e67d-119">OUTPUTS</span></span>

###  
<span data-ttu-id="4e67d-120">Ez a parancsmag egy profil-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="4e67d-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="4e67d-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4e67d-121">NOTES</span></span>

## <span data-ttu-id="4e67d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4e67d-122">RELATED LINKS</span></span>

[<span data-ttu-id="4e67d-123">Új – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e67d-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="4e67d-124">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e67d-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="4e67d-125">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4e67d-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


