---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329374"
---
# <span data-ttu-id="607ee-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="607ee-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="607ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="607ee-102">SYNOPSIS</span></span>
<span data-ttu-id="607ee-103">Új Office 365-forgalom-törési házirend definiálva, amely a virtuális eszköz webhelyhez használható.</span><span class="sxs-lookup"><span data-stu-id="607ee-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="607ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="607ee-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="607ee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="607ee-105">DESCRIPTION</span></span>
<span data-ttu-id="607ee-106">A New-AzOffice365PolicyProperties parancs meghatároz egy, a virtuális eszköz webhelyhez használható Office 365-törési házirendet.</span><span class="sxs-lookup"><span data-stu-id="607ee-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="607ee-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="607ee-107">EXAMPLES</span></span>

### <span data-ttu-id="607ee-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="607ee-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="607ee-109">Hozza létre az Office 365-ös forgalombetörési házirendobjektumot a virtuális eszköz webhelyparancsokkal való használatra.</span><span class="sxs-lookup"><span data-stu-id="607ee-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="607ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="607ee-110">PARAMETERS</span></span>

### <span data-ttu-id="607ee-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="607ee-111">-Allow</span></span>
<span data-ttu-id="607ee-112">Törd meg az engedélyezőkategória-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="607ee-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="607ee-113">-Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="607ee-113">-Default</span></span>
<span data-ttu-id="607ee-114">Törje meg az alapértelmezett kategóriaforgalmat.</span><span class="sxs-lookup"><span data-stu-id="607ee-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="607ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="607ee-115">-DefaultProfile</span></span>
<span data-ttu-id="607ee-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="607ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="607ee-117">- Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="607ee-117">-Optimize</span></span>
<span data-ttu-id="607ee-118">A kategória optimális forgalmának lebontása.</span><span class="sxs-lookup"><span data-stu-id="607ee-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="607ee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="607ee-119">CommonParameters</span></span>
<span data-ttu-id="607ee-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="607ee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="607ee-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="607ee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="607ee-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="607ee-122">INPUTS</span></span>

### <span data-ttu-id="607ee-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="607ee-123">None</span></span>

## <span data-ttu-id="607ee-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="607ee-124">OUTPUTS</span></span>

### <span data-ttu-id="607ee-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="607ee-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="607ee-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="607ee-126">NOTES</span></span>

## <span data-ttu-id="607ee-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="607ee-127">RELATED LINKS</span></span>
