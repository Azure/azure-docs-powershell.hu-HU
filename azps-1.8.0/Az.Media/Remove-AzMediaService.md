---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: f9d0ee722f828aba251c9776c231338b54c0580c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835177"
---
# <span data-ttu-id="4b089-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b089-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="4b089-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4b089-102">SYNOPSIS</span></span>
<span data-ttu-id="4b089-103">Adathordozó-szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4b089-103">Removes a media service.</span></span>

## <span data-ttu-id="4b089-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4b089-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b089-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4b089-105">DESCRIPTION</span></span>
<span data-ttu-id="4b089-106">A **Remove-AzMediaService** parancsmag eltávolítja a médiafájlt.</span><span class="sxs-lookup"><span data-stu-id="4b089-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="4b089-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4b089-107">EXAMPLES</span></span>

### <span data-ttu-id="4b089-108">1. példa: a médiaadatfolyam-szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4b089-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="4b089-109">Ez a parancs eltávolítja a MediaService0011 nevű médiafájlt a ResourceGroup001 nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="4b089-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="4b089-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4b089-110">PARAMETERS</span></span>

### <span data-ttu-id="4b089-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4b089-111">-AccountName</span></span>
<span data-ttu-id="4b089-112">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="4b089-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b089-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b089-113">-DefaultProfile</span></span>
<span data-ttu-id="4b089-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4b089-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b089-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4b089-115">-Force</span></span>
<span data-ttu-id="4b089-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4b089-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b089-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b089-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b089-118">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4b089-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b089-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4b089-119">-Confirm</span></span>
<span data-ttu-id="4b089-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4b089-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b089-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b089-121">-WhatIf</span></span>
<span data-ttu-id="4b089-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4b089-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b089-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b089-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b089-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b089-124">CommonParameters</span></span>
<span data-ttu-id="4b089-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4b089-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b089-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b089-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b089-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b089-127">INPUTS</span></span>

### <span data-ttu-id="4b089-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4b089-128">System.String</span></span>

## <span data-ttu-id="4b089-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b089-129">OUTPUTS</span></span>

### <span data-ttu-id="4b089-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b089-130">System.Boolean</span></span>

## <span data-ttu-id="4b089-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4b089-131">NOTES</span></span>

## <span data-ttu-id="4b089-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b089-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b089-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b089-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="4b089-134">Új – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b089-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="4b089-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="4b089-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


