---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015681"
---
# <span data-ttu-id="cc353-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cc353-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="cc353-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc353-102">SYNOPSIS</span></span>
<span data-ttu-id="cc353-103">Egy Azure RemoteApp-gyűjtemény sablonját exportálja a megadott Azure Storage-fiókba.</span><span class="sxs-lookup"><span data-stu-id="cc353-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="cc353-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc353-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc353-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc353-105">DESCRIPTION</span></span>
<span data-ttu-id="cc353-106">Az **export-AzureRemoteAppTemplateImage** parancsmag egy Azure RemoteApp-gyűjtemény sablonját exportálja a megadott Azure Storage-fiókba.</span><span class="sxs-lookup"><span data-stu-id="cc353-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="cc353-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cc353-107">EXAMPLES</span></span>

### <span data-ttu-id="cc353-108">1. példa: a sablon képének exportálása az Azure Storage-fiókjába</span><span class="sxs-lookup"><span data-stu-id="cc353-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="cc353-109">Ez a parancs exportálja a contoso nevű gyűjtemény ContainerName nevű tárolóját a AccountName és a Key AccountKey megadott Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="cc353-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="cc353-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc353-110">PARAMETERS</span></span>

### <span data-ttu-id="cc353-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="cc353-111">-CollectionName</span></span>
<span data-ttu-id="cc353-112">A forrás Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc353-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc353-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="cc353-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="cc353-114">Egy tároló nevét adja meg a cél Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="cc353-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc353-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cc353-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="cc353-116">A cél Azure tárterület-fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc353-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc353-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cc353-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="cc353-118">A cél Azure tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc353-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc353-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cc353-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="cc353-120">Jelzi, hogy a parancsmag felülírja a meglévő sablon képét.</span><span class="sxs-lookup"><span data-stu-id="cc353-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

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

### <span data-ttu-id="cc353-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="cc353-121">-Profile</span></span>
<span data-ttu-id="cc353-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="cc353-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc353-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="cc353-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc353-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cc353-124">-Confirm</span></span>
<span data-ttu-id="cc353-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cc353-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc353-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc353-126">-WhatIf</span></span>
<span data-ttu-id="cc353-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cc353-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc353-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc353-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc353-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc353-129">CommonParameters</span></span>
<span data-ttu-id="cc353-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc353-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc353-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc353-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc353-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc353-132">INPUTS</span></span>

## <span data-ttu-id="cc353-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc353-133">OUTPUTS</span></span>

## <span data-ttu-id="cc353-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc353-134">NOTES</span></span>

## <span data-ttu-id="cc353-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc353-135">RELATED LINKS</span></span>

[<span data-ttu-id="cc353-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cc353-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="cc353-137">Új – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cc353-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="cc353-138">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cc353-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="cc353-139">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="cc353-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


