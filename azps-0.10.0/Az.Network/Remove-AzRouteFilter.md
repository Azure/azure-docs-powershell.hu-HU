---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: 02f3e0a151fe8dc810e8530af88059371139f08c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843774"
---
# <span data-ttu-id="e017a-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e017a-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="e017a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e017a-102">SYNOPSIS</span></span>
<span data-ttu-id="e017a-103">{{Töltse ki a szinopszist}}</span><span class="sxs-lookup"><span data-stu-id="e017a-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="e017a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e017a-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e017a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e017a-105">DESCRIPTION</span></span>
<span data-ttu-id="e017a-106">{{Kitöltendő a Leírás}}</span><span class="sxs-lookup"><span data-stu-id="e017a-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e017a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e017a-107">EXAMPLES</span></span>

### <span data-ttu-id="e017a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e017a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e017a-109">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="e017a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e017a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e017a-110">PARAMETERS</span></span>

### <span data-ttu-id="e017a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e017a-111">-DefaultProfile</span></span>
<span data-ttu-id="e017a-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e017a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e017a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e017a-113">-Force</span></span>
<span data-ttu-id="e017a-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e017a-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e017a-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e017a-115">-Name</span></span>
<span data-ttu-id="e017a-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="e017a-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e017a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e017a-117">-PassThru</span></span>
<span data-ttu-id="e017a-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e017a-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e017a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e017a-119">-ResourceGroupName</span></span>
<span data-ttu-id="e017a-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e017a-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e017a-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e017a-121">-Confirm</span></span>
<span data-ttu-id="e017a-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e017a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e017a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e017a-123">-WhatIf</span></span>
<span data-ttu-id="e017a-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e017a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e017a-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e017a-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e017a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e017a-126">CommonParameters</span></span>
<span data-ttu-id="e017a-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e017a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e017a-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e017a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e017a-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e017a-129">INPUTS</span></span>

### <span data-ttu-id="e017a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e017a-130">System.String</span></span>

## <span data-ttu-id="e017a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e017a-131">OUTPUTS</span></span>

### <span data-ttu-id="e017a-132">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="e017a-132">System.Object</span></span>

## <span data-ttu-id="e017a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e017a-133">NOTES</span></span>

## <span data-ttu-id="e017a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e017a-134">RELATED LINKS</span></span>

