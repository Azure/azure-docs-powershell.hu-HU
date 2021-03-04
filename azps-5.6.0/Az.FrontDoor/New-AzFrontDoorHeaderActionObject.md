---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: ad005dbf386bc8340fa0da0c5e8dac1d11bf4bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928130"
---
# <span data-ttu-id="feb46-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="feb46-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="feb46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb46-102">SYNOPSIS</span></span>
<span data-ttu-id="feb46-103">PSHeaderAction objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="feb46-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="feb46-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="feb46-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="feb46-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="feb46-105">DESCRIPTION</span></span>
<span data-ttu-id="feb46-106">PSHeaderAction objektumot hoz létre a PSRulesEngineAction objektum létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="feb46-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="feb46-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="feb46-107">EXAMPLES</span></span>

### <span data-ttu-id="feb46-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="feb46-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="feb46-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feb46-109">PARAMETERS</span></span>

### <span data-ttu-id="feb46-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb46-110">-DefaultProfile</span></span>
<span data-ttu-id="feb46-111">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="feb46-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feb46-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="feb46-112">-HeaderActionType</span></span>
<span data-ttu-id="feb46-113">Az élőfejre alkalmazandó kezelés típusa.</span><span class="sxs-lookup"><span data-stu-id="feb46-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="feb46-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="feb46-114">-HeaderName</span></span>
<span data-ttu-id="feb46-115">Annak a fejlécnek a neve, amelyre a művelet vonatkozni fog.</span><span class="sxs-lookup"><span data-stu-id="feb46-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="feb46-116">-Érték</span><span class="sxs-lookup"><span data-stu-id="feb46-116">-Value</span></span>
<span data-ttu-id="feb46-117">Az az érték, amely alapján frissíteni kell a megadott fejlécnevet.</span><span class="sxs-lookup"><span data-stu-id="feb46-117">The value to update the given header name with.</span></span>
<span data-ttu-id="feb46-118">Ez az érték nem használatos, ha az actionType értéke Delete.</span><span class="sxs-lookup"><span data-stu-id="feb46-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="feb46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb46-119">CommonParameters</span></span>
<span data-ttu-id="feb46-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb46-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="feb46-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb46-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="feb46-122">INPUTS</span></span>

### <span data-ttu-id="feb46-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="feb46-123">None</span></span>

## <span data-ttu-id="feb46-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="feb46-124">OUTPUTS</span></span>

### <span data-ttu-id="feb46-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="feb46-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="feb46-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="feb46-126">NOTES</span></span>

## <span data-ttu-id="feb46-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="feb46-127">RELATED LINKS</span></span>
