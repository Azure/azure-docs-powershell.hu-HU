---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 3dfa3343edc82aaaf2c51a4e18ebc413ea3023c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495971"
---
# <span data-ttu-id="abdc6-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="abdc6-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="abdc6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abdc6-102">SYNOPSIS</span></span>
<span data-ttu-id="abdc6-103">Módosítja egy meglévő Media-szolgáltatás megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="abdc6-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abdc6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abdc6-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abdc6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="abdc6-105">DESCRIPTION</span></span>
<span data-ttu-id="abdc6-106">A **set-AzureRmMediaService** parancsmag egy meglévő Media-szolgáltatás megadott tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="abdc6-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="abdc6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="abdc6-107">EXAMPLES</span></span>

### <span data-ttu-id="abdc6-108">Példa 1: meglévő Media-szolgáltatás módosítása</span><span class="sxs-lookup"><span data-stu-id="abdc6-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="abdc6-109">Az első parancs létrehozza a címkék sorozatát, és azokat a címkéket a $Tags nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="abdc6-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="abdc6-110">Ez a második parancs frissíti a MediaService001 nevű, a ResourceGroup123 nevű erőforráscsoporthoz tartozó Media szolgáltatását, amely a $Tags változóban tárolt címkéket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="abdc6-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="abdc6-111">A parancs a $StorageAccounts változóban tárolt tárolási konfigurációs objektumok tömbjét is használja.</span><span class="sxs-lookup"><span data-stu-id="abdc6-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="abdc6-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abdc6-112">PARAMETERS</span></span>

### <span data-ttu-id="abdc6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="abdc6-113">-AccountName</span></span>
<span data-ttu-id="abdc6-114">Annak a médiafájlnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="abdc6-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="abdc6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abdc6-115">-DefaultProfile</span></span>
<span data-ttu-id="abdc6-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="abdc6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abdc6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abdc6-117">-ResourceGroupName</span></span>
<span data-ttu-id="abdc6-118">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="abdc6-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="abdc6-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="abdc6-119">-StorageAccounts</span></span>
<span data-ttu-id="abdc6-120">Megadja azokat a tárolási fiókokat, amelyeket ez a parancsmag a Media szolgáltatással társít.</span><span class="sxs-lookup"><span data-stu-id="abdc6-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="abdc6-121">-Címke</span><span class="sxs-lookup"><span data-stu-id="abdc6-121">-Tag</span></span>
<span data-ttu-id="abdc6-122">A médiafájlhoz társított címkék.</span><span class="sxs-lookup"><span data-stu-id="abdc6-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="abdc6-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abdc6-123">-Confirm</span></span>
<span data-ttu-id="abdc6-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abdc6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abdc6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abdc6-125">-WhatIf</span></span>
<span data-ttu-id="abdc6-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abdc6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abdc6-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abdc6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abdc6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abdc6-128">CommonParameters</span></span>
<span data-ttu-id="abdc6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abdc6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abdc6-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abdc6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abdc6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdc6-131">INPUTS</span></span>

### <span data-ttu-id="abdc6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="abdc6-132">System.String</span></span>

### <span data-ttu-id="abdc6-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="abdc6-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="abdc6-134">Microsoft. Azure. commands. Media. models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="abdc6-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="abdc6-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abdc6-135">OUTPUTS</span></span>

### <span data-ttu-id="abdc6-136">Microsoft. Azure. commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="abdc6-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="abdc6-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abdc6-137">NOTES</span></span>

## <span data-ttu-id="abdc6-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abdc6-138">RELATED LINKS</span></span>

[<span data-ttu-id="abdc6-139">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="abdc6-139">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="abdc6-140">Új – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="abdc6-140">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="abdc6-141">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="abdc6-141">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


