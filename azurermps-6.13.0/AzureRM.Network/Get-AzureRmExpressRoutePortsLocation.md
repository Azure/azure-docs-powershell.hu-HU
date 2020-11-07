---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680332"
---
# <span data-ttu-id="5cf10-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="5cf10-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="5cf10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5cf10-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf10-103">Itt érheti el azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.</span><span class="sxs-lookup"><span data-stu-id="5cf10-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cf10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5cf10-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cf10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5cf10-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf10-106">A **Get-AzureRmExpressRoutePortsLocation** parancsmag segítségével megkeresheti azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.</span><span class="sxs-lookup"><span data-stu-id="5cf10-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="5cf10-107">A parancsmag az adott helyen adja meg a kívánt helyet, a parancsmag a hely részleteit (például a rendelkezésre álló sávszélességek listáját) jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="5cf10-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="5cf10-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5cf10-108">EXAMPLES</span></span>

### <span data-ttu-id="5cf10-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5cf10-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="5cf10-110">Felsorolja azokat a helyeket, amelyeken elérhetők a ExpressRoutePort-források.</span><span class="sxs-lookup"><span data-stu-id="5cf10-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="5cf10-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="5cf10-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="5cf10-112">A hely $loc elérhető ExpressRoutePort-sávszélességek listája.</span><span class="sxs-lookup"><span data-stu-id="5cf10-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="5cf10-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5cf10-113">PARAMETERS</span></span>

### <span data-ttu-id="5cf10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf10-114">-DefaultProfile</span></span>
<span data-ttu-id="5cf10-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cf10-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf10-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="5cf10-116">-LocationName</span></span>
<span data-ttu-id="5cf10-117">A hely neve.</span><span class="sxs-lookup"><span data-stu-id="5cf10-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf10-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf10-118">CommonParameters</span></span>
<span data-ttu-id="5cf10-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5cf10-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf10-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf10-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf10-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cf10-121">INPUTS</span></span>

### <span data-ttu-id="5cf10-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf10-122">System.String</span></span>

## <span data-ttu-id="5cf10-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cf10-123">OUTPUTS</span></span>

### <span data-ttu-id="5cf10-124">Microsoft. Azure. commands. Network. models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="5cf10-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="5cf10-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5cf10-125">NOTES</span></span>

## <span data-ttu-id="5cf10-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cf10-126">RELATED LINKS</span></span>
