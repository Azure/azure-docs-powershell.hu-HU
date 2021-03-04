---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: a2b3a4878db022018bd0fae1d8e43e3700dd5e35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921794"
---
# <span data-ttu-id="c45ce-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="c45ce-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="c45ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c45ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c45ce-103">Hozzon létre egy Office 365-ös forgalomtörési házirendobjektumot.</span><span class="sxs-lookup"><span data-stu-id="c45ce-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="c45ce-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c45ce-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c45ce-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c45ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c45ce-106">Hozzon létre egy office 365-ös szabálytörési házirendet, amely a New-AzVpnSite és Update-AzVpnSite használható.</span><span class="sxs-lookup"><span data-stu-id="c45ce-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="c45ce-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c45ce-107">EXAMPLES</span></span>

### <span data-ttu-id="c45ce-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c45ce-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="c45ce-109">Hozzon létre egy office 365-ös forgalom-törési házirendet, amely lehetővé teszi az adatforgalom engedélyezett és optimalizálható kategóriáját.</span><span class="sxs-lookup"><span data-stu-id="c45ce-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="c45ce-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c45ce-110">PARAMETERS</span></span>

### <span data-ttu-id="c45ce-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="c45ce-111">-Allow</span></span>
<span data-ttu-id="c45ce-112">Törd meg az engedélyezőkategória-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="c45ce-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="c45ce-113">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="c45ce-113">-Default</span></span>
<span data-ttu-id="c45ce-114">Törje meg az alapértelmezett kategóriaforgalmat.</span><span class="sxs-lookup"><span data-stu-id="c45ce-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="c45ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c45ce-115">-DefaultProfile</span></span>
<span data-ttu-id="c45ce-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c45ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c45ce-117">- Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="c45ce-117">-Optimize</span></span>
<span data-ttu-id="c45ce-118">A kategória optimális forgalmának lebontása.</span><span class="sxs-lookup"><span data-stu-id="c45ce-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="c45ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c45ce-119">CommonParameters</span></span>
<span data-ttu-id="c45ce-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c45ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c45ce-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c45ce-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c45ce-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c45ce-122">INPUTS</span></span>

### <span data-ttu-id="c45ce-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c45ce-123">None</span></span>

## <span data-ttu-id="c45ce-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c45ce-124">OUTPUTS</span></span>

### <span data-ttu-id="c45ce-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="c45ce-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="c45ce-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c45ce-126">NOTES</span></span>

## <span data-ttu-id="c45ce-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c45ce-127">RELATED LINKS</span></span>
