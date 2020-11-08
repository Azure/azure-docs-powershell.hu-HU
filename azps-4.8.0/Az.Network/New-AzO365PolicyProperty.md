---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184818"
---
# <span data-ttu-id="59106-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="59106-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="59106-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59106-102">SYNOPSIS</span></span>
<span data-ttu-id="59106-103">Hozza létre az Office 365 forgalmi breakout Policy objektumát.</span><span class="sxs-lookup"><span data-stu-id="59106-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="59106-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59106-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59106-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59106-105">DESCRIPTION</span></span>
<span data-ttu-id="59106-106">A New-AzVpnSite és Update-AzVpnSite parancsmagokkal használható Office 365 breakout-házirend létrehozása</span><span class="sxs-lookup"><span data-stu-id="59106-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="59106-107">Példák</span><span class="sxs-lookup"><span data-stu-id="59106-107">EXAMPLES</span></span>

### <span data-ttu-id="59106-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="59106-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="59106-109">Az Office 365 forgalmi breakout házirendjét létrehozhatja a forgalom engedélyezéséhez és optimalizálásához használható breakout-házirendet.</span><span class="sxs-lookup"><span data-stu-id="59106-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="59106-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59106-110">PARAMETERS</span></span>

### <span data-ttu-id="59106-111">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="59106-111">-Allow</span></span>
<span data-ttu-id="59106-112">Az engedélyezés kategória szerinti forgalom kitörése</span><span class="sxs-lookup"><span data-stu-id="59106-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="59106-113">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="59106-113">-Default</span></span>
<span data-ttu-id="59106-114">Az alapértelmezett kategória szerinti forgalom kitörése</span><span class="sxs-lookup"><span data-stu-id="59106-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="59106-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59106-115">-DefaultProfile</span></span>
<span data-ttu-id="59106-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59106-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59106-117">-Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="59106-117">-Optimize</span></span>
<span data-ttu-id="59106-118">A kategória forgalmának optimalizálása</span><span class="sxs-lookup"><span data-stu-id="59106-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="59106-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59106-119">CommonParameters</span></span>
<span data-ttu-id="59106-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59106-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59106-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59106-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59106-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59106-122">INPUTS</span></span>

### <span data-ttu-id="59106-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="59106-123">None</span></span>

## <span data-ttu-id="59106-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59106-124">OUTPUTS</span></span>

### <span data-ttu-id="59106-125">Microsoft. Azure. commands. Network. models. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="59106-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="59106-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59106-126">NOTES</span></span>

## <span data-ttu-id="59106-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59106-127">RELATED LINKS</span></span>