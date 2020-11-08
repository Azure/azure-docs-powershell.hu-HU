---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025661"
---
# <span data-ttu-id="d4020-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4020-101">Set-AzMediaService</span></span>

## <span data-ttu-id="d4020-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4020-102">SYNOPSIS</span></span>
<span data-ttu-id="d4020-103">Módosítja egy meglévő Media-szolgáltatás megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="d4020-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="d4020-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4020-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4020-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4020-105">DESCRIPTION</span></span>
<span data-ttu-id="d4020-106">A **set-AzMediaService** parancsmag egy meglévő Media-szolgáltatás megadott tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="d4020-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="d4020-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d4020-107">EXAMPLES</span></span>

### <span data-ttu-id="d4020-108">Példa 1: meglévő Media-szolgáltatás módosítása</span><span class="sxs-lookup"><span data-stu-id="d4020-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="d4020-109">Az első parancs létrehozza a címkék sorozatát, és azokat a címkéket a $Tags nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d4020-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="d4020-110">Ez a második parancs frissíti a MediaService001 nevű, a ResourceGroup123 nevű erőforráscsoporthoz tartozó Media szolgáltatását, amely a $Tags változóban tárolt címkéket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4020-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="d4020-111">A parancs a $StorageAccounts változóban tárolt tárolási konfigurációs objektumok tömbjét is használja.</span><span class="sxs-lookup"><span data-stu-id="d4020-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="d4020-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4020-112">PARAMETERS</span></span>

### <span data-ttu-id="d4020-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d4020-113">-AccountName</span></span>
<span data-ttu-id="d4020-114">Annak a médiafájlnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="d4020-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d4020-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4020-115">-DefaultProfile</span></span>
<span data-ttu-id="d4020-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4020-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4020-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4020-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4020-118">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4020-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d4020-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d4020-119">-StorageAccounts</span></span>
<span data-ttu-id="d4020-120">Megadja azokat a tárolási fiókokat, amelyeket ez a parancsmag a Media szolgáltatással társít.</span><span class="sxs-lookup"><span data-stu-id="d4020-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="d4020-121">-Tag</span></span>
<span data-ttu-id="d4020-122">A médiafájlhoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="d4020-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4020-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4020-123">-Confirm</span></span>
<span data-ttu-id="d4020-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4020-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4020-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4020-125">-WhatIf</span></span>
<span data-ttu-id="d4020-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4020-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4020-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4020-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4020-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4020-128">CommonParameters</span></span>
<span data-ttu-id="d4020-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4020-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4020-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4020-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4020-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4020-131">INPUTS</span></span>

### <span data-ttu-id="d4020-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d4020-132">System.String</span></span>

### <span data-ttu-id="d4020-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d4020-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d4020-134">Microsoft. Azure. commands. Media. models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="d4020-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="d4020-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4020-135">OUTPUTS</span></span>

### <span data-ttu-id="d4020-136">Microsoft. Azure. commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="d4020-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="d4020-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4020-137">NOTES</span></span>

## <span data-ttu-id="d4020-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4020-138">RELATED LINKS</span></span>

[<span data-ttu-id="d4020-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4020-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="d4020-140">Új – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4020-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="d4020-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4020-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


