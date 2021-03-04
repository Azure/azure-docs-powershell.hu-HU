---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 1a4e3f08653f6c7bda799b55618caff4e77fe7bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004582"
---
# <span data-ttu-id="4429d-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="4429d-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="4429d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4429d-102">SYNOPSIS</span></span>
<span data-ttu-id="4429d-103">Egy CDN-profil erőforrás-használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4429d-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="4429d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4429d-104">SYNTAX</span></span>

### <span data-ttu-id="4429d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4429d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4429d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4429d-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4429d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4429d-107">DESCRIPTION</span></span>
<span data-ttu-id="4429d-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="4429d-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4429d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4429d-109">EXAMPLES</span></span>

### <span data-ttu-id="4429d-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4429d-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4429d-111">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="4429d-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="4429d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4429d-112">PARAMETERS</span></span>

### <span data-ttu-id="4429d-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4429d-113">-CdnProfile</span></span>
<span data-ttu-id="4429d-114">Az Azure CDN-profilobjektum.</span><span class="sxs-lookup"><span data-stu-id="4429d-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="4429d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4429d-115">-DefaultProfile</span></span>
<span data-ttu-id="4429d-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4429d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4429d-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4429d-117">-ProfileName</span></span>
<span data-ttu-id="4429d-118">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="4429d-118">The name of the profile.</span></span>

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

### <span data-ttu-id="4429d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4429d-119">-ResourceGroupName</span></span>
<span data-ttu-id="4429d-120">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="4429d-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="4429d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4429d-121">CommonParameters</span></span>
<span data-ttu-id="4429d-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4429d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4429d-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4429d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4429d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4429d-124">INPUTS</span></span>

### <span data-ttu-id="4429d-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="4429d-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4429d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4429d-126">OUTPUTS</span></span>

### <span data-ttu-id="4429d-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="4429d-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="4429d-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4429d-128">NOTES</span></span>

## <span data-ttu-id="4429d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4429d-129">RELATED LINKS</span></span>
