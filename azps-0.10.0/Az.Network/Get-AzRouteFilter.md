---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841529"
---
# <span data-ttu-id="1f4be-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f4be-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="1f4be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f4be-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4be-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="1f4be-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="1f4be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f4be-104">SYNTAX</span></span>

### <span data-ttu-id="1f4be-105">Nincs kibontva</span><span class="sxs-lookup"><span data-stu-id="1f4be-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f4be-106">Bővíteni</span><span class="sxs-lookup"><span data-stu-id="1f4be-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f4be-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f4be-107">DESCRIPTION</span></span>
<span data-ttu-id="1f4be-108">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="1f4be-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1f4be-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1f4be-109">EXAMPLES</span></span>

### <span data-ttu-id="1f4be-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1f4be-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1f4be-111">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="1f4be-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="1f4be-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f4be-112">PARAMETERS</span></span>

### <span data-ttu-id="1f4be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4be-113">-DefaultProfile</span></span>
<span data-ttu-id="1f4be-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f4be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f4be-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1f4be-115">-ExpandResource</span></span>
<span data-ttu-id="1f4be-116">A kibontani kívánt erőforrás-hivatkozás.</span><span class="sxs-lookup"><span data-stu-id="1f4be-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="1f4be-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1f4be-117">-Name</span></span>
<span data-ttu-id="1f4be-118">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1f4be-118">The resource name.</span></span>

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

### <span data-ttu-id="1f4be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4be-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f4be-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="1f4be-120">The resource group name.</span></span>

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

### <span data-ttu-id="1f4be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4be-121">CommonParameters</span></span>
<span data-ttu-id="1f4be-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f4be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4be-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f4be-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4be-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f4be-124">INPUTS</span></span>

### <span data-ttu-id="1f4be-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1f4be-125">System.String</span></span>

## <span data-ttu-id="1f4be-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f4be-126">OUTPUTS</span></span>

### <span data-ttu-id="1f4be-127">Microsoft. Azure. commands. Network. models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1f4be-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1f4be-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f4be-128">NOTES</span></span>

## <span data-ttu-id="1f4be-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f4be-129">RELATED LINKS</span></span>

