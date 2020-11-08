---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 82ff7d915a7ddc2d15655513dade28fc1e7ffff0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184816"
---
# <span data-ttu-id="a9a3e-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="a9a3e-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="a9a3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a3e-103">Adjon meg egy új Office 365 forgalmi breakout-házirendet egy virtuális készülék webhelyhez való használathoz.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="a9a3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9a3e-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9a3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9a3e-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a3e-106">A New-AzOffice365PolicyProperties parancs a virtuális woith használni kívánt Office-365 breakout-házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used woith a Virtual Appliance site.</span></span> 

## <span data-ttu-id="a9a3e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a9a3e-107">EXAMPLES</span></span>

### <span data-ttu-id="a9a3e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a9a3e-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="a9a3e-109">Hozza létre az Office 365 forgalmi breakout Policy objektumát a Virtual Appliance-webhely parancsaival való használatra.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="a9a3e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9a3e-110">PARAMETERS</span></span>

### <span data-ttu-id="a9a3e-111">– Engedélyezés</span><span class="sxs-lookup"><span data-stu-id="a9a3e-111">-Allow</span></span>
<span data-ttu-id="a9a3e-112">Az engedélyezés kategória szerinti forgalom kitörése</span><span class="sxs-lookup"><span data-stu-id="a9a3e-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="a9a3e-113">– Alapértelmezett</span><span class="sxs-lookup"><span data-stu-id="a9a3e-113">-Default</span></span>
<span data-ttu-id="a9a3e-114">Az alapértelmezett kategória szerinti forgalom kitörése</span><span class="sxs-lookup"><span data-stu-id="a9a3e-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="a9a3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a3e-115">-DefaultProfile</span></span>
<span data-ttu-id="a9a3e-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9a3e-117">-Optimalizálás</span><span class="sxs-lookup"><span data-stu-id="a9a3e-117">-Optimize</span></span>
<span data-ttu-id="a9a3e-118">A kategória forgalmának optimalizálása</span><span class="sxs-lookup"><span data-stu-id="a9a3e-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="a9a3e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a3e-119">CommonParameters</span></span>
<span data-ttu-id="a9a3e-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9a3e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a3e-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a9a3e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a3e-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9a3e-122">INPUTS</span></span>

### <span data-ttu-id="a9a3e-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="a9a3e-123">None</span></span>

## <span data-ttu-id="a9a3e-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9a3e-124">OUTPUTS</span></span>

### <span data-ttu-id="a9a3e-125">Microsoft. Azure. commands. Network. models. PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="a9a3e-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="a9a3e-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9a3e-126">NOTES</span></span>

## <span data-ttu-id="a9a3e-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9a3e-127">RELATED LINKS</span></span>
