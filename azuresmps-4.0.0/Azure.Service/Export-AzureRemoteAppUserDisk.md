---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015678"
---
# <span data-ttu-id="656f4-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="656f4-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="656f4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="656f4-102">SYNOPSIS</span></span>
<span data-ttu-id="656f4-103">Az egyik Azure RemoteApp-gyűjteményből származó összes felhasználói lemez exportálása a megadott Azure Storage-fiókba.</span><span class="sxs-lookup"><span data-stu-id="656f4-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="656f4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="656f4-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="656f4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="656f4-105">DESCRIPTION</span></span>
<span data-ttu-id="656f4-106">Az **AzureRemoteAppUserDisk** parancsmag az Azure RemoteApp-gyűjteményből származó összes felhasználói lemezt exportálja a megadott Azure Storage-fiókba.</span><span class="sxs-lookup"><span data-stu-id="656f4-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="656f4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="656f4-107">EXAMPLES</span></span>

### <span data-ttu-id="656f4-108">1. példa: egy gyűjteményből a megadott Azure Storage-fiókba exportálja az összes felhasználói lemezt.</span><span class="sxs-lookup"><span data-stu-id="656f4-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="656f4-109">Ez a parancs a contoso nevű gyűjteményből a ContainerName nevű tárolóba exportálja az összes felhasználói lemezt a name AccountName és a Key AccountKey nevű megadott Azure Storage fiókban.</span><span class="sxs-lookup"><span data-stu-id="656f4-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="656f4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="656f4-110">PARAMETERS</span></span>

### <span data-ttu-id="656f4-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="656f4-111">-CollectionName</span></span>
<span data-ttu-id="656f4-112">A forrás Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="656f4-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="656f4-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="656f4-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="656f4-114">Egy tároló nevét adja meg a cél Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="656f4-114">Specifies the name of a container in the destination Azure storage account.</span></span>

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

### <span data-ttu-id="656f4-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="656f4-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="656f4-116">A cél Azure tárterület-fiók kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="656f4-116">Specifies the Key of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="656f4-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="656f4-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="656f4-118">A cél Azure tárterület-fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="656f4-118">Specifies the name of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="656f4-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="656f4-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="656f4-120">Azt jelzi, hogy a parancsmag felülírja a meglévő felhasználói lemezt.</span><span class="sxs-lookup"><span data-stu-id="656f4-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

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

### <span data-ttu-id="656f4-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="656f4-121">-Profile</span></span>
<span data-ttu-id="656f4-122">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="656f4-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="656f4-123">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="656f4-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="656f4-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="656f4-124">-Confirm</span></span>
<span data-ttu-id="656f4-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="656f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="656f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="656f4-126">-WhatIf</span></span>
<span data-ttu-id="656f4-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="656f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="656f4-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="656f4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="656f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656f4-129">CommonParameters</span></span>
<span data-ttu-id="656f4-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="656f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656f4-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656f4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656f4-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="656f4-132">INPUTS</span></span>

## <span data-ttu-id="656f4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="656f4-133">OUTPUTS</span></span>

## <span data-ttu-id="656f4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="656f4-134">NOTES</span></span>

## <span data-ttu-id="656f4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="656f4-135">RELATED LINKS</span></span>

[<span data-ttu-id="656f4-136">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="656f4-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="656f4-137">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="656f4-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


