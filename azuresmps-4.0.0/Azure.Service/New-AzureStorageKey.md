---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016203"
---
# <span data-ttu-id="8a741-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="8a741-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="8a741-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a741-102">SYNOPSIS</span></span>
<span data-ttu-id="8a741-103">Azure Storage-fiókhoz tartozó tárolási kulcsok újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="8a741-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="8a741-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a741-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a741-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a741-105">DESCRIPTION</span></span>
<span data-ttu-id="8a741-106">A **New-AzureStorageKey** parancsmag regenerálta az Azure-tárterületet tároló fiók elsődleges vagy másodlagos kulcsát.</span><span class="sxs-lookup"><span data-stu-id="8a741-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="8a741-107">Egy olyan objektumot ad eredményül, amely a tárolási fiók nevét, az elsődleges kulcsot és a másodlagos kulcsot tulajdonságként tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="8a741-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="8a741-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8a741-108">EXAMPLES</span></span>

### <span data-ttu-id="8a741-109">1. példa: elsődleges tárolási kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="8a741-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="8a741-110">Ez a parancs újra létrehozta az elsődleges tárterületet a ContosoStore01-tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="8a741-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="8a741-111">2. példa: a másodlagos tárterület újragenerálása és egy változóban való mentése</span><span class="sxs-lookup"><span data-stu-id="8a741-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="8a741-112">Ez a parancs újra létrehozta a ContosoStore01-tárterület másodlagos tárolási kulcsát, és a $ContosoStoreKeyban tárolja a frissített tárterület-azonosító kulcs adatait.</span><span class="sxs-lookup"><span data-stu-id="8a741-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="8a741-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a741-113">PARAMETERS</span></span>

### <span data-ttu-id="8a741-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a741-114">-InformationAction</span></span>
<span data-ttu-id="8a741-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="8a741-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a741-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8a741-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a741-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="8a741-117">Continue</span></span>
- <span data-ttu-id="8a741-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="8a741-118">Ignore</span></span>
- <span data-ttu-id="8a741-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="8a741-119">Inquire</span></span>
- <span data-ttu-id="8a741-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a741-120">SilentlyContinue</span></span>
- <span data-ttu-id="8a741-121">állj</span><span class="sxs-lookup"><span data-stu-id="8a741-121">Stop</span></span>
- <span data-ttu-id="8a741-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="8a741-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a741-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a741-123">-InformationVariable</span></span>
<span data-ttu-id="8a741-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="8a741-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a741-125">-Típus</span><span class="sxs-lookup"><span data-stu-id="8a741-125">-KeyType</span></span>
<span data-ttu-id="8a741-126">Az újragenerálni kívánt kulcs megadása.</span><span class="sxs-lookup"><span data-stu-id="8a741-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="8a741-127">Az érvényes értékek: elsődleges és másodlagos.</span><span class="sxs-lookup"><span data-stu-id="8a741-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a741-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="8a741-128">-Profile</span></span>
<span data-ttu-id="8a741-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="8a741-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a741-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="8a741-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a741-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8a741-131">-StorageAccountName</span></span>
<span data-ttu-id="8a741-132">Annak az Azure-tárterület-fióknak a nevét adja meg, amelynek a kulcsát újra létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="8a741-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a741-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a741-133">CommonParameters</span></span>
<span data-ttu-id="8a741-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a741-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a741-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a741-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a741-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a741-136">INPUTS</span></span>

## <span data-ttu-id="8a741-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a741-137">OUTPUTS</span></span>

### <span data-ttu-id="8a741-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="8a741-138">StorageServiceKeys</span></span>

## <span data-ttu-id="8a741-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a741-139">NOTES</span></span>

## <span data-ttu-id="8a741-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a741-140">RELATED LINKS</span></span>

[<span data-ttu-id="8a741-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="8a741-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


