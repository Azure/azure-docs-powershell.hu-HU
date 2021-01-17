---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329401"
---
# <span data-ttu-id="c3a78-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="c3a78-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="c3a78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3a78-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a78-103">Hozzon létre egy Office 365-ös forgalomtörési házirendobjektumot.</span><span class="sxs-lookup"><span data-stu-id="c3a78-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="c3a78-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3a78-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3a78-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3a78-105">DESCRIPTION</span></span>
<span data-ttu-id="c3a78-106">Hozzon létre egy office 365-ös szabálytörési házirendet, amely a New-AzVpnSite és Update-AzVpnSite használható.</span><span class="sxs-lookup"><span data-stu-id="c3a78-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="c3a78-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3a78-107">EXAMPLES</span></span>

### <span data-ttu-id="c3a78-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3a78-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="c3a78-109">Hozzon létre egy office 365-ös forgalom-törési házirendet, amely lehetővé teszi a forgalom kategóriájának engedélyezett és optimalizálható törési házirendet.</span><span class="sxs-lookup"><span data-stu-id="c3a78-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="c3a78-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3a78-110">PARAMETERS</span></span>

### <span data-ttu-id="c3a78-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="c3a78-111">-Allow</span></span>
<span data-ttu-id="c3a78-112">Törd meg az engedélyezőkategória-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="c3a78-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="c3a78-113">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="c3a78-113">-Default</span></span>
<span data-ttu-id="c3a78-114">Törd meg az alapértelmezett kategóriaforgalmat.</span><span class="sxs-lookup"><span data-stu-id="c3a78-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="c3a78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3a78-115">-DefaultProfile</span></span>
<span data-ttu-id="c3a78-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3a78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3a78-117">- Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="c3a78-117">-Optimize</span></span>
<span data-ttu-id="c3a78-118">A kategória optimális forgalmának lebontása.</span><span class="sxs-lookup"><span data-stu-id="c3a78-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="c3a78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a78-119">CommonParameters</span></span>
<span data-ttu-id="c3a78-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3a78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a78-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3a78-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a78-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3a78-122">INPUTS</span></span>

### <span data-ttu-id="c3a78-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c3a78-123">None</span></span>

## <span data-ttu-id="c3a78-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3a78-124">OUTPUTS</span></span>

### <span data-ttu-id="c3a78-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="c3a78-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="c3a78-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3a78-126">NOTES</span></span>

## <span data-ttu-id="c3a78-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3a78-127">RELATED LINKS</span></span>
