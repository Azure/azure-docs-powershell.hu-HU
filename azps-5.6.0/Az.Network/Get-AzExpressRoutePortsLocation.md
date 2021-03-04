---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: d16b5d916f3a807de818c58de94f7f0841e04d17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921105"
---
# <span data-ttu-id="790c1-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="790c1-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="790c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="790c1-102">SYNOPSIS</span></span>
<span data-ttu-id="790c1-103">Beszerzheti az ExpressRoutePort-erőforrások rendelkezésre álló helyeit.</span><span class="sxs-lookup"><span data-stu-id="790c1-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="790c1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="790c1-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="790c1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="790c1-105">DESCRIPTION</span></span>
<span data-ttu-id="790c1-106">A **Get-AzExpressRoutePortsLocation** parancsmaggal lekérheti az ExpressRoutePort-erőforrások rendelkezésre álló helyeit.</span><span class="sxs-lookup"><span data-stu-id="790c1-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="790c1-107">A parancsmag adott helyet ad meg bemenetként, és megjeleníti az adott hely részleteit, azaz az adott helyen rendelkezésre álló sávszélességek listáját.</span><span class="sxs-lookup"><span data-stu-id="790c1-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="790c1-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="790c1-108">EXAMPLES</span></span>

### <span data-ttu-id="790c1-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="790c1-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="790c1-110">Felsorolja azokat a helyeket, ahol az ExpressRoutePort-erőforrások elérhetők.</span><span class="sxs-lookup"><span data-stu-id="790c1-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="790c1-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="790c1-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="790c1-112">Az Adott helyen elérhető ExpressRoutePort-sávszélességek $loc.</span><span class="sxs-lookup"><span data-stu-id="790c1-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="790c1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="790c1-113">PARAMETERS</span></span>

### <span data-ttu-id="790c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790c1-114">-DefaultProfile</span></span>
<span data-ttu-id="790c1-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="790c1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="790c1-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="790c1-116">-LocationName</span></span>
<span data-ttu-id="790c1-117">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="790c1-117">The name of the location.</span></span>

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

### <span data-ttu-id="790c1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790c1-118">CommonParameters</span></span>
<span data-ttu-id="790c1-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="790c1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790c1-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="790c1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790c1-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="790c1-121">INPUTS</span></span>

### <span data-ttu-id="790c1-122">System.String</span><span class="sxs-lookup"><span data-stu-id="790c1-122">System.String</span></span>

## <span data-ttu-id="790c1-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="790c1-123">OUTPUTS</span></span>

### <span data-ttu-id="790c1-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="790c1-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="790c1-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="790c1-125">NOTES</span></span>

## <span data-ttu-id="790c1-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="790c1-126">RELATED LINKS</span></span>
