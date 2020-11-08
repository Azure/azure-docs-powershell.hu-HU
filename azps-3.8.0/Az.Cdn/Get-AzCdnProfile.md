---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013685"
---
# <span data-ttu-id="40904-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="40904-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="40904-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40904-102">SYNOPSIS</span></span>
<span data-ttu-id="40904-103">Kap egy CDN-profilt.</span><span class="sxs-lookup"><span data-stu-id="40904-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="40904-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40904-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40904-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40904-105">DESCRIPTION</span></span>
<span data-ttu-id="40904-106">A **Get-AzCdnProfile** parancsmag Azure Content Delivery Network (CDN) profilját és kapcsolódó információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="40904-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="40904-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40904-107">EXAMPLES</span></span>

## <span data-ttu-id="40904-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40904-108">PARAMETERS</span></span>

### <span data-ttu-id="40904-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40904-109">-DefaultProfile</span></span>
<span data-ttu-id="40904-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="40904-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40904-111">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="40904-111">-ProfileName</span></span>
<span data-ttu-id="40904-112">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40904-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="40904-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40904-113">-ResourceGroupName</span></span>
<span data-ttu-id="40904-114">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="40904-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="40904-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40904-115">CommonParameters</span></span>
<span data-ttu-id="40904-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40904-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40904-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="40904-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40904-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40904-118">INPUTS</span></span>

### <span data-ttu-id="40904-119">System. String</span><span class="sxs-lookup"><span data-stu-id="40904-119">System.String</span></span>

## <span data-ttu-id="40904-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40904-120">OUTPUTS</span></span>

### <span data-ttu-id="40904-121">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="40904-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="40904-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40904-122">NOTES</span></span>

## <span data-ttu-id="40904-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40904-123">RELATED LINKS</span></span>

[<span data-ttu-id="40904-124">Új – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="40904-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="40904-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="40904-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="40904-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="40904-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


