---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 373647cfc06c36a510a8208424d00087f00e693e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492255"
---
# <span data-ttu-id="13819-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="13819-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="13819-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13819-102">SYNOPSIS</span></span>
<span data-ttu-id="13819-103">Adathordozó-szolgáltatás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="13819-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13819-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13819-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13819-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13819-105">DESCRIPTION</span></span>
<span data-ttu-id="13819-106">A **Remove-AzureRmMediaService** parancsmag eltávolítja a médiafájlt.</span><span class="sxs-lookup"><span data-stu-id="13819-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="13819-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13819-107">EXAMPLES</span></span>

### <span data-ttu-id="13819-108">1. példa: a médiaadatfolyam-szolgáltatás eltávolítása</span><span class="sxs-lookup"><span data-stu-id="13819-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="13819-109">Ez a parancs eltávolítja a MediaService0011 nevű médiafájlt a ResourceGroup001 nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="13819-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="13819-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13819-110">PARAMETERS</span></span>

### <span data-ttu-id="13819-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="13819-111">-AccountName</span></span>
<span data-ttu-id="13819-112">Annak a médiafájlnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="13819-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13819-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13819-113">-DefaultProfile</span></span>
<span data-ttu-id="13819-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="13819-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13819-115">-Force</span><span class="sxs-lookup"><span data-stu-id="13819-115">-Force</span></span>
<span data-ttu-id="13819-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="13819-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13819-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13819-117">-ResourceGroupName</span></span>
<span data-ttu-id="13819-118">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13819-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13819-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13819-119">-Confirm</span></span>
<span data-ttu-id="13819-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13819-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13819-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13819-121">-WhatIf</span></span>
<span data-ttu-id="13819-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13819-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13819-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13819-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13819-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13819-124">CommonParameters</span></span>
<span data-ttu-id="13819-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13819-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13819-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13819-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13819-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13819-127">INPUTS</span></span>

### <span data-ttu-id="13819-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="13819-128">None</span></span>
<span data-ttu-id="13819-129">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="13819-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="13819-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13819-130">OUTPUTS</span></span>

### <span data-ttu-id="13819-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13819-131">System.Boolean</span></span>

## <span data-ttu-id="13819-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13819-132">NOTES</span></span>

## <span data-ttu-id="13819-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13819-133">RELATED LINKS</span></span>

[<span data-ttu-id="13819-134">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="13819-134">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="13819-135">Új – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="13819-135">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="13819-136">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="13819-136">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


