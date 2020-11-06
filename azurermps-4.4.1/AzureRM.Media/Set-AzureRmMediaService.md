---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 19db06ff5563e954124ab36274d62cce0e51b3a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500815"
---
# <span data-ttu-id="b7fc9-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b7fc9-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="b7fc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fc9-103">Módosítja egy meglévő Media-szolgáltatás megadott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7fc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7fc9-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tags <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7fc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="b7fc9-106">A **set-AzureRmMediaService** parancsmag egy meglévő Media-szolgáltatás megadott tulajdonságait módosítja.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="b7fc9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b7fc9-107">EXAMPLES</span></span>

### <span data-ttu-id="b7fc9-108">Példa 1: meglévő Media-szolgáltatás módosítása</span><span class="sxs-lookup"><span data-stu-id="b7fc9-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="b7fc9-109">Az első parancs létrehozza a címkék sorozatát, és azokat a címkéket a $Tags nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="b7fc9-110">Ez a második parancs frissíti a MediaService001 nevű, a ResourceGroup123 nevű erőforráscsoporthoz tartozó Media szolgáltatását, amely a $Tags változóban tárolt címkéket tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="b7fc9-111">A parancs a $StorageAccounts változóban tárolt tárolási konfigurációs objektumok tömbjét is használja.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="b7fc9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7fc9-112">PARAMETERS</span></span>

### <span data-ttu-id="b7fc9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7fc9-113">-AccountName</span></span>
<span data-ttu-id="b7fc9-114">Annak a médiafájlnak a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b7fc9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fc9-115">-ResourceGroupName</span></span>
<span data-ttu-id="b7fc9-116">A Media-szolgáltatást tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b7fc9-117">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b7fc9-117">-StorageAccounts</span></span>
<span data-ttu-id="b7fc9-118">Megadja azokat a tárolási fiókokat, amelyeket ez a parancsmag a Media szolgáltatással társít.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-118">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="b7fc9-119">-Címkék</span><span class="sxs-lookup"><span data-stu-id="b7fc9-119">-Tags</span></span>
<span data-ttu-id="b7fc9-120">A médiaszolgáltató címkéit adja meg.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-120">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="b7fc9-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b7fc9-121">-Confirm</span></span>
<span data-ttu-id="b7fc9-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7fc9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7fc9-123">-WhatIf</span></span>
<span data-ttu-id="b7fc9-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7fc9-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7fc9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fc9-126">-DefaultProfile</span></span>
<span data-ttu-id="b7fc9-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7fc9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7fc9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fc9-128">CommonParameters</span></span>
<span data-ttu-id="b7fc9-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7fc9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fc9-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7fc9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fc9-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7fc9-131">INPUTS</span></span>

## <span data-ttu-id="b7fc9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7fc9-132">OUTPUTS</span></span>

### <span data-ttu-id="b7fc9-133">Microsoft. Azure. commands. Media. models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="b7fc9-133">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="b7fc9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7fc9-134">NOTES</span></span>

## <span data-ttu-id="b7fc9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7fc9-135">RELATED LINKS</span></span>

[<span data-ttu-id="b7fc9-136">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b7fc9-136">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="b7fc9-137">Új – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b7fc9-137">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="b7fc9-138">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="b7fc9-138">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


