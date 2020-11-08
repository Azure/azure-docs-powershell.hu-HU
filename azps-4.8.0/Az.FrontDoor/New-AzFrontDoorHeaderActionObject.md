---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184945"
---
# <span data-ttu-id="c9d43-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="c9d43-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="c9d43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9d43-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d43-103">PSHeaderAction objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="c9d43-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="c9d43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9d43-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9d43-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d43-106">Létrehozza a PSHeaderAction objektumot az PSRulesEngineAction objektum létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="c9d43-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="c9d43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9d43-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d43-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c9d43-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="c9d43-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9d43-109">PARAMETERS</span></span>

### <span data-ttu-id="c9d43-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d43-110">-DefaultProfile</span></span>
<span data-ttu-id="c9d43-111">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9d43-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9d43-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="c9d43-112">-HeaderActionType</span></span>
<span data-ttu-id="c9d43-113">Milyen típusú manipulációt kell alkalmazni a fejlécre.</span><span class="sxs-lookup"><span data-stu-id="c9d43-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d43-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c9d43-114">-HeaderName</span></span>
<span data-ttu-id="c9d43-115">Annak a fejlécnek a neve, amelyet a művelet alkalmazni fog.</span><span class="sxs-lookup"><span data-stu-id="c9d43-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d43-116">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="c9d43-116">-Value</span></span>
<span data-ttu-id="c9d43-117">Az az érték, amellyel frissítheti a megadott fejléc nevét.</span><span class="sxs-lookup"><span data-stu-id="c9d43-117">The value to update the given header name with.</span></span>
<span data-ttu-id="c9d43-118">Ezt az értéket a program nem használja, ha a actionType törlődik.</span><span class="sxs-lookup"><span data-stu-id="c9d43-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d43-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d43-119">CommonParameters</span></span>
<span data-ttu-id="c9d43-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9d43-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d43-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c9d43-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d43-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9d43-122">INPUTS</span></span>

### <span data-ttu-id="c9d43-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="c9d43-123">None</span></span>

## <span data-ttu-id="c9d43-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9d43-124">OUTPUTS</span></span>

### <span data-ttu-id="c9d43-125">Microsoft. Azure. Command. FrontDoor. models. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="c9d43-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="c9d43-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9d43-126">NOTES</span></span>

## <span data-ttu-id="c9d43-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9d43-127">RELATED LINKS</span></span>
