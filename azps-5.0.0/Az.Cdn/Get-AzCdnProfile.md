---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195241"
---
# <span data-ttu-id="ab5c4-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ab5c4-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="ab5c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ab5c4-103">Kap egy CDN-profilt.</span><span class="sxs-lookup"><span data-stu-id="ab5c4-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="ab5c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab5c4-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab5c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab5c4-105">DESCRIPTION</span></span>
<span data-ttu-id="ab5c4-106">A **Get-AzCdnProfile** parancsmag Azure Content Delivery Network (CDN) profilját és kapcsolódó információit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab5c4-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="ab5c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ab5c4-107">EXAMPLES</span></span>

## <span data-ttu-id="ab5c4-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab5c4-108">PARAMETERS</span></span>

### <span data-ttu-id="ab5c4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab5c4-109">-DefaultProfile</span></span>
<span data-ttu-id="ab5c4-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab5c4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab5c4-111">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="ab5c4-111">-ProfileName</span></span>
<span data-ttu-id="ab5c4-112">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab5c4-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="ab5c4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab5c4-113">-ResourceGroupName</span></span>
<span data-ttu-id="ab5c4-114">Annak az erőforrás-csoportnak a neve, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="ab5c4-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="ab5c4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab5c4-115">CommonParameters</span></span>
<span data-ttu-id="ab5c4-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab5c4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab5c4-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ab5c4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab5c4-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab5c4-118">INPUTS</span></span>

### <span data-ttu-id="ab5c4-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ab5c4-119">System.String</span></span>

## <span data-ttu-id="ab5c4-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab5c4-120">OUTPUTS</span></span>

### <span data-ttu-id="ab5c4-121">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ab5c4-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ab5c4-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab5c4-122">NOTES</span></span>

## <span data-ttu-id="ab5c4-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab5c4-123">RELATED LINKS</span></span>

[<span data-ttu-id="ab5c4-124">Új – AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ab5c4-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="ab5c4-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ab5c4-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="ab5c4-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="ab5c4-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


