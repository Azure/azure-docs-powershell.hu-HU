---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015549"
---
# <span data-ttu-id="f9a64-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9a64-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="f9a64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9a64-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a64-103">Az aktuális Azure-előfizetés tárolási fiókjainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f9a64-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="f9a64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9a64-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f9a64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9a64-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a64-106">A **Get-AzureStorageAccount** parancsmag egy olyan objektumot ad eredményül, amely az aktuális előfizetés tárolási fiókjaival kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f9a64-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="f9a64-107">Ha meg van adva a *StorageAccountName* paraméter, akkor csak az adott tárterület-fiókról kapott információkat adja vissza a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f9a64-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="f9a64-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f9a64-108">EXAMPLES</span></span>

### <span data-ttu-id="f9a64-109">1. példa: az összes tárterület-fiók visszaadása</span><span class="sxs-lookup"><span data-stu-id="f9a64-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="f9a64-110">Ez a parancs egy olyan objektumot ad eredményül, amely az aktuális előfizetéshez társított összes tárolási fiókot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f9a64-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="f9a64-111">2. példa: adott fiókhoz tartozó fiókadatok visszaadása</span><span class="sxs-lookup"><span data-stu-id="f9a64-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="f9a64-112">Ez a parancs olyan objektumot ad eredményül, amely csak a ContosoStore01-fiók adatait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f9a64-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="f9a64-113">3. példa: a tárolási fiókok táblázatának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="f9a64-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="f9a64-114">Ez a parancs egy olyan objektumot ad eredményül, amely az aktuális előfizetéshez társított összes tárolási fiókot tartalmazza, és a fiók nevét, a fiók címkéjét és a tárolási helyét tartalmazó táblázatként jeleníti meg őket.</span><span class="sxs-lookup"><span data-stu-id="f9a64-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="f9a64-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9a64-115">PARAMETERS</span></span>

### <span data-ttu-id="f9a64-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f9a64-116">-InformationAction</span></span>
<span data-ttu-id="f9a64-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f9a64-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f9a64-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f9a64-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f9a64-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f9a64-119">Continue</span></span>
- <span data-ttu-id="f9a64-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f9a64-120">Ignore</span></span>
- <span data-ttu-id="f9a64-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f9a64-121">Inquire</span></span>
- <span data-ttu-id="f9a64-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f9a64-122">SilentlyContinue</span></span>
- <span data-ttu-id="f9a64-123">állj</span><span class="sxs-lookup"><span data-stu-id="f9a64-123">Stop</span></span>
- <span data-ttu-id="f9a64-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f9a64-124">Suspend</span></span>

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

### <span data-ttu-id="f9a64-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f9a64-125">-InformationVariable</span></span>
<span data-ttu-id="f9a64-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f9a64-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f9a64-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="f9a64-127">-Profile</span></span>
<span data-ttu-id="f9a64-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f9a64-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f9a64-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f9a64-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f9a64-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f9a64-130">-StorageAccountName</span></span>
<span data-ttu-id="f9a64-131">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9a64-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="f9a64-132">Ha meg van adva, ez a parancsmag csak a megadott tárterület-objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="f9a64-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a64-133">CommonParameters</span></span>
<span data-ttu-id="f9a64-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9a64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a64-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a64-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a64-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9a64-136">INPUTS</span></span>

## <span data-ttu-id="f9a64-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9a64-137">OUTPUTS</span></span>

### <span data-ttu-id="f9a64-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="f9a64-138">ManagementOperationContext</span></span>

## <span data-ttu-id="f9a64-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9a64-139">NOTES</span></span>
* <span data-ttu-id="f9a64-140">`help node-dev`Ha segítségre van szüksége Node.js fejlesztéssel kapcsolatos parancsmagokkal kapcsolatban, adja meg a súgót.</span><span class="sxs-lookup"><span data-stu-id="f9a64-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="f9a64-141">`help php-dev`Ha segítségre van szüksége a PHP fejlesztéssel kapcsolatos parancsmagokhoz, írja be a segítséget.</span><span class="sxs-lookup"><span data-stu-id="f9a64-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="f9a64-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9a64-142">RELATED LINKS</span></span>

[<span data-ttu-id="f9a64-143">Új – AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9a64-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="f9a64-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f9a64-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


