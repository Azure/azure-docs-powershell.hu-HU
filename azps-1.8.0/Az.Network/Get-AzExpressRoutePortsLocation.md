---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670570"
---
# <span data-ttu-id="dda69-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="dda69-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="dda69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dda69-102">SYNOPSIS</span></span>
<span data-ttu-id="dda69-103">Itt érheti el azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.</span><span class="sxs-lookup"><span data-stu-id="dda69-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="dda69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dda69-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dda69-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dda69-105">DESCRIPTION</span></span>
<span data-ttu-id="dda69-106">A **Get-AzExpressRoutePortsLocation** parancsmag segítségével megkeresheti azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.</span><span class="sxs-lookup"><span data-stu-id="dda69-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="dda69-107">A parancsmag az adott helyen adja meg a kívánt helyet, a parancsmag a hely részleteit (például a rendelkezésre álló sávszélességek listáját) jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="dda69-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="dda69-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dda69-108">EXAMPLES</span></span>

### <span data-ttu-id="dda69-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dda69-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="dda69-110">Felsorolja azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.</span><span class="sxs-lookup"><span data-stu-id="dda69-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="dda69-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="dda69-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="dda69-112">A hely $loc elérhető ExpressRoutePort-sávszélességek listája.</span><span class="sxs-lookup"><span data-stu-id="dda69-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="dda69-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dda69-113">PARAMETERS</span></span>

### <span data-ttu-id="dda69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda69-114">-DefaultProfile</span></span>
<span data-ttu-id="dda69-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dda69-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda69-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="dda69-116">-LocationName</span></span>
<span data-ttu-id="dda69-117">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="dda69-117">The name of the location.</span></span>

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

### <span data-ttu-id="dda69-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda69-118">CommonParameters</span></span>
<span data-ttu-id="dda69-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dda69-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda69-120">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dda69-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda69-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dda69-121">INPUTS</span></span>

### <span data-ttu-id="dda69-122">System. String</span><span class="sxs-lookup"><span data-stu-id="dda69-122">System.String</span></span>

## <span data-ttu-id="dda69-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dda69-123">OUTPUTS</span></span>

### <span data-ttu-id="dda69-124">Microsoft. Azure. commands. Network. models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="dda69-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="dda69-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dda69-125">NOTES</span></span>

## <span data-ttu-id="dda69-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dda69-126">RELATED LINKS</span></span>
