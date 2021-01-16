---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327385"
---
# <span data-ttu-id="53934-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="53934-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="53934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53934-102">SYNOPSIS</span></span>
<span data-ttu-id="53934-103">Egy CDN-profil erőforrás-használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="53934-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="53934-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="53934-104">SYNTAX</span></span>

### <span data-ttu-id="53934-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53934-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53934-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53934-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53934-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="53934-107">DESCRIPTION</span></span>
<span data-ttu-id="53934-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="53934-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="53934-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="53934-109">EXAMPLES</span></span>

### <span data-ttu-id="53934-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="53934-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="53934-111">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="53934-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="53934-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53934-112">PARAMETERS</span></span>

### <span data-ttu-id="53934-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="53934-113">-CdnProfile</span></span>
<span data-ttu-id="53934-114">Az Azure CDN-profilobjektum.</span><span class="sxs-lookup"><span data-stu-id="53934-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="53934-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53934-115">-DefaultProfile</span></span>
<span data-ttu-id="53934-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="53934-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53934-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="53934-117">-ProfileName</span></span>
<span data-ttu-id="53934-118">A profil neve.</span><span class="sxs-lookup"><span data-stu-id="53934-118">The name of the profile.</span></span>

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

### <span data-ttu-id="53934-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53934-119">-ResourceGroupName</span></span>
<span data-ttu-id="53934-120">Az az erőforráscsoport, amelyhez a profil tartozik.</span><span class="sxs-lookup"><span data-stu-id="53934-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="53934-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53934-121">CommonParameters</span></span>
<span data-ttu-id="53934-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53934-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53934-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53934-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53934-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53934-124">INPUTS</span></span>

### <span data-ttu-id="53934-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="53934-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="53934-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53934-126">OUTPUTS</span></span>

### <span data-ttu-id="53934-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="53934-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="53934-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="53934-128">NOTES</span></span>

## <span data-ttu-id="53934-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53934-129">RELATED LINKS</span></span>
