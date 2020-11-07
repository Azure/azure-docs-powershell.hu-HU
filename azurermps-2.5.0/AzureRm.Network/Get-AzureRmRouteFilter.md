---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 007f020d97d0c46f5db5031f4163d669d976f642
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850686"
---
# <span data-ttu-id="3430d-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3430d-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="3430d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3430d-102">SYNOPSIS</span></span>
<span data-ttu-id="3430d-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="3430d-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3430d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3430d-104">SYNTAX</span></span>

### <span data-ttu-id="3430d-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="3430d-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3430d-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="3430d-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3430d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3430d-107">DESCRIPTION</span></span>
<span data-ttu-id="3430d-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="3430d-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3430d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3430d-109">EXAMPLES</span></span>

### <span data-ttu-id="3430d-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3430d-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3430d-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="3430d-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="3430d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3430d-112">PARAMETERS</span></span>

### <span data-ttu-id="3430d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3430d-113">-DefaultProfile</span></span>
<span data-ttu-id="3430d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3430d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3430d-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="3430d-115">-ExpandResource</span></span>
<span data-ttu-id="3430d-116">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="3430d-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3430d-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3430d-117">-Name</span></span>
<span data-ttu-id="3430d-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="3430d-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3430d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3430d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3430d-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="3430d-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3430d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3430d-121">CommonParameters</span></span>
<span data-ttu-id="3430d-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3430d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3430d-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3430d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3430d-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3430d-124">INPUTS</span></span>

### <span data-ttu-id="3430d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3430d-125">System.String</span></span>

## <span data-ttu-id="3430d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3430d-126">OUTPUTS</span></span>

### <span data-ttu-id="3430d-127">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3430d-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3430d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3430d-128">NOTES</span></span>

## <span data-ttu-id="3430d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3430d-129">RELATED LINKS</span></span>

