---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9e48bfd243133052f526f2b9adcbef2072cdd2cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921793"
---
# <span data-ttu-id="fee69-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="fee69-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="fee69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee69-102">SYNOPSIS</span></span>
<span data-ttu-id="fee69-103">Új Office 365-forgalom-törési házirend definiálva, amely a virtuális eszköz webhelyhez használható.</span><span class="sxs-lookup"><span data-stu-id="fee69-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="fee69-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fee69-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fee69-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fee69-105">DESCRIPTION</span></span>
<span data-ttu-id="fee69-106">A New-AzOffice365PolicyProperties parancs meghatároz egy, a virtuális eszköz webhelyhez használható Office 365-törési házirendet.</span><span class="sxs-lookup"><span data-stu-id="fee69-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="fee69-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fee69-107">EXAMPLES</span></span>

### <span data-ttu-id="fee69-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="fee69-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="fee69-109">Hozza létre az Office 365-ös forgalombetörési házirendobjektumot a virtuális eszköz webhelyparancsokkal való használatra.</span><span class="sxs-lookup"><span data-stu-id="fee69-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="fee69-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee69-110">PARAMETERS</span></span>

### <span data-ttu-id="fee69-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="fee69-111">-Allow</span></span>
<span data-ttu-id="fee69-112">Törd meg az engedélyezőkategória-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="fee69-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="fee69-113">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="fee69-113">-Default</span></span>
<span data-ttu-id="fee69-114">Törje meg az alapértelmezett kategóriaforgalmat.</span><span class="sxs-lookup"><span data-stu-id="fee69-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="fee69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee69-115">-DefaultProfile</span></span>
<span data-ttu-id="fee69-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fee69-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee69-117">- Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="fee69-117">-Optimize</span></span>
<span data-ttu-id="fee69-118">A kategória optimális forgalmának lebontása.</span><span class="sxs-lookup"><span data-stu-id="fee69-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="fee69-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee69-119">CommonParameters</span></span>
<span data-ttu-id="fee69-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee69-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee69-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fee69-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee69-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fee69-122">INPUTS</span></span>

### <span data-ttu-id="fee69-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="fee69-123">None</span></span>

## <span data-ttu-id="fee69-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fee69-124">OUTPUTS</span></span>

### <span data-ttu-id="fee69-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="fee69-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="fee69-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fee69-126">NOTES</span></span>

## <span data-ttu-id="fee69-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fee69-127">RELATED LINKS</span></span>
