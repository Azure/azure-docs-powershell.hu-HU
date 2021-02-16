---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160827"
---
# <span data-ttu-id="36430-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="36430-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="36430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36430-102">SYNOPSIS</span></span>
<span data-ttu-id="36430-103">Hozzon létre egy Office 365-ös forgalomtörési házirendobjektumot.</span><span class="sxs-lookup"><span data-stu-id="36430-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="36430-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36430-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36430-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36430-105">DESCRIPTION</span></span>
<span data-ttu-id="36430-106">Hozzon létre egy office 365-ös szabálytörési házirendet, amely a New-AzVpnSite és Update-AzVpnSite használható.</span><span class="sxs-lookup"><span data-stu-id="36430-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="36430-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36430-107">EXAMPLES</span></span>

### <span data-ttu-id="36430-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="36430-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="36430-109">Hozzon létre egy office 365-ös forgalom-törési házirendet, amely lehetővé teszi az adatforgalom engedélyezett és optimalizálható kategóriáját.</span><span class="sxs-lookup"><span data-stu-id="36430-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="36430-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36430-110">PARAMETERS</span></span>

### <span data-ttu-id="36430-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="36430-111">-Allow</span></span>
<span data-ttu-id="36430-112">Törd meg az engedélyezőkategória-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="36430-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36430-113">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="36430-113">-Default</span></span>
<span data-ttu-id="36430-114">Törd meg az alapértelmezett kategóriaforgalmat.</span><span class="sxs-lookup"><span data-stu-id="36430-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36430-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36430-115">-DefaultProfile</span></span>
<span data-ttu-id="36430-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36430-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36430-117">- Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="36430-117">-Optimize</span></span>
<span data-ttu-id="36430-118">A kategória optimális forgalmának lebontása.</span><span class="sxs-lookup"><span data-stu-id="36430-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36430-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36430-119">CommonParameters</span></span>
<span data-ttu-id="36430-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36430-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36430-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36430-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36430-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36430-122">INPUTS</span></span>

### <span data-ttu-id="36430-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="36430-123">None</span></span>

## <span data-ttu-id="36430-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36430-124">OUTPUTS</span></span>

### <span data-ttu-id="36430-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="36430-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="36430-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36430-126">NOTES</span></span>

## <span data-ttu-id="36430-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36430-127">RELATED LINKS</span></span>
