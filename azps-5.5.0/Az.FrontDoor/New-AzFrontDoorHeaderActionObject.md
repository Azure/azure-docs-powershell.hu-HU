---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204078"
---
# <span data-ttu-id="346bd-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="346bd-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="346bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="346bd-102">SYNOPSIS</span></span>
<span data-ttu-id="346bd-103">PSHeaderAction objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="346bd-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="346bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="346bd-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="346bd-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="346bd-105">DESCRIPTION</span></span>
<span data-ttu-id="346bd-106">PSHeaderAction objektumot hoz létre a PSRulesEngineAction objektum létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="346bd-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="346bd-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="346bd-107">EXAMPLES</span></span>

### <span data-ttu-id="346bd-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="346bd-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="346bd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="346bd-109">PARAMETERS</span></span>

### <span data-ttu-id="346bd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346bd-110">-DefaultProfile</span></span>
<span data-ttu-id="346bd-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="346bd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="346bd-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="346bd-112">-HeaderActionType</span></span>
<span data-ttu-id="346bd-113">Az élőfejre alkalmazandó kezelés típusa.</span><span class="sxs-lookup"><span data-stu-id="346bd-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="346bd-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="346bd-114">-HeaderName</span></span>
<span data-ttu-id="346bd-115">Annak a fejlécnek a neve, amelyre a művelet vonatkozni fog.</span><span class="sxs-lookup"><span data-stu-id="346bd-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="346bd-116">-Érték</span><span class="sxs-lookup"><span data-stu-id="346bd-116">-Value</span></span>
<span data-ttu-id="346bd-117">Az az érték, amely alapján frissíteni kell a megadott fejlécnevet.</span><span class="sxs-lookup"><span data-stu-id="346bd-117">The value to update the given header name with.</span></span>
<span data-ttu-id="346bd-118">Ez az érték nem használatos, ha az actionType értéke Delete.</span><span class="sxs-lookup"><span data-stu-id="346bd-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="346bd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346bd-119">CommonParameters</span></span>
<span data-ttu-id="346bd-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="346bd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346bd-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="346bd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346bd-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="346bd-122">INPUTS</span></span>

### <span data-ttu-id="346bd-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="346bd-123">None</span></span>

## <span data-ttu-id="346bd-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="346bd-124">OUTPUTS</span></span>

### <span data-ttu-id="346bd-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="346bd-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="346bd-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="346bd-126">NOTES</span></span>

## <span data-ttu-id="346bd-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="346bd-127">RELATED LINKS</span></span>
